---
NoteType: Theory
NoteCreation: 2026-03-09
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## What Is SQL
* **Structured Query Language:** built based on the relational model, but they shouldn't be exactly related with each others. An opensource universal standard this is used everywhere.
* We will be covering data definitions, datatypes, constraints, retrieval, INSERT, DELETE, UPDATE and additional features of SQL.
---
## Comprehensive DBMS
* Used both as a **DDL** and **DML** and details how these systems interact with each other.
	* **DDL:** Database structure
	* **DML:** How the database is accessed
* Controls who manipulates, queries, or removes data. SQL can be imbedded directly with other programming languages.
---
## Data Definition And Datatypes
```SQL
--This command creates data--
CREATE
---Example of DML Statement---
--Load and Retrieval--
SELECT
--Chanes Data/Record/Row--
INSERT
DELETE
UPDATE
```
---
## Schema And Catalog Concepts In SQL
* Schema's work differently than what is traditionally in related databases. You created schemas as an object you can access or manipulate; is permanent.
```SQL
--CREATE SCHEMA--
CREATE SCHEMA "SCHEMANAME" AUTHORIZATION "WHOHASAUTHORITY"
```
---
## Create Table Command
* How do we create a table in databases? You need to provide name, attributes and their types, and stored as a file in the database.
```SQL
--CREATE A TABLE--
CREATE TABLE "SCHEMA.TABLENAME"
CREATE TABLE "TABLENAME"
```
* Base relation tuples stored as a file in the DBMS. Attributes are ordered, but rows are not ordered within the relation.
```SQL
--Inserts Values Into Attributes Exclusively--
INSERT INTO "TABLE" "(ATTRIBUTE1, ATTRIBUTE2, ...)" VALUES(VALUE1, VALUE2, ...)
--INserts Vales Based On Order
INSERT INTO "TABLE" VALUES(VALUE1, VALUE2, ...)
```
* **A view** is a non-existent file, the database reflect the most current values and is considered a snapshot of the current database.
---
## Attribute Datatypes
* **Numerical Data Types:** 
	* **Whole Numbers:** INTEGER, INT (4 Bytes), SMALLINT (2 Bytes), 
	* **Decimal Numbers:** FLOAT, REAL, DOUBLE PRECISION
* **Character String Data Types:** 
	* **Fixed Characters:** CHAR(n), CHARACTER(n)
	* **Varying Character Size:** VARCHAR{n}, CHAR VARYING(n), CHARACTER VARYING(n)
* **Boolean Data Types:** True Or False
* **Date Datatype:**
* **Times Data Type:**
---
## More About CREATE TABLE
* You need to be mindful in the order of tables since there can be circular logic. There is also methods to counter this by referencing tables that are not yet created.
---
## Specifying Attribute Constraints
```SQL
--Default Value of an asttribute--
DEFAULT <value>
--CHECK Clause--
"ATTRIBUTE" "ATTRIBUTETYPE" NOT NULL CHECK (DomainConstraint)
```
---
## Giving Names To Constraints
* You can name constraints to organize varying constraint conditions.
---
## Basic Retrieval Queries
* Duplicates are impossible mathematically within a table, however, SQL is a multiset. Can be a set if you use ```DISTINCT keyword.
* Basic form of a select
```SQL
--List of attributes you want to get: COLLUMNS--
SELECT <ATTRIBUTE> 
--Select the table you want it from: TABLE--
FROM <TABLE LIST>
--A condition to get a certain piece of data: CERTAIN DATA--
WHERE <CONDITION>
```
* Uses regular comparison operators except for equal which is $\text{=} \neq\text{==}$
* [DBS Playground](https://www.db-fiddle.com/)
---
## Practical Implementation
```SQL
--Selects collumns of a given table: ATTRIBUTES, multiple attributess seperated by comma
SELECT *
--Select the table where the collumns are located--
FROM SELECTEDTABLE
--Select only certain data with a certain condition
WHERE SOMEATTRIBUTE SOMECONDITION
```
* You don't select the relationship, we will have the Cartesian product of the tables.
```SQL
--Connecting keys manually--
WHERE TABLE1.PRIMARYKEY = TABLE2.FOREIGNKEY
```
* You can discovery relationships within the same table using self-joining, multiplies at a Cartesian product
```SQL
SELECT *
FROM TABLE1 AS A, TABLE1 AS B
WHERE A.PRIMARYKEY = B.FOREIGNKEY
```
* You can minimize duplication of certain values, you can use **DISTINCT** In select
	* **UNION ALL:** Adds two unique sets
	* **EXCEPT ALL:** Leave out values
	* **INTERSECT ALL:** Keep values that are similar
* You can check similarity
	* LIKE "__0__2910"
* Can order things using **ORDER BY**
* 