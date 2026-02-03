---
NoteType: Theory
NoteCreation: 2026-02-02
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[Landing Page]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Review
* Entities with attributes
	* Columns And Rows
	* Relational Tables
* Database Management Systems: Manages how tables are operated on
	* To Read? To Query?
	* To write?
	* Or both?
* **Data Schema:**
	* How the data is structured
	* What are the attributes?
	* What are the constraints?
	* What the rules does it follow?
* **Data Consistency:**
	* How to control consistency and how does:
		* Controlled Redundancy
		* Constrolled Consistency
		* Caching data
	* The DBMS gives us rules and regulations how to make the database more efficient and stable.
___
## Definitions
* **Data Abstraction**: Hiding and showing data that we need to focus on.
	* **Program data independence**: 
	* **Program operation dependence**: Shouldn't cause issues to the database systems
* **Data Model**: Describes the concepts and operations of how a database operates.
* **Data Model Structures And Constraints**
___
## Definitions
* **Entity:** A real world object of some degree
* **Attribute:** Describes the entity in some important way.
* **Relationship**: How do entities relate and in what way?
* EX.
**Library System**

| Book | Book_ID |
| ---- | ------- |
|      |         |

| member_id | name |
| --------- | ---- |
|           |      |

| load_id | date_given |
| ------- | ---------- |
|         |            |

* An Entity can be an attribute, or vice-versa, or related through a table
* **Data Model**: Represents the structure, operations, and rules of the database
---
## Data Model Categories
* **Conceptual**: How do we perceive data? Human friendly or computer friendly.
* **Physical:** How is data stored in the computer?
* **Representational**: Provide useful data to the user up-front.
* **Self-Describing**: Certain parts of the data showcases its structure intrictly.
___
## Database Schema
* Schema describes the structure/table?
* How does the data connect with one another?
* Separate tables to prevent error or system disability.
___
## Database State
* Tells us what is the status of the data at a certain time.
* Has all the data in the database
	* **Empty State**: Initiated new data schema (Content)
	* **Initial State**: State of the database after its loaded with data (Time)
	* **Current State**: State of the database at present time
	* **Valid State**: A state in which the constraints and structure is up to par.