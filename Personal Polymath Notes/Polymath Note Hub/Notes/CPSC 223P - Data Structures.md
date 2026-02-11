---
NoteType: Theory
NoteCreation: 2026-02-03
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## More On Lists
* Lists are treated as classes thus have:
	* Methods
	```python
	list.append(x)
	list.extend(iterable)
	list.insert(I,x)
	list.remove(x)
	list.pop()
	list.clear()
	list.index(x[, start[, end]])
	list.count(x)
	list.sort(*,key=None, revere=False)
	list.reverse()
	list.copy()
	```
* You can use pop and push just like in stacks with lists
---
## Tuple
* Consists of multiple different type of values to be held in one variable, they are **immutable**
```python
#Create a tuple
t = value, value, value
#You can nest tubles
y = t, (1,2,3,4,5)
```
* Comparing between a list and a tuple
```python
#Empty list
i = []
#List containing item
i = ['a']
#Empty tuple
i = ()
#Tuple containing one item
i = ('a',)
```
___
## Tuples Packing And Unpacking
* You can unpack tuples if they follow the same amount of variables within the tuple
```python
someTuple = (59, "Sweet", 'a')
x, y, z = someTuple
```
___
## Sets
* Unordered and don't have any duplicates
```python
#A string
mystr = 'abc'
#A list
myList = ['a', 'b', 'c']
#A tuple
myTuple = ('a', 'b', 'c')
#A set
mySet = {'a', 'b', 'c'}
#To make an empty set
mySet = set()
```
___
## Dictionaries
* Its a set of key value pairs, best for database systems, can store and retrieve data.
```python
#Create a dictionary
x = {44:"Ainge", 54:"Manalo", 86:"Burthum"}
```