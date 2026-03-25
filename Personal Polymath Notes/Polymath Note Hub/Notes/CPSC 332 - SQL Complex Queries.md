---
NoteType: Theory
NoteCreation: 2026-03-23
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CSPC 332 - Introduction To Databases]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Comparison Involving NULL And Three Valued Logic 
* We often use logic tables to dictate how data between three attributes relate; such as one attribute can make the whole query false.
```SQL
TRUE = NULL
#Results in
null
```
---
## Nested Queries, Tuples, And Set/Multiset Comparison
* You can nest queries consecutively, such as:
```SQL
SELECT DISTINCT Name
FROM EMPLOYEE BACKUP
WHERE (Name) in (SELECT Name FROM EMPLOYEE_BACKUP WHERE CITY = 'San Jose')
```
---
## All, Any, And Some
* **ALL:** Must compare all attributes of data
* **ANY:** Check only Min And Max of dataset
---
## EXISTS and UNIQUE Functions
* **EXISTS:** Checks if a certain row exists.
---
## Inner Join
* **INNER JOIN:** Inner exclusive
* **LEFT JOIN:** Left inclusive
* **RIGHT JOIN:** Right inclusive
* **FULL OUTER JOIN:** Whole inclusive
---
## Rename Aggregation Function Results
* **SUM (COLLUM)**
* **MAX (COLLUM)**
* **MIN (COLLUM)**
* **AVERAGE (COLLUM)**
---
## Joins
```SQL
SELECT *
FROM  TABLE1, TABLE2
--I want to match one number in one table, from another
WHERE TABLE1.PRIMARYKEY = TABLE2.FOREIGNKEY

SELECT *
FROM TABLE1, TABLE2
--What key should I use? (PK->FK) INNER JOIN IS DEFAULT
JOIN TABLE1 ON TABLE1.PRIMARYKEY = TABLE2.FOREIGNKEY
--The result will be the same, but left and right join order matters
SELECT *
FROM TABLE1
LEFT JOIN TABLE2 ON TABLE1.PRIMARYKEY = TABLE2.FOREIGNKEY
--or
SELECT *
FROM TABLE1
RIGHT JOIN TABLE2 ON TABLE1.PRIMARYKEY = TABLE2.FOREIGNKEY
--MULTIWAY JOIN a wyay to nest joins, top-down inclusivity
SELECT *
FROM TABLE1, TABLE2, TABLE3
WHERE TABLE1.X = TABLE2.X = TABLE3.X
--You can chain the joins as a join results in a table
```
---
## Aggregate Functions
```SQL
--Used to summarize data and save it somewhere else
COUNT()
SUM() 
MAX()
MIN()
AVG()
--Group entries based on conditions, aggregate functions ignore null values
--Count works wierd when COUNT(*) gives every existing entrties, other functions respond with NULL count gives an integer.
GROUP BY CATEGORICALATTRIBUTE
--CAUTION: Doesn't know how to group, so specifiy SELECT, use collumn and aggregated functions
SELECT CATEGORICALATTRIBUTE, COUNT(*)
FROM TABLE1
GROUP BY CATEGORICALATTRIBUTE
```