# IDD Apprentice Notes
Sandro gave the apprentices an overview of his thoughts on IDD. This was specifically aimed at people who have watched his talk and read the blog post. Below are our notes from the post-talk retrospective.

## When to use IDD
IDD is a design-tool like any other and therefore it will not be appropriate in all scenarios. We will enumerate a few key points
came up as a result of Sandro talking about IDD.

### Designing individually vs consistently
Within literature it is often noted that we as developers should strive for consistency, as not to surprise anyone. An
example of this might be if we are following DDD (Domain Driven Design):

Imagine an API with the following endpoint `/books`. The below articulates the various steps involved when a user
requests a particular book:

* Request comes in from user requesting a book
* Domain service is invoked, getting book from the repository
* Repository returns book

Now this is a perfectly sensible flow, one which flows from the `Domain Service` to the `Repository`.

If we had another feature to implement, we might decide that there is not enough logic in the service to warrant the
aforementioned flow, but everywhere else in our application utilises that flow.

So, we have ourselves a dilemma: be consistent or introduce inconsistency.

This is not an easy dilemma to solve (obviously), so it will need to be done one a team basis usually, to gather the
consensus on what is appropriate.

### Depth and intercommunication of a feature
If you have simple and shallow features you might not want to use IDD as the feature is not sufficiently complex enough.

However, if you find yourself in a similar situation to the previous section, you might want to decide whether it is
worth it to implement IDD for this feature, even if this means being inconsistent with the implementation of other
features.

### Should I use IDD on everything?
No, like all tools, use them wisely and where appropriate.

## Domain Driven Design Divergence AKA: how does IDD differ from DDD?
*  In IDD entities are treated as glorified data holders. Business logic is moved into services.
*  In IDD repositories are treated as second-class citizens and are not shared between bounded contexts (they cannot logically exist outside of their domain).
*  In IDD we focus on requirements leading to verbs (actions) first, and then only define the smallest amount of state (entities) needed to support these verbs. This is the opposite of DDD.
	* IDD: verbs lead to nouns (behaviour drives entity creation).
	* DDD: nouns are defined for verbs to use (entities are created and then behaviour is added to use these entities).
*  In IDD we speak more of "behaviour" than we do of "state". 
	* Data leads to object-oriented code.
	* Whereas behaviour leads to functional code.
*  Sandro says that IDD is "more prescriptive but more flexible than DDD".

## Some definitions around IDD
* "Domain Model" == "Model" - both are treated as the same conceptually and provide a view on the actual domain.
* "non-functional requirements" are better called "operational requirements" - Examples: Security, performance, scalability…lots of …-bilities).
* BookCollection vs BookRepository - organise and visualise relationships of entities, objects and behaviour in appropriately named packages / namespaces.
* Macro design allows micro design objects (sub-organisations) to communicate with each other - the way those are organised depends on their responsibilities.

## "Actions" in IDD
*  What we call an "application service" in DDD is called an "action" in IDD.
*  Actions handle flow control (higher level of abstraction of behaviour).
	* Domain services provide the more fine-grained, domain-specific behaviour used by actions.
	* Actions are defined by verbs (e.g. "AddBookToCollection"), domain services are described by nouns (e.g. "BookService").
*  Uncle Bob calls actions "use cases".

## DDD guidelines
* Have a screaming architecture
* Architecture is upfront - you cannot TDD it
* Macro design can be done with Outside-in
* Micro design can be done TDD
* Architecture is derived from business flows
* Learn to justify design and architecture decisions within the context
* Domain services cannot cross domain boundaries
* While execution, design and testing go in the same direction the layer of abstraction becomes more fine-grained
* Controllers expose and endpoint - keep them thin
* Actors can also be software/hardware
* Outside-in design - each behaviour exists to justify the needs of an actor or external need