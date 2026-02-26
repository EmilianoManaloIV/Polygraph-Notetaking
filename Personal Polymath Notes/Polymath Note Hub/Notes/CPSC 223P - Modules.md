---
NoteType: Theory
NoteCreation: 2026-02-24
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****

## Modules
* **Modules** are .py files, brings functions and variables from other modules.
```Python
#To include a module from another script
import moduleName
#Import just the functions
from files import *
```
* Note that functions that run in other modules are called will execute based on import order.
* **__name__:** Global variable that is contained with every module, __main__ exists when its the point of entry.
---
## More On Modules
* You can specify and select which functions you can import
```Python
#Import certain function
from someModule import function1, function2
#Import all functions
from fibo import *
#Import fib as an object
import someModule as moduleName
moduleName.someModuleFunction()
```
---
## Executing Modules As Scripts
* You can always do a check to determine if you are running the right script or not, using global variables or other check methods.
```Python
#Execute a certain function or operation if main
if __name__ == '__main__':
	functionExecutedIfMain()
```
* Wanna give a parameter at command line execution? Saved as a list, element [0] is the filename, followed by any arguments the user typed in the command line.
```Python
import sys
#Access list
sys.args[certainElement]
#Make sure to cast when necessary
```
---
## The Module Search Path
* Search Order
	* Is it a built-in module?
	* It is a system path module: **list of directories**
	* Check active directory
___
## Compiled Python Files
* The only time something is compiling in python is when importing in certain files.
---
## Standard Modules
* A module that helps directly interact with the interpreter itself.
___
## The dir() Function
* Gives all the functions and variables you defined
```Python
dir(someModule)
#List all built in python modules
import builtins
dir(builtins)
```
___
## Packages
* A **package** is a directory of **modules**
* You need this is every component of the directory to be considered a package
  ```__init__.py```
* You can import all or selectively import packages
```Python
#Import a certain sub package, must be majoriy of packages
import primaryPackage.subPackage.subSubPackage
#Import the package with something user defines
from primaryPackage.subPackage subSubPackageName
```
___
## Importing * From A Package
* You can import everything using 
```Python
#Imports everything in __all__ within the __init__
from package.subPackage import *
```
---
## Intra-Package References
* You can use relative path to change references
	. or .. or ..packages
---
## Packages In Multiple Directories
* You can use this to specify the reference in \__path\__, can be used to extend the uses of the package.