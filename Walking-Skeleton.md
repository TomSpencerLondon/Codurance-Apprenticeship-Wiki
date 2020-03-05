# Do you validate chosen architecture and technologies some time during definition?
  * If you don’t, why?
  * If you do, why?
  * If you do, when?
  * If you do, how?

# In a nutshell
“A Walking Skeleton is a tiny implementation of the system that performs a small end-to-end function. It need not use the final architecture, but it should link together the main architectural components. The architecture and the functionality can then evolve in parallel.”

Alistair Cockburn in “Crystal Clear : A Human Powered Methodology for Small Teams”

* A vertical slice through all the architecture layers
* Minimal implementation that proves the architecture through some end-to-end functionality
* From heavy architectural design to validating chosen architecture early on
* Production code, with production level quality and testing required.
* Automatically buildable
* Automatically deployable
* Automaticaly testable
* No functionality required
* Initial architecture

# Why to put the bones together?
* Get early feedback if chosen architecture and technology is suitable.
* Build quality in, by defining the main architectural structure early on and making it be consistent. (but at the same time, not doing whole bottom layers first).
* Allows to set up required development environments, such as CI systems, required load testing tools and so on.
* Improve knowledge and work estimations
* Give a jumpstart to development by setting the baseline onto which build. (skeleton where to hang the flesh, so to speak).
* Synchronizer
  * Walking skeleton can also work as synchronizer of the work if multiple teams are working on same product. The walking skeleton provides a basic structure and proven way to do things in product where independent teams can then build on.

# Exercise
The exercise for the day and probably the following day is to start doing the Shopping Basket kata with a walking skeleton.

The most basic thing to achieve for the walking skeleton will be this:
- Continuous Integration with the tool of your choice (Circle CI, TravisCI, Jenkins, ...)
- Web frontend with a single button that fetches from a datastore (of your choice) the items that can be added to the basket (two or three will be more than enough)
- Display on the screen the data fetched
- Deployment of the system into a machine (could be your own, AWS, Azure, ...)
- Be able to run and end to end tests that uses the button on the frontend and asserts that the information has come back and is being displayed (remember, it has to come back from the datastore)

After the above is completed, you can continue with the kata as usual