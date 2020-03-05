# Week 5 - Macro Design (DDD/IDD)

Exit Criteria → “Be comfortable with macro design”

Objectives:
  * Architectures: MVC, N tier Layers, Hexagonal, Clean. When to apply it
  * Single page application (SPA)
  * REST
  * Sequence Diagrams (UML)
  * DDD (building blocks)

Previous/secondary goals:
  * Understand Interaction driven design
-----
#### Learning Resources
[Macro design concepts (slides)](https://docs.google.com/presentation/d/1mMQY1XPMFHx8xS62Adu4W7TVuhqloyXBx8kM_YtqYFE/edit#slide=id.p)
###### Interaction Driven Design
* [IDD slides](https://drive.google.com/drive/u/0/folders/1DNmrZexzl49c90CcWhjKDnUokHo6Od0l) by Sandro Mancuso
* [IDD talk](https://vimeo.com/128596005) by Sandro Mancuso
* [IDD blog post](https://codurance.com/2017/12/08/introducing-idd/) by Sandro Mancuso
* [IDD Apprentice Notes](https://github.com/codurance/apprenticeship/wiki/IDD-Apprentice-Notes)
###### Domain Driven Design
* [DDD Basics](http://dddcommunity.org/learning-ddd/what_is_ddd/)
* [Event Storming](https://github.com/codurance/apprenticeship/wiki/Event-Storming)
* [Event Storming Workshop Cheat Sheet](https://github.com/wwerner/event-storming-cheatsheet)
* [Event Sourcing](https://github.com/codurance/apprenticeship/wiki/Event-Sourcing)
* [Aggregates, Repositories, Domain Events and Bounded Contexts](https://drive.google.com/open?id=1ApuqE0d1_FjqEqh3dMgLlmT_6Kd_P4NkYPS-pe_5w5s)
* [Ubiquitous Language, Entities, Factories and Anti Corruption Layer](https://docs.google.com/presentation/d/122t1MG_ZU6raaf_hWRlbR_zZnmGMIIjWUNHC-qN-TUE/edit?usp=sharing)
* [Model, Value Objects, Services](https://github.com/codurance/apprenticeship/wiki/Model,-Value-Objects,-Services)
* [Domain Driven Design Quickly](https://www.infoq.com/minibooks/domain-driven-design-quickly)
* [Notes taken while reading Domain Driven Design Quickly](https://docs.google.com/document/d/1miN7yXHMc8M8QXLY_p306CFPgb1iqhVQWWyjOr6XcJM/edit?usp=sharing)
###### Architectural Styles
* [Layered](https://docs.google.com/presentation/d/19jAD2mUJtgdjOadhJrourjGogVfU4pdspg3-2Rkx9Y4/edit?usp=sharing)
* [Event-driven](https://drive.google.com/open?id=1UcCsqcUd1Q0WzF2Zhva71vXtcNk0-2UUn83qhJoVc1c)
* [Microkernel](https://drive.google.com/open?id=1OUOWSWHJUmFh4zM6AHtPvdZZ0fQVBHc2BfTd-5YsYNo)
* [Model-View-Controller](https://docs.google.com/presentation/d/1M-c4nmxIL7wI5n3-TJRAarlkF5dSMy8G9SAm16QSA50/edit?usp=sharing)
* [Microservices](https://docs.google.com/presentation/d/1sdgy-TG3cFBeq8BWGPXYztKaSSFQSE6c-Mb7Ddu8D7o/edit?usp=sharing)
###### Hexagonal Architecture
* [Main article](https://softwarecampament.wordpress.com/portsadapters/) , by Alistair Cockburn. (cached)
* [Hexagonal Architecture](http://pradeeploganathan.com/architecture/hexagonal-architecture/) by Pradeep Loganathan.

----

Note: this schedule should not be followed. Just an idea of the amount of time for each activity.

## Day 1: MVC / Layers / DDD

| Start | Duration | Description        
| ------| -------- | -----------
| 09:00 | 90 m     | Introduction to macro design concepts [MVC / Layers / DDD](https://github.com/codurance/apprenticeship/wiki/Macro-Design-resources)
| 10.30 | 15 m     | Break
| 10:45 | 15 m     | Introduction to DDD
| 11:00 | 60 m .   | Extreme learning: Building blocks
| 12:00 | 60 m     | Lunch 
| 13:00 | 60 m     | Presentations and discussions
| 14:00 | 30 m     | Extreme learning: Bounded context
| 14:30 | 30 m     | Presentations and discussions
| 15:00 | 15 m     | Break
| 15:15 | 45 m     | Extreme learning: Strategic side of DDD
| 16:30 | 30 m     | Presentations and discussions

## Day 2: DDD Modeling

| Start | Duration | Description        
| ------| -------- | -----------
| 09:00 | 90 m     | DDD Modeling [Ciccio Pasticcio food ltd](https://github.com/codurance/apprenticeship/wiki/DDD-Ciccio-Pasticcio-food-ltd)
| 10.30 | 15 m     | Break
| 10:45 | 75 m     | DDD Modeling [Ciccio Pasticcio food ltd](https://github.com/codurance/apprenticeship/wiki/DDD-Ciccio-Pasticcio-food-ltd)
| 12:00 | 60 m     | Lunch 
| 13:00 | 90 m     | DDD Modeling [Ciccio Pasticcio food ltd](https://github.com/codurance/apprenticeship/wiki/DDD-Ciccio-Pasticcio-food-ltd)
| 15:00 | 15 m     | Break
| 15:15 | 75 m     | DDD Modeling [Ciccio Pasticcio food ltd](https://github.com/codurance/apprenticeship/wiki/DDD-Ciccio-Pasticcio-food-ltd)

Alternative exercise - modelling code from examples:
(https://github.com/codurance/apprenticeship/wiki/DDD-Exercise_Acme-Library)

## Day 3: Interaction Driven Design

| Start | Duration | Description        
| ------| -------- | -----------
| 09:00 | 90 m     | IDD introduction / presentation (Sandro presenting or watching video)
| 10.30 | 15 m     | Break
| 10:45 | 75 m     | Exercise: create project skeleton
| 12:00 | 60 m     | Lunch 
| 13:00 | 90 m     | Exercise: create project skeleton (continuation)
| 15:00 | 15 m     | Break
| 15:15 | 75 m     | Presentation

## Day 4: Sequence diagrams

| Start | Duration | Description        
| ------| -------- | -----------
| 09:00 | 90 m     | Create a sequence diagram of the main features of the project done on the day before
| 10.30 | 15 m     | Break
| 10:45 | 75 m     | Create a sequence diagram of the main features of the project done on the day before
| 12:00 | 60 m     | Lunch 
| 13:00 | 90 m     | Create a sequence diagram of the main features of the project done on the day before
| 15:00 | 15 m     | Break
| 15:15 | 75 m     | Create a sequence diagram of the main features of the project done on the day before

## Day 5: Outside-In TDD on the skeleton project

| Start | Duration | Description        
| ------| -------- | -----------
| 09:00 | 90 m     | Outside-In TDD on the skeleton project
| 10.30 | 15 m     | Break
| 10:45 | 75 m     | Outside-In TDD on the skeleton project
| 12:00 | 60 m     | Lunch 
| 13:00 | 90 m     | Outside-In TDD on the skeleton project
| 15:00 | 15 m     | Break
| 15:15 | 75 m     | Outside-In TDD on the skeleton project
