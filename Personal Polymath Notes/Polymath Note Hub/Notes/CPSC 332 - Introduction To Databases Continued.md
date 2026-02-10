---
NoteType: Theory
NoteCreation: 2026-01-28
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Data Model 
* There is certain **entities** in a data model or dataset such as:
	* **University**
		* Students
		* Professors
		* Classes
		* Department
* Students have to take classes, professors teach classes, classes depend on the department; these things are related with each other.
___
## Basic Definitions
* **Entity:** Thing or object that is represented in database
* **Attribute**: Properties that describes an entity
* **Mini-Word**: Part of the real world we want to store data about
* This is why **DBMS** is required, so that we can organize these things in an efficient and secure manner.
___
## Constructing University Database
* How do we store that data in a university setting and create a table?
	* Rows: Certain Student
	* Columns: Attribute 
* **Direct Reference:** Finding a relationship within the table itself (same student_id)
* **Indirect Reference**: Finding a relationship implicitly from one table to another (sutdent_num -> secition_identified -> crs_num)
* DB manipulation. how do we manipulate data once stored?
___
## Database Schema
* How do entities interact with each other? How do attributes relate to each other?
	* Database description
	* A Blueprint of the database
	* Determines what can be stored in the schema.
---
## Class Example
• Think about entities for a Bank database
• Identify basic attributes for those entities
- BANK DATABASE
- Employee
	- Name
	- Employee ID
	- Position
	- Email
- Customer
	- Name
	- Balance
	- PIN
	* History (Purchase, Withdrawal, Deposit)
	- Phone Number
	* SSN
	- Customer_ID
- Vault
	* Customer_ID
    - Lockbox_ID
    - Lockbox_code
    - Item Type (Legal Document, Precious Materials, Other)
    - Record
    
___
## Application Activities Against A Database
* Application interacts with the DBMS:
___
## Database Design
1. **Requirement specification**: what data are we storing? What are we going to ask for? What is the conceptual design? ER diagrams?
2. **Logical Design**: Using the ER model as an actual structure we can implement. Define the tables and define our constraints.
3. **Physical Design:** Actual creation of the database and outlines the actual relationships in the database
___
## Characteristics Of Database Approach
* **Self Describing Nature Of A DB System:** 
	* **Catalog**: Stores the descripting of particular data
	* **Description:** Metadata of the system
* **Data Abstraction:** How is data stored? What is its relationship between the upper and lower abstraction.
* **Support Of Multiple Views Of The Data**: Limit the access of the data based on roles or privileges.
* **Data Sharing**: Databases serve as a concurrent process where multiple users can access certain data.
___
## Database Users
* **Database Administers:** Manage the database and maintains its operations.
* **Database Designers:** Determines the actual architecture of the database.
* **End Users:** The users that utilize the database provided by both the designers and administrators.
	* **Casual:** Access the DB once and awhile
	* **Naive:** Access of certain data on a whim
* **System Analyst and Application Developers**
* **Actors Behind The Scene:** Low level development of the the database
___
## Hierarchical Model
* Most database systems are based on a natural Hierarchical Model; however most relationships are not tree based by nature.
___
## Network Model
* Connects within each other
___
## Relational Model
* Interrogability with many different components of data.