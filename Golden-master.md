The Golden Master technique is very useful when a clear input and output is easy to obtain on the system level. There are some cases where the Golden Master technique can be applied with difficulty or where it cannot be applied at all. We will discuss these situations further as well.

For all the given situations we need to think if the system tests generated with the Golden Master are enough, or we need to start adding other types of tests like unit tests, component tests, integration tests, security tests, etc.
The Golden Master technique is based on the following steps:

1. Find the way the system delivers its outputs
   * Check for clear outputs of the system: console, data layer, logger, file system, etc.

2. Find a way to capture the output of the system without changing the production code
   * Think if that output can be “stolen” without changing the production code. For example you could “steal” the console output by redirecting the stream of the console to an in-memory stream. Another example would be injecting an implementation of a data layer interface that would write to another data source than the production code would.

3. Find a pattern of the outputs
   * The output of the system could be text or a data structures tree or another type of stream. Starting from this output type you can decide if you could go on to the next step.

4. Generate enough random inputs and persist the tuple input/output
   * In the case you can persist the outputs to a simple data repository, you can think about what are the inputs for the corresponding outputs. Here the magic consists in finding a good balance of random or pseudo-random inputs. We need inputs that would cover most of the system with tests, but in the same time the test would run in seconds. For example in the case of a text generating algorithm we need to decide if we want to feed the system with 1000 or one million entry data. Maybe 10 000 input data are enough. We will anyway check the tests coverage during the last stage.
   * We need to persist the pair input-output. The output would be the Golden Master, the reference data we will always check our SUT against.

5. Write a system test to check the SUT against the previously persisted data
   * Now that we have a way to “steal” the outputs and we have a guess about how to generate enough input-output pairs, but not too many, we can call the system and check it against the outputs for a given input. We need to check if the test touches the SUT and if it passes. We also need to check that the test runs fast enough, in seconds.

6. Commit the test
   * Always when a green test passes we need to commit the code to a local source control system. Why? So that we can easily revert to a stable testable system.
   * Important: Do not forget to commit also the golden masters (files, database, etc)!

7. Check test behaviour and coverage
   * In this stage I tend to do two things:
     * Use a test coverage tool to see where the system tests touch the SUT
     * Start changing the SUT in order to see the golden master test go red.
     * If the test does not go red, I can understand that the code base is not covered by tests in that area and I should not touch it during the next stages, until I have a basic safety net. Always after this step I will revert to the previous commit, not matter how small the change to the SUT was.

8. If not enough behaviours are covered, go to 3
   * In the case we found during the last stage some behaviours that were not covered by the golden master test, we need to write some more tests with other inputs and outputs. We go on until all the visible behaviours needing to be covered by tests are covered.
