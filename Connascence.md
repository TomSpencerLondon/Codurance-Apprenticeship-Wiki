## A Flexible Metric
Connascence is a metric, and like all metrics is an imperfect measure. However, connascence takes a more holistic approach, where each instance of connascence in a codebase must be considered on three separate axes:

* **Strength**. Stronger connascences are harder to discover, or harder to refactor.

* **Degree**. An entity that is connascent with thousands of other entities is likely to be a larger issue than one that is connascent with only a few.

* **Locality**. Connascent elements that are close together in a codebase are better than ones that are far apart.

The three properties of Strength, Degree, and Locality give the programmer all the tools they need in order to make informed decisions about when they will permit certain types of coupling, and when the code ought to be refactored.

### A Vocabulary for Coupling
Arguably one of the most important benefits of connascence is that it gives developers a vocabulary to talk about different types of coupling. Connascence codifies what many experienced engineers have learned by trial and error: Having a common set of nouns to refer to different types of coupling allows us to share that experience more easily.

### Strength
![](https://www.codesai.com/assets/connascence-o-meter--md5--1f3dc254184c12f1fc87559ef4bfe373.png)

### Degree
The degree of a piece of connascence is related to the size of its impact. Does the coupling in question affect 2 entities, or 200?

### Locality
The locality of an instance of connascence is how close the two entities are to each other. Code that is close together (in the same module, class, or function) should typically have more, and higher forms of connascence than code that is far apart (in separate modules, or even codebases). Many of the stronger forms of connascence that can be devastating to the readability and maintainability of a codebase when they appear far apart are innocuous when close together.

Locality matters! Stronger connascences are more acceptible within a module. Weaker connascences should be used between entities that are far apart (in separate modules or even codebases).

## Resources
[Connasence IO](http://connascence.io/)

[About connascence](https://www.codesai.com/2017/01/about-connascence#nota7)