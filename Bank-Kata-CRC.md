## Kata
In this session, we will do an OO design for a known kata, using paper and pencil only.
* The objective is to define a design for the first story of a new product we will be launching soon. 
* We will be creating a design using CRC cards, following OO design principles such as SOLID, DRY, YAGNI, Tell Don’t Ask, etc.
* The product is a personal savings ATM machine like this:
  * For the first release 
    * We will disregard the card reader and user authentication, safe, money counting.
    * We will implement the Deposit, Withdraw and Print Statement operations.

We have the following GTW definition for our first user story:<br>

Given a kid makes a deposit of 10 on 10-01-2012<br>
And a deposit of 20 on 13-01-2012<br>
And a withdrawal of 5 on 14-01-2012<br>
When they print their bank statement<br>

Then they would see:<br>
date              || credit || debit || balance<br>
14/01/2012 ||             || 5.00  || 25.00<br>
13/01/2012 || 20.00  ||           || 30.00<br>
10/01/2012 || 10.00  ||           || 10.00<br>

## Tips
* When you create the cards try to tell a story of each operation using the cards
* Don't jump from operation to operation try to finish one before starting another
* Try to spot any missing cards in between cards, if you describe an operation and mention something not represented by a card you may want to add a card to represent that missing abstraction
* Test your design, look for SOLID violations, OO principles violations, Code smells.
* Look for external concepts leaking into the internals of your design
* Design outside in to avoid creating abstractions that are not serving a client