---
NoteType: Theory
NoteCreation: 2026-03-10
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[Landing Page]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Syntax/Parsing Errors
* Issues with writing the code before the code is event executed.
---
## Exceptions
* Code though statically correct does not mean it will run properly; dividing by zero, index overflow, name error, type issues, etc.
---
## Handling Exceptions
* Utilize the **try** and **except** 
```Python
#This is a try operation while true
try:
	#Executes fully if there is no error
	x = int(input("Enter A Value"))
	break
except ValueError:
	#Executes if an error is found
	print("ERROR: INVALID VALUE")
except (Error1,Error2,Error3):
	#Executes if any of these errors occured
	pass
#Executes as normal if no exception is found or unhandled exception
```
* **Else** will execute if no exceptions occur at all.
```Python
else:
	#Executes if no exception is found
```
* You can get the error itself as a type and display it to the user
```Python
#Stored as a variable which can be accessed
except Exception as someVar: 
#Print the error
print(someVar)
```
* Try and catch cases can operate outside of the local function; handles them within global scope.
* **raise:** raises an error immediately like it was invoked by the interpreter; has to be under the **exception class** (something you can derive)
* You can reraise it back if you want to, so its not being called but handled.
---
## Exception Chaining
* You can do exception chaining with from so that all exception error messages are shown.
```Python
def somefunc():
	try:
		int("someString")
	except anotherError as e:
		raise RuntimeError("Parsing Error Occured") from e
```
---
## User Defined Exceptions
* You need to make a class of type Exception to make your exceptions
```Python
#Creating your own exception in python
class ErrorName(Exception):
	pass
```
---
## Defining Clean-Up Actions
* **finally:** Executed regardless of exceptions or not; always runs last after everything within the scope.