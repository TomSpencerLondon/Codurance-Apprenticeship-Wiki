Event sourcing is a pattern that provides an alternative method of handling state within a system. Traditionally, state is stored in a database record. When we wish to change the state of the system, we change it directly. Therefore, if we were to take a look at the state of the system, we are looking at a snapshot of the system and cannot discern how we got there.

## Traditional
Let's take a look at an example. Say we deposit and withdraw money from a bank account, traditional systems would look something like the below:
```
We start from an empty account.
state = 0
(1) - Deposit £100
state = 100
(2) - Withdraw £50
state = 50
(3) - Deposit £10
state = 60
```

As previously mentioned, it is not obvious from querying the state how we got there, we just get a snapshot in time of the current state of someone's bank account.

## Event-sourced
So how would we do this in an event-sourced system? Well, I am glad you asked. If we look at the previous example in a traditional system, there was a very important part that was overlooked. In that example we cared about the _what_ (state is now £100), but we did not pay attention to the _why_ (deposit of £100 was made).

Let's show how the previous example would work with an event-sourced system.
```
Account "111" created
Account "111" made a deposit of £100
Account "111" made a withdrawal of £50
Account "111" made a deposit of £10
```

Now we can calculate the state (i.e. the balance) by playing all of these events to see how they affect the balance. This is advantageous for many reasons, such as the ability to see what is happening within a system (the _why_). Furthermore, if you wanted to decommission some of your infrastructure, you could recreate the state of the system as it was just by replaying the events.

### Snapshots
In an event-driven architecture, it might be time-consuming to recreate the state every time you want to query it. For example, if I want to get the current balance of someone's account, but I have to play one year's worth of events to do so, this is very expensive. Fortunately, this is where the concept of snapshots come in very handy.

Snapshots work by saving the state at a specified interval (i.e. at end of the day), decreasing the amount of events we have to compute to calculate the current state. In the example of a bank account, if we take a snapshot of a bank account every evening, when the customer queries their bank account the next day, we only have to play the events that have occurred that same day to calculate their balance.

#### Resources
* [Greg Young — A Decade of DDD, CQRS, Event Sourcing](https://www.youtube.com/watch?v=LDW0QWie21s)
* [The Many Meanings of Event-Driven Architecture • Martin Fowler](https://www.youtube.com/watch?v=STKCRSUsyP0)
* [Event Sourcing - Martin Fowler](https://martinfowler.com/eaaDev/EventSourcing.html)