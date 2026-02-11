---
NoteType: Theory
NoteCreation: 2026-02-10
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Python Data Types
* Variables are classes
```Python
#Immutable numbers
int x = 3
float x = 3.0
complex x = 2 + 3j
#Immutable strings
string x = "123"
#Mutable list
list x = [1,2,3]
#Immutable list
tuple x = (1,2,'a')
#Mutable set
set x = {1,2,'a'}
#Dictionary that contains mutable and unmutable data
dictionary x = {'name':'joe','age':32}
```
___
## Looping Techniques
* You can loop through different methods

```Python
for x, y in dictionary.items():
	print(x,y)

for x, y in enumerate[someList]:
	print(x,y)
	
for x, y in zip[List_1, List_2]
	print(x,y)
```
___
## Nested Dictionaries
* You can nest dictionaries utilizing key based indexing
```Python
#Example of adding items from a dictionary into a list
for x, y in someDic.items():
	mylist.append(y['job'])
```
___
## Comparing Sequences
```Python
(1,2,3) < (1,2,4)
[1,2,3] < [1,2,4]
'ABC' < 'C' < 'Pascal' < 'Python'
(1, 2, 3, 4) < (1, 2, 4,3)
```
___
## More On Sets
```Python
#Each letter is an element
x = set("Hello There")
#The whole string is one element
y = {"Hello There"}
```