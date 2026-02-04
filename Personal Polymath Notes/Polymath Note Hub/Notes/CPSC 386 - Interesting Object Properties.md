---
NoteType: Theory
NoteCreation: 2026-02-04
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 386 - Introduction To Game Design]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Debugging Objects
```C#
//You can always use logs to detail information
Debug.Log("This Message Will Show Up In The Console Within The Editor")
```
___
## J-son And Registry Serialization Using PlayerPrefs
* Keep note of string length over 2 kilobytes of data (Use For Simple Data), string, int, float
```C#
//How to save persistant data on a given platform such as saving a previous posiition.
PlayerPrefs.SetString("PersistantLocation", JsonUtility.ToJson(transform.position))
//To retrieve and query the data that was saved in the position tuple
Vector3 v = JsonUtility.FromJson<Vector3>(PlayerPrefs.GetSTring("PersistentLocation"))
```
___
## Version Control
* Reverting your project and having "saves" creates a safeguard against possible issues.
___
## Unity's New Input System
* There is more robust systems current in place that expand to multiple actions and inputs.
* **Input Actions Object**: An object that can save and configure mapping for a given platform. It also allows segmentation of scenes and sets of actions.
* Delegation of multiple actions for the same result or response serving as a function call.
* You can use this input as a method to auto-assume changed values.
___
## Monobehaviors
* Fields that are exposed are considered public, or tagged with **serializedfield** tag. Best option for proper field 
```C#
[field:SerializedField]
```
* **Script Execution Order**: To address race conditions you can prioritize which methods are executed first.
___
## Prefabs
* Serves as templates for an object, which means they have their own execution as a game object.
* Blue represents unsaved changes to the prefab you are modifying or overloading.
* Changed values dictate what parts of the prefab are serialized or not
