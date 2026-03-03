---
NoteType: Theory
NoteCreation: 2026-03-02
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Relational Model Concepts
* Traditionally, models often uses stringent designed data structures to access data.
* However, relational systems like SQL makes it easier to access and collect data and not having to focus on the underlying systems in how that data is stored.
* A **relation** if often a **table**
* **Rows** are **tuples** and **columns** are **attributes**
	* These are considered sets, so there is no order or duplication of objects within the database.
* **Domain:** Set of atomic values that are able to accompany a certain attribute type. Often known as **dom(A)**
* **Relation Key:** Identifies a certain row (Key, Artificial Key, Surrogate Key)
___
## Domain Constraints
* First step into specific a certain name for the attribute, specific what kind of datatype, and then specify a format.
* Some datatypes, depending on the storage method, can be detrimental depending on the use-case.
---
## Definitions
* **Schema:** Structure that describes the rows and columns of the dataset.
* **Relational Degrees:** How many attributes are for each row.
---
**Tuple**
* Represents an ordered amount of data for a certain character often represented by $< >$
* You can switch order in SQL
___
## Relation State
* **Cartesian Product:** Two domains of attributes with multiple domains that are defined in the set.
---
## Ordering
* Since they are tuples, any point in the row will change, hence if you change an attribute position it will move that entire row; row order doesn't matter.
---
## Characteristics Of Relations
* Tuples in SQL don't have any order, because the attributes are schema bound like a dictionary.
---
## Values And NULLS In The Tuples
* Values need to adhere to the rule defined in the schema of the database.
* If a student doesn't fulfill a certain data, is considered NULL data.
---
## Relational Model Notation
$$R(A_{1},A_{2},\dots,A_{n})=\text{Schema}$$
$$R=\text{Relation State}$$
$$A_{1},A_{2},\dots,A_{n}=Attributes$$
___
## Relational Model Constraints
* **Inherent Or Implicit Constraint:** Set issues, atomic value constraints
* **Schema Based Constraint:** We set the foreign key and cardinality rules
* **Semantic Or Application Based Rule:** A determined rule we setup that violates a certain attribute.
* **Constraints:**
	* Key Constraints
	* Entity Integrity Constraints
	* Referential Integrity Constraints.
----
## Key Constraints
* Tuples cannot have the same values of each other.
* **SuperKey:** Any attribute that identifies a row or entry absolutely.
---
## Candidate Key
* We often have a **primary key** that is utilized in most cases, however there is other protentional keys, known as a **candidate key**.
* 