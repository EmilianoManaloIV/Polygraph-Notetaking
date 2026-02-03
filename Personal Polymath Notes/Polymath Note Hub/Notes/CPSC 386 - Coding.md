---
NoteType: Theory
NoteCreation: 2026-02-02
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[Landing Page]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Namespaces
* Use you're own namespaces to avoid conflict errors.
___
## Lists And Dictionaries
* **Lists**, similar to an operation such as a vector in C++
* **Dictionaries:** A hash table to retrieve data based on other variables or key-unique identifier.
* The unity serializer operates differently, recommended to use Odin to serialize data. Change how to process data:
	* Muli-list systems for serialization and deserialization
___
## Coroutines
* Executing codes on different frames, you can use things such as 
	* **IEnumerator**
	* **Yield Return Null**
	* **new WaitForSecond(FloatValue)**
* An alternative to the basic update frame and other default coroutine options.
___
## Quaternion
* Rotational values utilizing **EulerAngles**
* **Slerp:** The smooth transition between different angles based on Quaternion values
___
## Delegates
* Creates predetermined functions and variables that can be manipulated at runtime.
___
## Events
* Delegates that are built into the unity game engine and need to be addressed under race conditions.
* You can assign a function at runtime to create dynamic assigned functions.
___
## Readability And Usability
* There is many tools to organize your code.
```C#
//Add regions to help you
#region <name>
//This is a doc string for developers
/// <summary>
/// This does something important
/// <summary>/
```
___
## Attributes
* You can set permissions to avoid run-case errors.
* Use Debug menu to see all serialized and unserialized values