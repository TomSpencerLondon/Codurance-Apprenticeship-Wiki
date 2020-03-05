* Principles
  * Tests should test one thing only
  * Test one logical assertion
  * Don't mix asserts of state and collaborations together
    * State = method return value / object state via properties/getters
    * Collaboration = Use a mock to verify correct collaboration between objects
  * Make tests independent of each other
  * Don't refactor with failing test (don’t refactor on red)
  * Organise your unit tests to reflect your production code (similar project structure)
  * Keep your tests and production code separate
  * Do not use production data and code to test production code
    * Use data you can control for your tests
  * If your tests are difficult to write or maintain, consider changing the design

* Red
  * Create more specific tests to drive a more generic solution (Triangulate)
  * Give your test meaningful names (behaviour / goal-oriented) - that reflects your business domain
  * Write the assertion first and work backwards
  * See the test fail for the right reason
  * Ensure you have meaningful feedback from failing tests
  * Organize your test in Arrange, Act and Assert blocks
    * Arrange (aka Given) – all necessary preconditions and inputs.
    * Act (aka When) – on the object or method under test.
    * Assert (aka Then) – that the expected results have occurred.
    * Structure the code in tests to reflect these concepts.
* To Green
  * Write the simplest code to pass the test
  * Consider using Transformation Priority Premise
  * Write any code that makes you get to the refactor phase quicker
  * It is okay to write any code that you might improve at a later stage
* Green -> Refactor
  * Refactor aggressively and constantly
  * Treat tests as first class code
  * Use the IDE to refactor quickly and safely
  * Use the Rule of 3 to tackle duplication
    * Code can be copied once, but that when the same code is used three times, it should be abstracted. Or if you need something once, build it. If you need something twice, pay attention. If you need it a third time, abstract it.
    * But keep in mind that duplication is cheaper than the wrong abstractions