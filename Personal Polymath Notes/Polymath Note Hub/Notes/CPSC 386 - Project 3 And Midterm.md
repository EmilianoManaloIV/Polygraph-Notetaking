---
NoteType: Theory
NoteCreation: 2026-03-23
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 386 - Introduction To Game Design]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
# Snapshot Beta
## Idea:
* Photography Simulator With First-Person Shooter Elements; The Player Is Tasked With Taking Certain Photos Provided By The Clients.
## Inspiration:
* Interior Worlds
* Various Steam Photography Simulators
* Call Of Duty Pick Attachment System
## Core Mechanics:
* Switching Out Gear
* Completing Missions 
* Exploration
* Skill progression and game persistence (save files?)
* Player Settings (Rebinding, FOV, Volume, etc.)
## Interested Focus
* Raycasting, rendering, shaders, saving non-structured data, and real time mesh creation.
## System Code In-Theory Place
### Primary Managers (Singleton Pattern)
* **GameManager**
	* Handles all scene data and actions
* **PlayerManager**
	* Handles all player data and actions
* **CameraManager**
	* Handles all camera data and actions
### Object Mangers (N-Series Pattern)
* **Subject**
	* Handles all logic regarding item detection and attributes
* **Missions**
	* Handles how missions are provided and the attributes needed to complete the mission.
* 
* ****