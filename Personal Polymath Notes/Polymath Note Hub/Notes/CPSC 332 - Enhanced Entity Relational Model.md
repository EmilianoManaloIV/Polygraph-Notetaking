---
NoteType: Theory
NoteCreation: 2026-02-23
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Definitions
* **Enhanced ER Model**: Hierarchical description of data 
* **Additional Concepts:** 
	* subclasses/super classes
	* specialization/generalization
	* categories
	* polymorphism & inheritance
	* object oriented types
___
## Superclass & Subclass
* An entity may contain more components that have their own dedicated relationships.
* Subclasses contain their own attributes from a superclass
* If a class/super class has multiple sub-classes
	* **Disjoint:** Cannot be more than one
	* **Overlapping:** Can be more than one
* **IS-A Relationship:** They are a direct subset of the class or superclass, inherits all properties of the parent class.
---
## Specialization
* Top-Down approach to assigning a super class. We define what is common across the board with other subclasses; detail what relates all the entities.
* **Local Attributes:** attributes not related to the superclass but related to the varying subclasses it is related to.
---
## Generalization
* Down-Up approach, has a bunch of entities that may be related to one another, then we can generalize the superclass with the information.
* **Predicates:** A check to determine if these attributes align with the sub-class you have.
* **Double Line:** Required subclasses
* **Single Line:** Optional subclasses