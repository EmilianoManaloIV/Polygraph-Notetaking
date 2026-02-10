---
NoteType: Theory
NoteCreation: 2026-02-02
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
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
	* **Current State**: State of the database at present time; snapshot (Event)
	* **Valid State**: A state in which the constraints and structure is up to par (Correctness)
___
## Case Exercise
* Case 1: Initiation of schema no errors.
	* Is empty
	* Not initialized
	* Is Current
	* Is Valid
* Case 2: Schema defined, data loaded, no errors
	* Is not empty
	* Is initial
	* Is current
	* Is valid
* Case 3: Added new data to order, no errors
	* Is not empty
	* Is not initial
	* Is current
	* Is valid
* Case 4: Data has been changed and there was an error.
	* Version 1 
		* Is not emtpy
		* It not initialization
		* Is current
		* is valid
	* Version 2
		* Is not empty
		* Is not initialization
		* Is current
		* is not valid
___
## Three Schema Architecture
* **Self-Describing Nature**: The system often describes itself
* **Insulation Of Programs**: Keeping things separate to deal with segments of issues.
* **Support Of Multiple Views**: Letting multiple users utilize a database system
* **Internal Schema**: Physical data, indexing and low-level operations.
* **Conceptual Schema**: ER diagrams and logical design
* **External Schemas**: How a database is viewed in relation with users.
* **Mappings**: The process of how layers of the system interact with one another. Its the communication channels between each of the systems that the user doesn't implicitly see.
___
## Data Independence
* **Logical Data Independence:** We change the conceptual schema without having to change external application programs.
* **Physical Data Independence:** Can be changed how things are formatted without modifying any of the prior data.
* When a schema or lower level is changed, we only need to change the **mappings.**
___
## DBMS Language
* **DDL:** Change the schema of the database and doesn't touch the entries (MetaData)
	* **SDL:** Internal Schema
	* **VDL:** User view
* **DML:** Change the entries or data within the schema.
	* **SQL:** Non procedural data 
	* **PL/SQL:** How to get certain parts of data using data provided
___
## DBMS Languages DML
* **High Level or Non-Procedural Language**: I want a certain piece of data, I don't want to know how I got it.
* **Low Level Or Procedural Language**: Get every piece of data you specified, matters how I want to get it.
___
## DBMS Interfaces
* **Menu-Based (Often Web Based):** Utilize a user interface that fronts the queries you want.
* **Apps For Mobile Devices**: Built in programmed interacted and with limited menu options.
* **Forms Based**: A form that is created for a user that fills it out and then is saved into the database.
* **Graphics Based**: Displays a schema utilizing a built in query and menu system.
* **OTHER INTERFACES
	* Natural Language
	* Speech input/output
	* Keyword Based Search
	* Parametric 
* ****
## DBMS Component Modules: Group 1
* **Top Users:** Care about the table structure and schema of the system, doesn't care about the data associated with the schema
* **Bottom Users**: 
___
## DBMS Component Modules: Group 2
* **Casual Users:** Occasionally need access to the query system once and awhile
* **Query Compiler:** Complies the query given
* **Query Optimizer:** Dictates how to execute the commands to be the most efficient.
___
## **DBMS Component Modules: Group 3**
* **Application Programmer:** Writes programs that the database uses.
* **Precompile**: Extracts DML commands 
___
## DBMS Component Modules: Group 4
* Parametric users: Often interacts outside the scope of the database but often shovels data from one place to another.
___
## Database System Utilities
* There are tools to find what values are accessible and can be manipulated, and in the best efficient way.
___
## Centralized DBMS Architecture
* **Older Architecture:** Large mainframe computer that holds all the operations of the system, such as front-end and back-end systems in one large computer: mainframe.
___
## Client Server Architecture
* Accessing the data in a segmented client to server system. Where that network can route the user to what they need to access. The communication network handles alot of the data traffic in what the user needs to access.
___
## Two-Tier Client/Server Architecture
* There is a client that handles the UI and applications program, while the server can handle just the database. 
* A three-tier system includes one more tier that serves the database system and is the middle man between the application and server.
	* Extra Security
	* Efficiency
	* Scalability
___
## DBMS: Classification 2
* Number Of Users: Members within the same machine
* Number Of Sites: Querying the data over multiple sites