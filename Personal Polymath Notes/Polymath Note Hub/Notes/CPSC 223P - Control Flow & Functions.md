---
NoteType: Theory
NoteCreation: 2026-01-27
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Break Statement
* Exits and "breaks" out of a current loop
```python
#Create a range of values from 0,1,2,3,4,5
for i in range(5):
	#Check if the range value is three and exit
	if(i==3):
		break
	#Print the value
	print(i)
```
* "else" can be used within a loop as a way to see if the loop was not broken
```python
#Create a range of values from 0,1,2,3,4,5
for i in range(5):
	#Check if the range value is three and exit
	if(i==3):
		break
	#Print the value
	print(i)
else:
	print("Doesn't execute")
```
___
## Continue Statement
* Just continues the next iteration of the loop it is within
```python 
#For range of numbers from 2,3,4,etc.
for num in range(2,10):
	#Check if divisible by two
	if num % 2 == 0:
		#Print if found even numbers
		print("Found an even number", num)
		continue
	#Found an odd number
	print("Found an odd number", num)
```
* You can use "pass" as placeholder code
```python
while True;
	pass
```
___
## Some Examples Of Break And Continue Statement
* Place a break statement in the for loop so that it prints 0 to 10
```python
for i in range(100):
	#Break out if its "11"
	if(i == 11):
		break
	#Print current number
	print(i)
```
---
## Match Statement
* Similar to a switch case:
```python
def http_error(status):
	match status:
		case 400:
			return "Bad Request"
		case 404:
			return "Not Found"
		case 418:
			return "I'm A Teapot"
		case _:
			return "Im a default value"
```
___
## Defining Functions
* You can create functions the same way using "def" and providing arguments. 
	* You must create functions first before calling
	* Variables within functions are not global (symbol table separation)
```python
#Create the function
def fib(n):
	#This is a docstring!
	"""Print A Fibonocaii Series up to n"""
	#Fibonacci algorithim
	a, b = 0, 1
	while a < n:
		print(a, end-"")
		a, b - b, a+b
	print()
```
* Example of scope operation
	* Automatically finds dependencies and assumes variable references, inside scope -> outward scope
```python
#Define the varialbe
x = 0
#Create the function
def f1():
	x = 1
	#Print the value within the funciton
	print(x)
#Call the function
f1()
#Call the print function
print(x)
```
---
## Passing Arguments To Functions
* View this as mutable or unmmutable of an argument
* **Call By Object Reference**
* **Call By Assignment**
```python
#Showcase a mutable proejct
#Make a vector of 1 and 2
x = [1,2]
#Create the function that adds three and prints
def f1(x):
	x.append(3)
	print(x)
#Print in global space
print(x)
#Utilize the function
f1(1)
```
___
## Return Statement
* Returns the value back from the function
	* Functions will return 'NONE' by default
```python
def f1(x):
	y = x + 1
	return(y)
```
---
## Default Argument Values
* You can create a default value when defining a function in the argument ("x = "world"")
	* This can operate with multiple arguments
```python
#Create an optional parameter
def greet(x = "world")
	print("Hello", x)
greet("bob")
#This will result in "Hello Bob"
greet()
#This will result in "Hello World"
```
___
## In Keyword
* You can use in to compare a value to a list
```python
#Create a list
x = [1,2,3]
#Have a value
y = 1
#Compare and do something 
if y in x:
	print("Found ID")
```
___
## Function Keyword Arguments
* You can use keywords to signal certain arguments
	* Keyword arguments can't be followed by positional arguments
	* Can't double define at the same argument
	* Can't pass arguments that aren't part of the function
```python
#Create a function
def add(x,y)
	return(x+y)
#Can pass positionally
add(3,4)
#Or by keyword (Order doesn't matter)
add(x=3, y=4)
add(y=4,x=3)
```
* You can have varying argument lengths using "*"
```python
#Define loose amount of arguments
def my_function(*args):
	print(args)
	#Very argument do this
	for i in range(len(args))
		#Print the argumnet
		print(args[i])
```
* You can restrict arguments using "/" for position and "*" for keyword only
```python
#Example of restricting argumnets
def f(pos1, post2, /, pos_or_kwd, *, kwd1, kwd2)
```
* When to use this methodology!
	* Positional: There is no real meaning
	* Keyword: The name mean something
		* DO NOT USE THIS WITH AN API
---
## Lambda Functions
* Small functions you can call at any time, only has one expression but multiple arguments
	* Can follow argument restrictions
	* May be useful for mixed strings ("id" + number)
	* Useful in conjunction with other python functions
```python
#Lambda funciton format
f = lambda x,y: x+y
#Same thing explicityly
def f(x,y)
	return(x+y)
```
___
## Higher Order Functions
* Higher order functions take one or more functions as arguments.
* This is where lambda functions can be implemented
```python
#Example of manipulating a sort function
Mylist = ["1","2","3","100"]
#Casts the elements in the list as an integer
print(sorted(MyList, key = lambda x:int(x)))
#Filter can operate the same way
filter(function, sequence)
#Sorting based on length
sorted(cards, key lambda x:len(x))
```
* Lambda functions operate as modifying individual elements within the list