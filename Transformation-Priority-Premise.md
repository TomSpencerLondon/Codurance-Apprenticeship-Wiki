If we go back to how we evolve code in TDD, we have these methods:<br>
1. Fake it is where you just return the exact value you need. If your test expects a zero from a method, use a “return 0;” statement. Usually you use this when you cannot tell how to implement certain functionality, or your previous steps were too large and you cannot figure out what went wrong. Something that works is better than something that doesn’t work!
2. Use obvious implementation when you are pretty sure of the code you need to write, so write it and see if the test passes. The majority of the time you will use this method to move forward with TDD quickly.
3. Triangulation is where you want to generalize certain behaviour, but are not sure how to do it. So you start with fake it and add additional tests that force the code to be more generic along a certain dimension.

“Use obvious implementation” is ambiguous, what does “obvious implementation” mean? It may mean something for you and something else for another developer. The transformations on the following table are a way to clarify ambiguity the “obvious implementation”.

|#  | Transformation | Start code | End code
| --| -------------- | ---------- | --------
| 1 | {} -> nil | {} | [return] nil
| 2 | Nil -> constant | [return] nil | [return] “1”
| 3 | Constant -> constant+ | [return] “1” | [return] “1” + “2”
| 4 | Constant -> scalar | [return]  “1” + “2” | [return]  argument
| 5 | Statement -> statements | [return]  argument | [return] min(max(0, argument), 10) 
| 6 | Unconditional -> conditional | [return] argument | if(condition) [return] argument else [return] 0
| 7 | Scalar -> array | dog | [dog, cat]
| 8 | Array -> container | [dog, cat] | {dog=”DOG”, cat=”CAT”}
| 9 | Statement -> tail recursion | a + b | a + recursion
| 10 | If -> loop | if(condition) | loop(condition)
| 11 | Statement -> recursion | a + recursion | recursion
| 12 | Expression -> function | today – birth | CalculateBirthDate()
| 13 | Variable -> mutation | day | var Day = 10; Day = 11;
| 14 | Case/Switch		

Transformations on the top of the list should be preferred to those that are lower. It is better (or simpler) to change a constant into a variable than it is to add an if statement. So when making a test pass, you try to do so with transformations that are simpler (higher on the list) than those that are more complex.
<b>Please do not take this table literally</b>. This is a starting point. Adapt this table to your language and environment.
