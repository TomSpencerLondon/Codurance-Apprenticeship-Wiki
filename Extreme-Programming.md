The goal of Extreme Programming (XP) is outstanding software development. Software can be developed at lower cost, with fewer defects, with higher productivity, and with much higher return on investment. The same teams that are struggling today can achieve these results by careful attention to and refinement of how they work, by pushing ordinary development practices to the extreme.

# What is XP?

Extreme Programming (XP) **is about social change**. It is about letting go of habits and patterns that were adaptive in the past but now get in the way of us doing our best work. It is about giving up the defenses that protect us but interfere with our productivity. **It may leave us feeling exposed**

It is about being open about what we are capable of doing and then doing it. [...] It is about getting past our adolescent surety that "I know better than everyone else and all I need is to be left alone to be the greatest". It is about the process of becoming more of our best selves and in the process our best as developers. And it is about writing great code that is really good for business.

**Good relationships lead to good business.** [...] You need both technique and good relationships to be successful. [...] Prepare for success. Do your best and then deal with de consequences.

XP is a **style of software development** focusing on the **excellent application of programming techniques, clear communication, and teamwork** which allows us to accomplish things we previously could not even imagine.

## Continuous improvement
XP is a **path of improvement to excellence** for people coming together to develop software. XP includes:

1. A philosophy of software development based on the **values** of:
- Communication
- Feedback
- Simplicity
- Courage
- Respect

2. A body of **practices** proven useful in improving software development. They are chosen as expressions of the values.

3. A set of complementary **principles**, intellectual techniques for translating the values into practice.

4. A **community** that shares these values and many of the same practices.

It is distinguished from other methodologies by:

1. Its short development cycles, resulting in early concrete, and continuing feedback.

2. Its incremental planning approach, [...] that is expected to evolve through the life of the project.

3. Its ability to flexibly schedule the implementation of functionality, responding to changing business needs.

4. Its reliance on automated tests written by programmers, customers, and testers to monitor the progress of development, to allow the system to evolve, and to catch defects early.

5. Its reliance on oral communication, tests and source code to communicate system structure and intent.

6. It's reliance on an evolutionary design process that lasts as long as the system lasts.

7. Its reliance on the close collaboration of actively engaged individuals with ordinary talent.

8. It's reliance on practices that work with both the short-term instincts of the team members and the long-term interests of the project.

## The Paradigm

This is the paradigm for XP: Stay aware. Adapt. Change

> *Everything in software changes. The requirements change. The design changes. The business changes. The technology changes. The team changes. The team members change. **The problem isn't change because change is going to happen**; the problem rather, is our **inability to cope with change***

# Values, Principles and Practices

## Values 

The values of XP are universal, the same values as you work are applied on your life.

Values are the roots of the things we like and don't like in a situation.

Making values explicit is important because without values, practices quickly become rote, activities performed for their own sake but lacking any purpose or direction. 

These are the 5 values where XP focuses on improving: 

• **Communication**: Everyone on a team works jointly at every stage of the project.

• **Simplicity**: Developers strive to write simple code bringing more value to a product, as it saves time and efforts.

• **Feedback**: Team members deliver software frequently, get feedback about it, and improve a product according to the new requirements.

• **Respect**: Every person assigned to a project contributes to a common goal.

• **Courage**: Programmers objectively evaluate their own results without making excuses and are always ready to respond to changes.

## Principles

Most researchers denote **5 XP principles** as:

• **Rapid feedback**: Team members understand the given feedback and react to it right away.

• **Assumed simplicity**: Developers need to focus on the job that is important at the moment and follow YAGNI (You Ain’t Gonna Need It) and DRY (Don’t Repeat Yourself) principles.

• **Incremental changes**: Small changes made to a product step by step work better than big ones made at once.

• **Embracing change**: If a client thinks a product needs to be changed, programmers should support this decision and plan how to implement new requirements.

• **Quality work**: A team that works well, makes a valuable product and feels proud of it.

## Practices

When it comes to the quality of our software and making sure we are building the thing right, XP practices provide us with many ways to shorten the feedback loop. 

> The practices are a vector from where you are to where you can be with XP

It's possible to write good software with only a few practices, but XP works best with every piece in play.

These practices are commonly divided in 12, derived from the best practices of software engineering, we will grouping them in three groups.

### Coding Practices

The primary practices are useful independet of what else you are doing. They each can give you immediate improvement. You can start safely with any of them.


<u>***Code and Design Simply***</u>

> to produce software that’s easy to change

XP has three rules that govern simplicity: 

- Do the Simplest Thing That Could Possibly Work
- You Aren’t Gonna Need It
- and Once and Only Once*

Simple designs are easier to understand and to explain. Simple code is easier to test, maintain, and change.

**A simple design requires**:

- Good communication between developers and the customer, to identify the necessary features.

- Confidence, for the whole team to believe that you can adapt to change.

- The rare ability to recognize simplicity, or at least the willingness to keep trying.

<u>***Code refactoring</u>***

> to find the code’s optimal design.

Refactor your code regularly. After making a test pass, refactor the new code. After finishing a task, take a few moments to do a little house cleaning. Eliminate repetition. Break long methods and functions into smaller ones. Clarify variable and method names. Make the most of the opportunity to simplify the code and its design. Leave the code easier to understand and easier to modify.

Refactoring should simplify the overall design. Refactoring should change only the structure of code, leaving its external behavior untouched.

Ideally, a test that passes before a refactoring will also pass after that refactoring *without modification*. By relying on tests, you can simplify your code while retaining its necessary behavior.

**Refactoring requires**:

- Discipline, to find and to perform potential refactorings whenever possible.

- Comprehensive tests, to prove that the behavior of the code remains the same across refactorings.

- Collective code ownership, to enable you to refactor any part of the system that needs it.

- Coding standards, to govern the types of changes that the team expects.
  

<u>***Coding Standards</u>***


> to communicate ideas clearly through code.

Feature requests and charts will come and go, but the project lives or dies with the software. As long as someone maintains it, it lives.

Coding standards are conventions. They’re almost conversational techniques. They describe your best practices.

The best coding standards are guidelines, not commandments. They represent your project’s shared values, both symbolically and in reality. When necessary, they can be suspended. Reasonable and thoughtful developers know when rules can be broken.


**Coding standards require**:

- Developer teamwork, to set aside habits and preferences in favor of clear communication.

- Occasional review, to ensure that the existing standards communicate the shared values and intent of the code sufficiently.

- Pair programming, to help ensure that all new code adheres to the standards.


<u>***Develop a common vocabulary</u>***

> to communicate ideas about code clearly

Develop a common vocabulary to describe your project as it evolves. This vocabulary will likely come from a *metaphor* with well-understood relationships

Your vocabulary should describe each major component in the project. Keep it expressive and approachable because you’ll share it with the customer

**A shared vocabulary requires**:

- Simple design, to be described simply


### Developer practices

These practices reinforce good programming habits by guiding less experienced developers and keeping everyone on track.

<u>***Test-Driven Development</u>***

> to prove that the code works as it should.


Adopt test-driven development. Write a test that fails. Write code to pass the test. Check that the test passes. Refactor the code. Automate your tests. Keep them passing. Use failing tests to prompt you to write code. This cycle produces a natural rhythm of rapid feedback.

**Test-driven development requires**:

- Positive peer pressure, for developers to overcome the initial shock of test-driven development and to continue testing even when it seems difficult.

- Clear customer communication, to identify what the acceptance tests should cover. 


<u>***Pair programming</u>***

Program in pairs. When you start a task, ask another developer to work with you. Pairs generally work together for just one task, perhaps an entire afternoon, and then form other pairs with new partners. This spreads the knowledge of the system throughout the whole team.

Pairs reinforce good programming habits, with each partner exerting positive peer pressure on the other. Having a partner present reduces the temptation to skip testing, refactoring, or simplifying. Two brains on a task and two sets of eyes on the code produce fewer bugs, leading to cleaner code that fits the team coding standards. Spend a little more time on communication while you code. It will produce higher quality code that needs much less debugging.

**Pair programming requires**

- Facilities designed for pairing, to allow two programmers to sit and work together at one workstation.

- Developers willing to try pair programming.

- Managers willing to try pair programming, to produce better code with less overall effort.

- Coding standards, to allow developers to code with the same voice. 

<u>***Code ownership</u>***

> to spread the responsibility for the code to the whole team.

Adopt collective code ownership, where the entire codebase belongs to the whole team. Any developer is free to change any piece of the code as needed to complete a task. This allows you to move at your natural pace. Write the appropriate tests, write the necessary code, and run the full test suite to verify that your changes make sense.

**Collective code ownership requires**:

- Coding standards, so that the style of the code is consistent across developers. 
  
- Comprehensive testing, to ensure that risky changes can be detected and fixed rapidly. 

- Frequent integration, so that all pairs have access to the freshest code. 

- A shared vocabulary, to explain the place of each piece of the code within the whole system. 
  
<u>***Continuous integration</u>***

> to reduce the impact of adding new features.

Continual integration keeps everyone on the same page. By keeping tasks small, pairs can integrate their work after a few minutes or a few hours—everyone can work on the freshest possible working code. Staying close to the main source tree avoids the pain of playing catch-up after weeks or months away. Code cleanups and other enhancements made by one pair are only an integration away for everyone else.

Integration must be simple. Just run the test suites, merge, and commit the code. It must be quick and painless. Automate as much as you can. You’ll be integrating often. The rest of the team should not have to wait for you to finish. Having short tasks helps by producing fewer changes to merge.

**Integrating continually requires**:

- A collective source code repository, to hold the master source.

- Comprehensive testing, to judge the health of the system. 

- A quick test suite, to speed up integrations.

- The planning game, to divide the work into small pieces. 
  
- Working at a sustainable pace, to know how much time to invest in a task in a day. 


### Business Practices

Building a successful software project requires far more than just coding. A beautiful, elegant, and comprehensively tested project is useless unless it meets the customer’s actual needs.

<u>***Add a customer to the team</u>***

> to address business concerns accurately and directly

Add a customer to the team. XP calls this the *Whole Team.* The customer provides a business perspective as an actual user of the software. Regular, reliable, and rapid communication between technical and business people improves confidence, reduces guesswork and misunderstandings, and produces the desired results more quickly.

The customer should work closely with you. Ideally, she will work alongside the developers. She writes story cards and is always available to answer questions. The closer the customer is to the rest of the team, the better. Make it as easy as possible to go directly to the source of business knowledge—if possible, make it easier to turn around to ask the customer a question than to assume the answer.

It’s better to deliver software that fills the customer’s most important needs on time than to delay the software to add less important features. Allow the customer to decide what is most valuable.


**A customer in the team requires**:

- An initial investment in the project, to convince the customer to join the team.

- A common vocabulary, to improve communication between the customer and the developers.


<u>***Play the Planning Game</u>***

> to schedule the most important work


Play the planning game to produce and to refine your schedule. XP uses the phrase Planning Game to describe the give and take process of deciding which features to implement in what order. The goal of the planning game is to maximize the value of features produced.

XP schedules are based around the iteration. An iteration is a snapshot of the entire development cycle. The customer requests features. The team plans them. They’re implemented,tested, and delivered. The whole process takes one to four weeks before it starts again.

**The planning game requires**:

- An active customer, to write story cards and to set priorities. 

- Mutual respect, for customers to believe developer estimates and for developers to believe customer stories and priorities.

<u>***Release Regularly</u>***

> to return the customer’s investment often.

Release regularly. At the end of each iteration, after the software passes all acceptance tests, release the software to the customer. Keep iterations short—from one to four weeks long. Keep your feedback loops short. Allow regular, small adjustments.

A short release cycle quickly starts to return on the customer’s investment. With every release, the customer receives her most valuable features. You can respond to her feedback rapidly—scheduling and implementing her changes in the next iteration. She’ll receive a steady flow of features, adapted to her actual current needs.

Regular releases deliver bug fixes well. While critical bug fixes can be delivered immediately, less severe bugs can be scheduled as normal stories and included in the next appropriate iteration. 

**Regular releases require**: 

- Simple design, to keep iterations short and manageable.

- Comprehensive testing, to ensure that all of the code works. 

- Continual integration, to keep the code in a releasable state. 

- The planning game, to set priorities for the current iteration.

<u>***Work at a Sustainable Pace</u>***

> to be productive

Work at a sustainable pace. Everyone has a natural level of productivity. It will vary from person to person, but everyone has a limited amount of physical, mental, and creative energy. Every hour of work costs energy. Sleep, family activities, and recreation replenish your reserves. Pushing your limits is counterproductive.

Your velocity must be accurate to schedule the next iteration. Overcommitting due to overtime exacerbates the problem—you’re promising more than you could actually deliver in the previous iteration.



---

Bibliographical sources:

[Extreme Programming Xplained, 2nd editions, Kent Beck](https://drive.google.com/file/d/1OCc2clum7wfxjBFUdpYuvXc2J9n11AvS/view)

[Extreme Programming Pocket Guide](http://shop.oreilly.com/product/9780596004859.do)

[Extreme Programming: Values, Principles, and Practices](https://www.altexsoft.com/blog/business/extreme-programming-values-principles-and-practices/)