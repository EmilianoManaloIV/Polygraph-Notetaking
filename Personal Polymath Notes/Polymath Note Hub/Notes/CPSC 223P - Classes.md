---
NoteType: Theory
NoteCreation: 2026-03-17
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Classes Introduction
* Classes that model entities that can have data and functions packaged into one; blueprint of an entity.
* When an object is created (instantiated) it now exists.
* **Class:** Blueprint
* **Instance:** Existing entity bound by the blueprint
---
## Names And Objects
* **Names** are **labels** for objects which identifies a certain **instantiation**.
---
## Python Scopes And Namespaces
* **Namespaces:** bounds in the area of your code where things are executed; often utilized as a dictionary.
* **Scope:** Area where you the program is allowed the namespace occurs.
	* **Local Scope:** Smallest area of scope
	* **Non-Local Scope:** Between the local and global scope
	* **Global Scope:** Furthermost user defined scope
	* **Built-In Scope:** Scope provided in base python
	* Only works inside out.
```Python
#Elevate a variable into the scope of "global"
globalVar
def someFunction()
	global globalVar
#You can do the same with "non local"
nonLocalVar
def someFunction()
	nonlocal nonLocalVar
```
___
## Class Definition Syntax
* Define a class
```Python
class className:
	<statement-1>
	.
	.
	.
	<statement-N>
```
---
## Class Objects
* You can instantiate an object, or you can collect attributes/variables of a class
* Utilize the . notation to access the object methods and attributes by reference or by assignment.
```Python
#Initialize a class
someVar = myClass():
#Initailize a class with values (Constructor)
	def __init__(self, var1, var2):
		self.a1 = var1
		self.a2 = var2
		
```
* Variables can be created at runtime, without prior instantiation.
* You can extract functions straight from a an object if needed by assigning the function reference to a variable.
---
## Inheritance
```Python
#This is how you create your own derived class
class DerivedClassName(BaseClassName):
#You can do the same with modules
class DerivedClassName(packageName.BaseClassName)
```
* Looks for functions in parent class if not found in their parent function.
* You can use super().functionName to call the function in the parent class
---
## All Classes Derived From Object
```Python
#You can check how instants are related to classes
isinstance(instance, class)
#Or how classes are related to each other
issubclass(childClass, parentClass)
```
* All of these things are based off of hierarchy.
---
## Overriding Methods
* You can override methods by using the same name when deriving another class, have to use the same amount of arguments.
---
## Multiple Inheritance
* You can do multiple inheritance for multiple classes
```Python
class DerivedClassName(Base1,Base2,Base3)
	<statement-1>
	...
	<statement-N>
```
* Note is reads **LEFT** to **RIGHT** (DOWN-UP, depth-first)
* Skips if there is an overlap
---
## Private Variables
* We use notation to set private variables with _ and __
	* __ actually changes the variables name at runtime, this is called name mangling
```Python
__variableName
#This turns into at runtime:
_className__variableName
```
* You can do the same with functions, by instantiating the functions.