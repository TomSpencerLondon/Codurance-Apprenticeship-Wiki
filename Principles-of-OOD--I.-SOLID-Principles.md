What is object-oriented design? What is it all about? What are it's benefits? What are it's costs? It may seem silly to ask these questions in a day and age when virtually every software developer is using an object-oriented language of some kind. Yet the question is important because, it seems to me, that most of us use those languages without knowing why, and without knowing how to get the most benefit out of them.

OOD principles expose the dependency management aspects of OOD as opposed to the conceptualization and modeling aspects. This is not to say that OO is a poor tool for the conceptualization of the problem space, or that it is not a good venue for creating models. Certainly, many people get value out of these aspects of OO. The principles, however, focus very tightly on dependency management.

**Dependency Management** is an issue that most of us have faced. Whenever we bring up on our screens a nasty batch of tangled legacy code, we are experiencing the results of poor dependency management. Poor dependency management leads to code that is hard to change, fragile, and non-reusable. Indeed, I talk about several different design smells in the PPP book, all relating to dependency management. On the other hand, when dependencies are well managed, **the code remains flexible, robust, and reusable**. So dependency management, and therefore these principles, are at the *foundation of the -ilities that software developers desire*.

### SOLID Principles
---
The first five principles are **principles of class design**. They are:

[SRP	The Single Responsibility Principle](https://drive.google.com/file/d/0ByOwmqah_nuGNHEtcU5OekdDMkk/view)
 
>*A class should have one, and only one, reason to change.*

[OCP	The Open Closed Principle](https://drive.google.com/file/d/0BwhCYaYDn8EgN2M5MTkwM2EtNWFkZC00ZTI3LWFjZTUtNTFhZGZiYmUzODc1/view)

> *You should be able to extend a classes behaviour, without modifying it.*

[LSP	The Liskov Substitution Principle](https://drive.google.com/file/d/0BwhCYaYDn8EgNzAzZjA5ZmItNjU3NS00MzQ5LTkwYjMtMDJhNDU5ZTM0MTlh/view)

> *Derived classes must be substitutable for their base classes.*


[ISP	The Interface Segregation Principle](https://drive.google.com/file/d/0BwhCYaYDn8EgOTViYjJhYzMtMzYxMC00MzFjLWJjMzYtOGJiMDc5N2JkYmJi/view)

> *Make fine grained interfaces that are client specific.*


[DIP	The Dependency Inversion Principle](https://drive.google.com/file/d/0BwhCYaYDn8EgMjdlMWIzNGUtZTQ0NC00ZjQ5LTkwYzQtZjRhMDRlNTQ3ZGMz/view)
> *Depend on abstractions, not on concretions.*

###### Bibliographical Sources:

- Extract from http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod by Robert C. Martin

***
#### Repos with useful examples
* [Java examples explaining SOLID](https://github.com/upsd/solid)

