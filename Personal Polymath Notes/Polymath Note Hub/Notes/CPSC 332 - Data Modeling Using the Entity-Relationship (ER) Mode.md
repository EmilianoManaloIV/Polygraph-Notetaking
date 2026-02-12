---
NoteType: Annotations
NoteCreation: 2026-02-09
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Definitions
* **Entity-Relationship Model:** High level conceptual data
* **ER Diagrams:** Diagrammatic notation that isn't really associated with the UML diagram system.
* **UML Diagram**: A standardized way to describe a system
___
## Conceptual Design
* What is being stored? What values and attributes are associated with what entity?
___
## Logical Design
* You will need to associate "keys" with multiple different tables, there is a "division" and association of a relationship.
---
## Entity Relationship Model
* **E:** Known as an entity which contains a certain amount of attributes
* **A:** An attribute that describes an entity and is often a value
___
## Attributes
* **Simple:** Have a singular atomic model; data that cannot be partitioned or "broken" up. (EX. age)
* **Composite:** Breaking up the base data can give significant meaning to the broken up parts. (EX. full name) It also may be hierarchical.
* **Multivalued:** Holds multiple data that can have some significant association with the entity.
___
## Entity Types And Key Attributes
* **Entity Type:** Entities with the same basic attributes
* **Key Attribute:** Each entity has a unique value and could be possibly composite, which makes things easier to partition.
___
## Entity Set
* An entity can have multiple keys
* Multiple entitles that have shared keys, becomes an entity set!
___
## Attribute: Value Set
* Just like some programming languages, we can specify certain data types in the data set.
___
## Weak Entity Type
* **Partial Key:** A key that can minimize some degree of ambiguity, but still can contain duplicates.
___
## Exam 1 Guide
* Use printed or handwritten notes, only use lockdown browser before anything else.
* 40 Minutes
* 25 Questions
___
## Relationship
* Defines set of associations with a certain amount of entities.
	* **Cardinality:** Amount of max relationships 1:N, N:M, N:1
	* **Participation:** Amount of minimum relationships (-,=)
![[Entity Diagram.svg]]
___
## Cardinality Ratio
* Details the ratio between a relationship such one department can have many employees, but an employee can only have one department.
* The ratio describes the amount of entities within a given relationship.
* A:B = x:y
* A can have y B's
* B can have x A's
* Details with what is at-most; MAX
___
## Recursive Relationships
* These are relationships that doesn't just interact with one entity, but can interact with multiple entities in various ways.
___
## Constraints In Participation
* Is this relationship guaranteed or is it optional?
* Such as you don't have to have a dependent as an employee, but a dependent must have an employee.
___
## Ternary Relationship
* There can be more than two entities related in a relationship, thus you need to create a representation of the relationship between three entities.
___
## Structural Constraint: Alternative
* You can use ( , ) format to define the maximum and minimum; combination of cardinality and participation.
