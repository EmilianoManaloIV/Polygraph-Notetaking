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
* **Partial Key:** A key that can minimize some degree of ambiguity.
* 