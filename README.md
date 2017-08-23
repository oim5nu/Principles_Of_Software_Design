# Principles_Of_Software_Design
Six Principles Of Software Design

## Single Responsibility Principle (SRP)

### Core
* There should never be more than ONE REASON for a class(or interface) to CHANGE

### Description
* Class A has responsibility R1, R2, when R1 or R2 needs to be modified, there could impact each others.

### Pros
* Reduce Class/Interface complexity, increase readibility, maintenability, extendability. Also reduce the risk of modifications.

### Practical Experience
* Responsibilities and reasons of modification are hard to measure in practical projects
* Interface must be undertaken with SRP, and Class should only be modified by ONE REASON.

## Liskov Substitution Principle (LSP)

### Core
* Definition: o1 is object of type S, o2 is object of type T, all programs P defined in terms of T, the behaviour of P is unchanged when o1 
  is subtituted for o2, then S is subtype of T.
* Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it.

### Understanding
* Objects of derived classes could be replaced by objects of base classes without causing any anomalies.

### Pros
* Reduce repeatable work for creating class
* Increase reusability of code
* Increase extendability
* Increase products/projects openness

### cons
