## Guidelines	
* **Leave things better than you found them** (Boy scout rule)
* Never be more than 2 minutes away from checking in and going home
  * **Stay in the green** for as long as possible
  * Commit as often as possible
    * Allows you to work in small and safe increments
    * Allows easy rollbacks
* Arm yourself
  * Tests
    * Don’t change production code that is not covered by tests
    * If you need to add tests start from shortest to deepest branch
* Characterization tests (Late unit tests)
* Golden master tests/Approval based tests
* Model based tests
* Property based tests
  * Tools (Resharper, NCrunch, WebStorm)
    * Prefer IDE automated refactoring, minimize text editing.
  * Patterns, principles and code smells
    * Detect code smells and apply refactors
* Refactor to design patterns when appropriate
* Refactor to SOLID compliant design
* Use the Transformation Priority Premises table
  * Make code testable (Seams)
    * Identify needed code seam
    * Split code on seam
    * Make it testable
* Remove the 3 C’s
  * Clutter – Anything in your code that does not add value
    * Format the code
    * Delete dead code
    * Delete useless comments
    * Delete unnecessary code
  * Complexity
    * Rename bad names
    * Extract smaller methods from long methods
    * Return from methods as early as possible
    * Extract methods from deep conditionals
    * Extract constants from magic numbers and strings
    * Refine scope for improper variable scoping
    * Encapsulate where we find missing encapsulation
  * Cleverness – “If it’s simple and elegant, you wouldn’t refer to it as ‘clever’”
    * Make abbreviated code explicit 
    * Encapsulate cryptic code in methods
* Remove the 3 D’s
  * Duplication
  * Duplication
  * Duplication

## Links
* https://sourcemaking.com/refactoring/refactorings
## Videos
* https://www.youtube.com/watch?v=_NnElPO5BU0
* https://www.youtube.com/watch?v=WpKb1XqSiUs
* https://codurance.com/videos/2016-09-02-complex-refactoring-in-simple-steps-I/
* https://codurance.com/videos/2016-09-30-complex-refactoring-in-simple-steps-II/
* https://codurance.com/videos/2017-01-30-complex-refactoring-in-simple-steps-III/
* https://www.youtube.com/watch?v=aWiwDdx_rdo
## Books
* http://martinfowler.com/books/refactoring.html
* https://www.amazon.co.uk/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052