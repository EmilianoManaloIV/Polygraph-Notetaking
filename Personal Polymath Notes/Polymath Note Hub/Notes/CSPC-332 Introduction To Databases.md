---
NoteType: Annotations
NoteCreation: 2026-01-26
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Exam & Project Important Data
* Exam Information:
	* Exam 1: 1, 2, 3
	* Exam 2: 4, 5, 6
	* Technically not cumulative, but the chapters build off each other, similar to mathematical lesson plans.
* Projects
	* Part A: 1-6
	* Part B: 7
---
## Database And Database Users
* **Data:** Known facts that can be recorded or cataloged.
	* Student **Table:**
	* Student is smart (optionaire data)

| student_id | gpa | award        |
| ---------- | --- | ------------ |
| 123456     | 4.0 | ...,....,... |
* **Database**: Collection of related idea, think about the relationship between an objects their components.
* **Data model:** Details how that data is structures and how is it stored? Blueprint of how data is retrieved, added, or changed.
* **Database Management System:** Software that lets us create data, query data, etc. The liaison between the data model and the application.
---
## Where Do We See It?
* Social media platforms, public universities, e-commerce, etc.
* A way to store, display, and manipulate data at a large scale.
---
## Application
* **Traditional:** Textual or numeric by nature, often built off of relationships.
* **Non-Traditional:** Images, posts, tweets, more complicated objects.
---
## Simplified Database Systems Environment
* Three is there primary components:
	* **Application Program**
	* **DBMS System**
	* **Retrieve From Server/Storage**
* **Query:** What data you want
* **Transaction:** Tells what operation should be executed; multiple operations such as querying.
* **DBMS:** System that determined how to access or change data.
* The user doesn't do the programming, its the engineers job to turn user action to queries.
---
## Read Only Vs Update Transaction
1. Show me my grades - Read Only
2. Register for a class - Update Transaction
3. Check bank balance - Read Only
4. Transfer $100 - Update Transaction
5. Look up product price - Read only.
---
## Data Redundancy
* **Data Redundancy**: Storing data in multiple times.
	* May be inconsistent
	* May cause higher hardware use
	
**Student Table**

| student_id | name | intructor_id |
| ---------- | ---- | ------------ |
| 1          | Alex | 1            |
| 2          | Mary | 2            |
| 3          | //   |              |
| //         | //   |              |
**Instructor Table**

| instructor_id | name |
| ------------- | ---- |
| 1             | Noah |
| 2             | Day  |
**Count Table**

| instructor_id | cnt |
| ------------- | --- |
| 1             | 2   |
| 2             | 1   |

* There is a relationship between tables which can have:
	* inconsistencies: this is what must use for a **DBMS**
___
## DBMS Purpose
* Defines the database, what we are storing, how we are storing it, conditions that it fulfills and operations it must do.
* Helps us create the database.
* Allows us to manipulate the database.
* Lets us share the database
---
## Denormalization
* Data placed closely together to avoid inconsistency: **denormalization**
	* Introduces controlled redundancy, which increases resources use.
---
## Enforcing Integrity Constraints (DBMS Advantage)
* Defines certain rules automatically which can avoid errors or unintentional manipulation.
* **Domain Constraint:** Prevents invalid values when stored.
* **Key (Uniqueness) Constraint:** Each student entity needs to have a unique "student_number"
* **Entity Integrity Constraint:** Can't have a null value
* **Referral Integrity Constraint:** Solidifies a relationship between several entities and tables without dependency errors.
---
1. A student record has no student ID.- Entity integrity constraint
2. Two students share the same student ID. - Key Constraint
3. A grade of ‘Z’ is entered. - Domain Constraint
4. A student is enrolled in a course that doesn’t exist. - Referral Integrity Constraint