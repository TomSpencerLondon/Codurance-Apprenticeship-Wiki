* [Software architecture for developers](http://www.codingthearchitecture.com/presentations/oreillysaconlondon2017-software-architecture-for-developers)
* [Software architecture for developers video](https://www.safaribooksonline.com/library/view/oreilly-software-architecture/9781491985274/video315446.html)
* [Software architecture for developers books](https://drive.google.com/file/d/0B5FDdTcluIehZGtfMWhSV01FTTA/view?usp=sharing)

# Architecture vs design (From Simon Brown book)

Grady Booch has a well cited definition of the difference between architecture and design that really helps to answer this question. In On Design, he says that

_"As a noun, design is the named (although sometimes unnameable) structure or behavior of a system whose presence resolves or contributes to the resolution of a force or forces on that system. A design thus represents one point in a potential decision space."_

If you think about any problem that you’ve needed to solve, there are probably a hundred and one ways in which you could have solved it. Take your current software project for example. There are probably a number of different technologies, deployment platforms and design approaches that are also viable options for achieving the same goal. In designing your software system though, your team chose just one of the many points in the potential decision space.
Grady then goes on to say that...

All architecture is design but not all design is architecture.
This makes sense because creating a solution is essentially a design exercise. However, for some reason, there’s a distinction being made about not all design being “architecture”, which he clarifies with the following statement.

_"Architecture represents the significant design decisions that shape a system, where significance is measured by cost of change."_

Essentially, he’s saying that the significant decisions are “architecture” and that everything else is “design”. In the real world, the distinction between architecture and design isn’t as clear-cut, but this definition does provide us with a basis to think about what might be significant (i.e. “architectural”) in our own software systems. For example, this could include:

* The shape of the system (e.g.client-server,web-based,nativemobileclient,distributed, asynchronous, etc)
* The structure of the software system (e.g. components, layers, interactions, etc)
* The choice of technologies (i.e. programming language, deployment platform, etc)
* The choice of frameworks (e.g. web MVC framework, persistence/ORM framework,
etc)
* The choice of design approach/patterns (e.g. the approach to performance, scalability,
availability, etc)

The architectural decisions are those that you can’t reverse without some degree of effort. Or, put simply, they’re the things that you’d find hard to refactor in an afternoon.

## MVC
* [MVC XEROX PARC 1978-79](http://heim.ifi.uio.no/~trygver/themes/mvc/mvc-index.html)
* [A Cookbook for Using View-Controller User the ModelInterface Paradigm in Smalltalk-80](https://www.lri.fr/~mbl/ENS/FONDIHM/2013/papers/Krasner-JOOP88.pdf)
* [MVC, DELIVERY MECHANISM AND DOMAIN MODEL](https://codurance.com/2017/09/20/mvc-delievery-mechanism-dm/)
* [Understanding Model-View-Controller](https://blog.codinghorror.com/understanding-model-view-controller/)

# Architectural-styles

## Layered Architecture

![Architectural-styles](http://www.codingthearchitecture.com/images/2016/20160425-architectural-styles.png)

[Layers, hexagons, features and components](http://www.codingthearchitecture.com/2016/04/25/layers_hexagons_features_and_components.html)

### Layers

[Presentation Domain Data Layering](https://martinfowler.com/bliki/PresentationDomainDataLayering.html)
![](https://d3ansictanv2wj.cloudfront.net/sapr_0102-4d066ea1b22b2730ac3020954a2c944e.png)

### Hexagonal (ports & adapters)

![](https://8thlight.com/blog/assets/posts/2012-08-13-the-clean-architecture/CleanArchitecture.jpg)

### Feature packages

### Components

## Event-Driven Architecture

![](http://s.radar.oreilly.com/wp-files/2/2015/02/sapr_0203.jpg)

## Microkernel Architecture

![](https://www.safaribooksonline.com/library/view/software-architecture-patterns/9781491971437/assets/sapr_0301.png)

## Microservices Architecture Pattern

If you can’t build a modular monolith, what makes you think microservices is the answer?

![](http://microservices.io/i/Microservice_Architecture.png)