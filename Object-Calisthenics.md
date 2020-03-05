* TDD is not enough
* DRY is not enough.
* TDD will punish you if you don’t understand design
* If your tests are difficult to write your design is probably wrong

# 9 steps to better software design

* Only one level of indentation per method
* Don't use the ELSE keyword
* Wrap all primitives and strings (if it has behaviour or it’s an important domain concept)
* First class collections (wrap collections in classes, if it has behaviour or it’s an important domain concept)
* One dot per line (Do not write dog.Body.Tail.Wag() write dog.ExpressHapiness())
* Don't abbreviate
* Keep all entities small 
  * 10 files per package
  * 50 lines per class
  * 5 lines per method
2 arguments per method
* No classes with more than two instance variables
* No getters/setters/properties

## Use only one level of indentation per method.
Ever stare at a big old method wondering where to start?  A giant method lacks cohesiveness.  One guideline is to limit method length to 5 lines, but that kind of transition can be daunting if your code is littered with 500-line monsters.  Instead, try to ensure that each method does exactly one thing – one control structure, or one block of statements, per method.  If you’ve got nested control structures in a method, you’re working at multiple levels of abstraction, and that means you’re doing more than one thing.  
As you work with methods that do *exactly* one thing, expressed within classes doing exactly one thing, your code begins to change. As each unit in your application becomes smaller, your level of re-use will start to rise exponentially. It can be difficult to spot opportunities for reuse within a method that has five responsibilities and is implemented in 100 lines.   A three-line method that manages the state of a single object in a given context is usable in many different contexts. Use the Extract Method feature of your IDE to pull out behaviours until your methods only have one level of indentation.

## Don’t use the else keyword
Every programmer understands the if/else construct. It’s built into nearly every programming language, and simple conditional logic is easy for anyone to understand.  Nearly every programmer has seen a nasty nested conditional that’s impossible to follow, or a case statement that goes on for pages.  Even worse, it is all too easy to simply add another branch to an existing conditional rather than factoring to a better solution. Conditionals are also a frequent source of duplication. Object-oriented languages give us a powerful tool, polymorphism, for handling complex conditional cases.  Designs that use polymorphism can be easier to read and maintain, and express their intent more clearly.   But it’s not always easy to make the transition, especially when we have ELSE in our back pocket.   So as part of this exercise, you’re not allowed to use ELSE.  Try the Null Object pattern; it may help in some situations. There are other tools that can help you rid yourself of the else as well. See how many alternatives you can come up with.

## Wrap all primitives and strings
In C# int is a primitive, not a real object, so it obeys different rules than objects.  It is used with a syntax that isn’t object-oriented. More importantly, an int on its own is just a scalar, so it has no meaning.   When a method takes an int as a parameter, the method name needs to do all of the work of expressing the intent.  If the same method takes an Hour as a parameter, it’s much easier to see what’s going on.  Small objects like this can make programs more maintainable, since it isn’t possible to pass a Year to a method that takes an Hour parameter. With a primitive variable the compiler can’t help you write semantically correct programs. With an object, even a small one, you are giving both the compiler and the programmer additional info about what the value is and why it is being used.
Small objects like Hour or Money also give us an obvious place to put behavior that would otherwise have been littered around other classes. This becomes especially true when you apply the Rule X, and only the small object can access the value. 

## Use only one dot per line
Sometimes it’s hard to know which object should take responsibility for an activity.  If you start looking for lines of code with multiple dots, you’ll start to find many misplaced responsibilities.  If you’ve got more than one dot on any given line of code, the activity is happening in the wrong place.  Maybe your object is dealing with two other objects at once.  If this is the case, your object is a middleman; it knows too much about too many people.  Consider moving the activity into one of the other objects.
If all those dots are connected, your object is digging deeply into another object.  These multiple dots indicate that you’re violating encapsulation.  Try asking that object to do something for you, rather than poking around its insides.  A major part of encapsulation is not reaching across class boundaries into types that you shouldn’t know about. 
The Law of Demeter (“Only talk to your friends”) is a good place to start, but think about it this way:  You can play with your toys, toys that you make, and toys that someone gives you. You don’t ever, *ever* play with your toy’s toys.  

## Don’t abbreviate
It’s often tempting to abbreviate in the names of classes, methods, or variables.  Resist the temptation – abbreviations can be confusing, and they tend to hide larger problems.
Think about why you want to abbreviate.  Is it because you’re typing the same word over and over again?  If that’s the case, perhaps your method is used too heavily and you are missing opportunities to remove duplication.  Is it because your method names are getting long?  This might be a sign of a misplaced responsibility, or a missing class.

## Keep all entities small
This means no class over 50 lines and no package over 10 files.  Classes over 50 lines usually do more than one thing, which makes them harder to understand and harder to reuse.  50-line classes have the added benefit of being visible on one screen without scrolling, which makes them easier to grasp quickly.
What’s challenging about creating such small classes is that there are often groups of behaviors that make logical sense together.   This is where we need to leverage packages.  As your classes become smaller and have fewer responsibilities, and as you limit package size, you’ll start to see that packages represent clusters of related classes that work together to achieve a goal.  Packages, like classes, should be cohesive and have a purpose.  Keeping those packages small forces them to have a real identity.

## Don’t use any classes with more than two instance variables
Most classes should simply be responsible for handling a single state variable, but there are a few that will require two. Adding a new instance variable to a class immediately decreases the cohesion of that class. In general, while programming under these rules, you’ll find that there are two kinds of classes, those that maintain the state of a single instance variable, and those that coordinate two separate variables. In general, don’t mix the two kinds of responsibilities. 

## Use first-class collections
Application of this rule is simple: any class that contains a collection should contain no other member variables.   Each collection gets wrapped in its own class, so now behaviors related to the collection have a home.  You may find that filters become a part of this new class.   Also, your new class can handle activities like joining two groups together or applying a rule to each element of the group.   

## Don’t use any getters/setters/properties
Another way this rule is commonly stated is “Tell, don’t ask”. Tell-Don't-Ask is a principle that helps people remember that object-orientation is about bundling data with the functions that operate on that data. It reminds us that rather than asking an object for data and acting on that data, we should instead tell an object what to do. This encourages to move behaviour into an object to go with the data.

