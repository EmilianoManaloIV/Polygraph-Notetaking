---
NoteType: Annotations
NoteCreation: 2026-01-20
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
**Background Information In Regards To Python**
* Dynamically type, utilizes values
```python
#Python focuses on values not on types compared to C++
x = 10
x = "hello"
```
* Python is an extremely high level language and utilizes multiple datatypes that are complex.
* The libraries are vast, making development easy and supported; its free.
* C++ is **compiled**: its fast to execute, slow to develop
	* Compiled (Assembly Code)
	* Assembler (Machine Code)
	* Linker (Connects Other Machine Code)
	* Loader (Loads into memory)
	* Executable (Runs the code)
* Python is **interpreted:** development is fast, slow to execute
	* Each line is read at a time
* **Extensible:** allows the use of python in other programming languages.
* **OOP:** Object oriented language (encapsulation, polymorphism, etc.)
```bash
#Opens up Python prompt mode
C:\Users\%USER>py
#Opens up python on script mode
```
* Python uses indentation instead of curly braces
```python
x = 1
y = 2
if(x = y):
	print("X is equal to Y")
else:
	print("X is not equal to Y")
```
* Python has a built in IDE called IDLE which comes pre-packaged with the python application
* Printing is only required with IDE and compiling data
* Order Of Operation
	* Multiplication/Division
	* Addition/Subtraction
```python
#Addtiion
2 + 2
#Subtraction
2 - 2
#Division with float result
17/3
#Floor Division
17//3
#Modulus Operatior
17%3
#Power Operator
5**2
```
---
# Data Types
## Strings

```python
x = 'Hello'
print(type(x))
#str type clas
```
* All variables serve as a class of something class (string, int, float, etc.)
* Use a backlash character to characterize special characters "/" or utilize " " to encapsulate strings, or use "r" before the string.
* You can print multiple lines using three colon
* You can print forward and backward from an elements
```python
x = "hello"
#Access indicies forward
x[0]
x[1]
x[2]
x[3]
x[4]
#Access indicies backwards
x[-5]
x[-4]
x[-3]
x[-2]
x[-1]
```
* You can splice strings by utilizing from index x:index y 
```python
x[0:2] #will become "he", indicie 0 to 2 not included
x[0:] #Will include everything to the end
```
* You can also combine and multiple strings
```python
x[-2:] #Will display "lo"
```
* Indexing will cause errors, ranges inferences what it may be and either goes to the end or from the front
* There is also the increment operation where has a range, but increments within itself. Can work inversely with negative indexes
```python
x["from":"to":"incr"]
```
* There is several immutable types such as strings which can't be changed, they just create new variables and free old memory.
## Lists
* Lists can hold many different values separated by a comma
```python
someList = [1,4,8, True, "Some String"]
```
* You access it through indices
```python
someList[0] #Will display 1
someList[:3] #Will display 1,4, 8
```
* Lists are mutable by nature, thus doesn't follow the some constraint as strings.
```python
myList = [1,2,3]
myList[0] = 10
#Thus becomes [10,2,3]
#You can also use slicing
myList[0:2]
#What will result is [10,2]
```
* You can use append in python operations
```python
myList.append(8)
#Thus results in [10,2,3,8]
```
* You can clear lists using empty lists
```python
myList[2:5] = []
#Empties the list from index 2 incluse to 5 exclusive
```
* You can get the length of a list using .len(x)
```python
myList.len(x)
```
* If you slice more than your last index, it adds values
* You can nest types with lists
```python
x = [100,'h',[1,2]]
print(x[2])
#Get sub list from other lists
print(x[2][0])
#THis will return 1
```
