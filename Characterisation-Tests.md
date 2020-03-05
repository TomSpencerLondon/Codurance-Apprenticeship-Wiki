Characterization test is a means to describe (characterize) the actual behaviour of an existing piece of software, and therefore protect existing behaviour of legacy code against unintended changes via automated testing. This term was coined by Michael Feathers.

Michael Feathers defines characterization tests as tests that characterize the actual behaviour of a piece of code. In other words, they don’t check what the code is supposed to do, as specification tests do, but what the code actually and currently does.

Having a set of characterization tests helps developers working with legacy code because they can run those tests after modifying their code and make sure that their modification did not cause any unintended or unwanted changes in functionality somewhere else.

1. Use a piece of code in a test harness.
2. Write an assertion that you know will fail.
3. Run the test and let the failure tell you what the actual behaviour is.
4. Change the test so that it expects the behaviour that the code actually produces.
5. Repeat.
