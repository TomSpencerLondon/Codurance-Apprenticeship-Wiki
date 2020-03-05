Individual [CRC Cards](http://www.extremeprogramming.org/rules/crccards.html) are used to represent objects. The class of the object can be written at the top of the card, responsibilities listed down the left side, collaborating classes are listed to the right of each responsibility.

Use Class, Responsibilities, and Collaboration (CRC) Cards to design the system as a team. The biggest value of CRC cards is to allow people to break away from the procedural mode of thought and more fully appreciate object technology. CRC Cards allow entire project teams to contribute to the design. The more people who can help design the system the greater the number of good ideas incorporated.

CRC Steps
* Step 1. Decide to use CRC cards and choose an coherent set of use cases
  * Decide to work with CRC cards as opposed to or in conjunction with object interaction diagrams and object type diagrams.
  * Select a set of use cases which look as though they will touch a related set of object types. These provide the scenarios for the group to walk through.
* Step 2. Put a card on the table
  * Put a first card onto the table to represent the external actor who triggers the use case.
  * Put a second card on the table. This is the card to whom the first card will send its initial message.
  * Alternatively, put cards onto the table for all the known, relevant object types, and label the cards with their main responsibilities.
* Step 3. Walk through the scenario, naming cards and responsibilities
  * Walk through the handling of a scenario of the use case, pointing to or picking up the cards, naming their responsibilities and how they handle and delegate each request.
  * In a brainstorming session, add new cards as new functions are needed, or reallocate the responsibilities of the cards already on the table. It is not always necessary to name both the object type and the responsibility at the moment the card is put onto the table, as long as they are both written before the end.
* Step 4. Vary the situations, to stress test the cards
  * At any time during the walkthrough, you may vary the assumptions on the use case, to see if that causes a shift in the handling. With a good design, the handling is the same, but with the addition of a future object, or the change to at most one card.
  * If it is decided a new object is needed to create a more stable design, add a new card, with the needed responsibility put onto it.
  * Not all the cards on the table need be used; some may drift out to the sides if they are not used much. The cards that are needed at the end are those that get put into the design.
* Step 5. Add cards, push cards to the side, to let the design evolve
  * CRC cards permit several design alternatives to sit on the table at the same time. An unpopular initial design may turn out to be a popular later design, or perhaps the final design is a small alteration of an initially rejected design.
  * Do not throw cards away, but push them to the side, in case it turns out later they are useful.
* Step 6. Write down the key responsibility decisions and interactions
  * Often, the design turns around a few key decisions about the allocation of responsibilities. Write these down.
  * It is not useful to draw interaction diagrams for all the scenarios considered, but it is very useful to draw a representative few.
