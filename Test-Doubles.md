Test doubles is an extension to Test-Driven Development that supports good Object-Oriented design by guiding the discovery of a coherent system of types within a code base. It turns out to be less interesting as a technique for isolating tests from third-party libraries than is widely thought.

## Different types of test doubles

* Dummy objects are passed around but never actually used. Usually they are just used to fill parameter lists.
* Stubs provide canned answers to calls made during the test, usually not responding at all to anything outside what's programmed in for the test.
* Fake objects actually have working implementations, but usually take some shortcut which makes them not suitable for production (an in memory database is a good example).
* Mocks are pre-programmed with expectations which form a specification of the calls they are expected to receive. They can throw an exception if they receive a call they don't expect and are checked during verification to ensure they got all the calls they were expecting.
* Spies are stubs that also record some information based on how they were called. One form of this might be an email service that records how many messages it was sent.
 
Read also:
* https://martinfowler.com/articles/mocksArentStubs.html
* http://xunitpatterns.com/Mocks,%20Fakes,%20Stubs%20and%20Dummies.html
* http://blog.ploeh.dk/2013/10/23/mocks-for-commands-stubs-for-queries/
* http://blog.cleancoder.com/uncle-bob/2014/05/14/TheLittleMocker.html

## Principles
* Allow/Setup Queries; Expect/Verify Commands
  * Use Mocks for Commands
    * Commands are all about side effects, and Mocks are all about Behaviour Verification: that is, that side effects occurred
  * Use Stubs for Queries
    * Stubs mainly exist to 'make happy noises', and one of the ways they have to do that, is to return data from dependencies, when return data is required.

* Only mock/stub classes you own
  * Mock Objects is a design technique so programmers should only write mocks for types that they can change. Otherwise they cannot change the design to respond to requirements that arise from the process. Programmers should not write mocks for fixed types, such as those defined by the runtime or external libraries. Instead they should write thin wrappers to implement the application abstractions in terms of the underlying infrastructure. Those wrappers will have been defined as part of a need-driven test. We have found this to be a powerful insight to help programmers understand the technique. It restores the pre-eminence of the design in the use of Mock Objects, which has often been overshadowed by its use for testing interactions with third-party libraries.

* Specify as little as possible in a test 
  * When testing with Mock Objects it is important to find the right balance between an accurate specification of a unit's required behaviour and a flexible test that allows easy evolution of the code base. One of the risks with TDD is that tests become “brittle”, that is they fail when a programmer makes unrelated changes to the application code. They have been over-specified to check features that are an artefact of the implementation, not an expression of some requirement in the object. A test suite that contains a lot of brittle tests will slow down development and inhibit refactoring. The solution is to re-examine the code and see if either the specification should be weakened, or the object structure is wrong and should be changed. Following Einstein, a specification should be as precise as possible, but not more precise.

* Don’t use mocks/stubs to test boundary/isolated objects
  * If an object has no relationships to other objects in the system, it does not need to be tested with mock objects. A test for such an object only needs to make assertions about values returned from its methods. Typically, these objects store data, perform independent calculations or represent atomic values. While this may seem an obvious thing to say, we have encountered people trying to use mock objects where they don’t actually need to.

* Don’t add behaviour 
  * Mock objects are still stubs and should not add any additional complexity to the test environment, their behaviour should be obvious [10]. We find that an urge to start adding real behaviour to a mock object is usually a symptom of misplaced responsibilities. A common example of this is when one mock has to interpret its input to return another mock, perhaps by parsing an event message. This introduces a risk of testing the test infrastructure rather than the target code. For example:
    ```
    mock.expect(once()) .method("retrieve").with(eq(KEY1)) .willReturn(VALUE1); 
    mock.expect(once()) .method("retrieve").with(eq(KEY2)) .willReturn(VALUE2);
    ```

* Only mock/stub your immediate neighbours 
  * An object that has to navigate a network of objects in its implementation is likely to be brittle because it has too many dependencies. One symptom of this is tests that are complex to set up and difficult to read because they have to construct a similar network of mock objects. Unit tests work best when they focus on testing one thing at a time and only setting expectations on objects that are nearest neighbours. The solution might be to check that you are testing the right object, or to introduce a role to bridge between the object and its surroundings.

* Too Many Mocks/Stubs
  * A similar problem arises when a test has to pass too many mock objects to the target code, even if they are all immediate neighbours. Again, the tests is likely to be complex to set up and hard to read. Again the solution might be to change misaligned responsibilities, or to introduce an intermediate role. Alternatively, it is possible that the object under test is too large and should be broken up into smaller objects that will be more focussed and easier to test

## Footnotes
* From Sandro's videos with Uncle Bob: "Mocking is not about testing, it is about designing the collaboration between classes".