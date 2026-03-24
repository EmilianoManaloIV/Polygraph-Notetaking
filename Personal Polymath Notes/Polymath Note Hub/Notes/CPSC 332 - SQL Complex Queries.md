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
* *