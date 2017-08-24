# Principles_Of_Software_Design
Six Principles Of Software Design

## I. Single Responsibility Principle (SRP)

### Purpose
* Reduce Class/Interface complexity, increase readibility, maintenability, extendability. Also reduce the risk of modifications.

### Core
* There should never be more than ONE REASON for a class(or interface) to CHANGE

### Description
* Class A has responsibility R1, R2, when R1 or R2 needs to be modified, there could impact each others.

### Practical Experience
* Responsibilities and reasons of modification are hard to measure in practical projects
* Interface must be undertaken with SRP, and Class should only be modified by ONE REASON.

## II. Liskov Substitution Principle (LSP)

### Purpose
* Increase program robustnesss when adding more derived class. 

### Core
* Definition: o1 is object of type S, o2 is object of type T, all programs P defined in terms of T, the behaviour of P is unchanged when o1 is subtituted for o2, then S is subtype of T.
* Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it.

### Understanding
* Derived classes must implement the methods of base classes completely. 
* Call base class or interace in different class rather than call derived class or concrete method.
* Derived class may have its own methods or properties.
* Arguments in Methods of derived class should have equal/larger scales over those of base class, so as to call methods of 
base class avoiding logic chaos. 

### Practical Experience
* Try not to inject extra properties or methods into the derived different from the base

## III. Dependence Inversion Principle (DIP)

### Purpose
* Decoupling classes, reduce the risk of parallel coding

### Core
* High level modules should not depend upon low level modules.Both should depend upon abstractions.
* Abstractions should not depend upon details.
* Details should depend on abstractions.

### Understanding
* Interface-Oriented Design

### Practical experience
* Each class should have interface or abstract class, or both.
* Variables should be interace or abstract except utils' class or clonable class
* Any classes must not be inherited from concrete class.
* Base class should not be overrided by derived
* Interface is resposible for defining public properties and methods, and declaring dependent relationships with other objects.
  Abstract class is responsible for implementation of common features and logic.

## IV. Interface Segregation Principle (ISP)
### Purpose
* High cohesion, reduce interactions(public methods) between modules, less code, less cost 

### Core
* The dependancy of one class to another one should depend on the smallest possible interface.

### Understanding
* Fullfil SRP first, and then minimise the number of methods in interface (Atomic Interface).
* Interfaces need to be highly cohesive, i.e. reduce the number of public methods that interact with other class
* Customised Interface/methods for specific class, so as to have minimised dependencies. i.e. Hide unused methods, and only expose those methods that classes may call.  
* Sufficient granularity of interface design is expected. Small one may have more flexibility but complexity, leading to more difficulty in development and high cost in mantenance.

### Practical Experience
* One interface only serves submodule or business logic
* Squeeze the number of public methods in interfaces, and try to avoid fat interfaces
* Try to alter polluted intefaces, if high risky, use adapter patterns to fix it. ?????
* Domain experience is important

## V. Law of Demeter (LoD) / Least Knowledge Principle (LKP)

### Purpose
* Decoupling classes

### Core
* One object is supposed to have least knowledge against other objects.

### Understanding
* Only talk to your immediate friends (try do build direct dependeny like A->B->C, rather than A->B, A->C, B->C), methods in class try not to create objects not declared within that class.
* Friends have distance, try not announce too many public methods or non static properties, instead use as many private, protected as you could to have more high cohesion.

### Practical Experience
* Applying Lod may produce quite a few transit classes, leading to complexity of program and high maintenance. There should be 
  a balance between clear structure and high cohesion, less coupling. 
  
## VI. Open Close Principle (OCP)

### Purpose

### Core
* Software entities like classes, modules and functions should be open for extension but closed for modifications.

### Understanding
* Modification Type: 
  1) Logic/algorithm, modify the method straight away as long as other modules/classes follow the rules
  2) Sub-module, low level modules' modifications may cause more modifications in the high levels'. Adding derived class to avoid developing risk is a good option.
  3) User Interface, may apply modifications/extentions depending on scenarios
  
* Modifications' impact to testing
* OCP increases logic granularity and code reusability
* OCP increases maintenability

### Practical Experience
#### Abstract Constraint
* Apply extention constraint for abstract classs/interface, avoid public method of derived not existing in base/interface
* Use abstract/interface type as argument, not concrete class
* Keep abstract stable/unchanged

#### Metadata controls behaviour of modules
* Metadata is the data that describes environment and data. i.e. configuration variables.

#### Build project regulations/conventions

#### Encapsulate modifications
* Encapsulate similar modifications into one interface or abstract class
* Encapsulate different modifications into different interfaces or abstract classes

# Conclusion
* SRP: Classs should have single responsibility
* LSP: Don't destroy the mechanism of inheritance
* DIP: Interface Oriented Programming
* ISP: Simplify/minimise interface
* LoD: Reduce coupling between classes
* OCP: Open to extensions, Close to modifications


 


  

