## Duplicated Code
_Identical or very similar code exists in more than one location or duplicated knowledge._<br>
DRY violation.<br>
Cohesion violation.

## Long Method
_Methods should do only one thing._<br>
SRP violation.
“Functions should do one thing. Should do it well.<br>
Should do it only”.<br>
One level of abstraction. No more than 5 to 15 lines.<br>
Cohesion violation.

## Large Class
_Classes should have only one responsibility._<br>
No more than 50 lines per class.<br>
Possible SRP violation.<br>
Cohesion violation.

## Long Parameter List
Ideal: 0 niladic<br>
Ok: 1 monadic<br>
Acceptable: 2 dyadic<br>
Debatable: 3 triadic avoid<br>
Special justification: 3+ polyadic.<br>
Coupling violation.<br> 
Connascence of position.

## Divergent Change
_One class is commonly changed in different ways for different reasons._<br>
OCP, SRP violation.<br>
God class.<br>
Cohesion violation.	

## Shotgun Surgery
_Opposite of Divergent change. One change, forces lots of little changes in different classes._<br>
DRY violation.<br>
Coupling violation.

## Feature Envy
_A class that uses methods or properties of another class excessively._<br>
Tell, don’t ask violation.<br>
Cohesion and Coupling violation.

## Data Clumps
_Same data items together in lots of places._<br>
Special case of duplicated code.
DRY violation.<br>
Cohesion violation.

## Primitive Obsession
_Don't use primitive types as substitutes for classes. If the data type is sufficiently complex, use a class to represent it._<br>
Coupling violation.<br>
Connascence of meaning.

## Switch Statements
_Can lead to same switch statement scattered about a program in different places._<br>
Can lead to Dry violation.<br>
Could be Cohesion violation.<br>

## Parallel Inheritance Hierarchies
_Special case of shotgun surgery. Creating a subclass of one class, forces subclass of another._

## Data Class
_Classes that have fields, properties, and nothing else._<br>
_Anaemic classes that contain no behaviour._ 
Special case of lazy class.<br>
Cohesion violation.

## Speculative Generality
_YAGNI violation or only users of method or class are test cases._<br>
Cohesion violation.

## Temporary Field
_Class contains an instance variable set only in certain circumstances._<br>
Cohesion violation.

## Message Chains
_Too many dots:_ Dog.Body.Tail.Wag()<br>
Should be:<br>
Dog.ExpressHappiness()<br>
Law of Demeter violation.<br>
Coupling violation.

## Middle Man
_If a class is delegating all its work, cut out the middleman._<br>
Beware classes that are wrappers over other classes or existing functionality.<br>
Special case of lazy class.

## Inappropriate Intimacy
_A class that has dependencies on implementation details of another class._<br>
Special case of feature envy.<br>
Cohesion violation.

## Alternative Classes with Different Interfaces
_If two classes are similar on the inside, but different on the outside, perhaps they can be modified to share a common interface._

## Incomplete Library Class
_Adding missing functionality by not changing library can lead to functionality implemented in odd places._

## Lazy Class
_A class that does too little._<br>
May be acting only as middle man or a data class or can be caused by speculative generality.

## Refused Bequest
_Throw not implemented._
Usually means the hierarchy is wrong.<br>
LSP violation.

## Comments
_Make effort to create code that expresses intent instead of comments._

## Dead Code
_Code that has no references to it, commented code._