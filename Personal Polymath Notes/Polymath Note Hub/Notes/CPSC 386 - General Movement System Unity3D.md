---
NoteType: Practice
NoteCreation: 2026-02-11
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 386 - Introduction To Game Design]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Planning
* Create a movement system that is modular within the confines of the Unity3D project, first person.
* The goal is to compare a system I created using my own research and with help with generative AI.
* Would cost some time, but remember this is for modular use on multiple projects and something you can call your own.
___
## Requirements Gathering
* First Person
* Within the scope of Unity3D
* Basic movement and mouse factors
	* Moving Mouse Relevant To Player Camera
	* Run
	* Jump (With ground state)
	* Crouch
	* Prone
	* Relatively Move Forward
	* Relatively Move Backward
	* Relatively Move Left
	* Relatively Move Right
* Adjust certain properties:
	* Mouse Sensitivity 
	* Walk Speed
	* Run Speed
	* Crouch Speed
	* Prone Speed
	* Remap Inputs
	* FOV
---
## Design
* Integrate a character controller with a custom script that allows modification of mouse sensitivity, walk speed, run speed, crouch speed, prone speed, various different input systems, and FOV slider. Given the developer options when it comes to even modifying the script for their own use. The character controller must be able to adapt in sour states known as walk, run, crouch, and jump (air strafing may be advised)
* Helpful Links:
	* https://medium.com/@fulton_shaun/character-movement-in-unity-3-ways-to-do-it-b10c6fd1a909
* AI Prompt: I'm making a first person controller for Unity3D, I want to utilize the character controller component to be integrated with a custom script that can adjust the following parameters: mouse sensitivity, walk speed, run speed, crouch speed, prone speed, FOV slider, remapped inputs. The character controller also needs to adjust properly to four different states such as: walk, run, crouch, and jump.