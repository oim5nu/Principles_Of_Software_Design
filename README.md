# Principles_Of_Software_Design
Six Principles Of Software Design

## Single Responsibility Principle (SRP)

### Core
* There should never be more than ONE REASON for a class(or interface) to CHANGE

### Description
* Class A has responsibility R1, R2, when R1 or R2 needs to be modified, there could impact each others.

### Purpose
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
* Derived classes must implement the methods of base classes completely. 
* Call base class or interace in different class rather than call derived class or concrete method.
* Derived class may have its own methods or properties.
* Arguments in Methods of derived class should have equal/larger scales over those of base class, so as to call methods of 
base class avoiding logic chaos. 

### Purpose
* Increase program robustnesss when adding more derived class. 

### Practical Experience
* Try not to inject extra properties or methods into the derived different from the base

## Dependence Inversion Principle (DIP)

### Core
* High leve modules should not depend upon low level modules.Both should depend upon abstractions.
* Abstractions should not depend upon details.
* Details should depend on abstractions.

### Understanding
* Interface-Oriented Design

### Purpose
* Decoupling classes, reduce the risk of parallel coding

### Practical experience
* Each class should have interface or abstract class, or both.
* Variables should be interace or abstract except utils' class or clonable class
* Any classes must not be inherited from concrete class.
* Base class should not be overrided by derived
* Interface is resposible for defining public properties and methods, and declaring dependent relationships with other objects.
  Abstract class is responsible for implementation of common features and logic.


