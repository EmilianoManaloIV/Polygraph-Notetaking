---
NoteType: Theory
NoteCreation: 2026-01-26
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 386 - Introduction To Game Design]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Unity's Interface
* **Toolbar:** Allows access to tools, version control, and pre-determined layout system.
	* **Scene View**: Lets us develop the game freely; editor interaction.
	* **Game View:** Determines interaction with the game; bound to the player.
	* **Play mode:** Activates the game scene and game process. You can also pause the game when necessary.
* **Hierarchy:** Determines the relationship between objects within the scene.
	* **Parent/Child Relationship:** Objects have a parent and child relationship.
	* **Transforms Are Relative:** Parent component transformations effect child components.
* **TIP:** You can change the color of the window depending if in play mode.
* **Navigation:** There are several ways to navigate in the unity editor.
	* **Q:** Pan
	* **W**: Position
	* **E**: Rotation
	* **R**: Scale
	* **ctrl**: Snap
	* **ctrl + s:** Save a scene
	* **F**: Well frames selected object
* **Inspector:** Presents the data associated with the objects or assets.
	* **Components**: Given behaviors of object within a game
	* **Field:** Associated data that is within a component.
	* **References:** Objects that are associated with other objects or assets.
	* **Circle/Gear:** Can select associated asset or object
	* **Tag:** Organizes objects
	* **Layer:** Associated layer properties of the object, collider gating.
* **Project Window:** Contains assets you may use within your game (code, objects, shaders, etc.).
	* **Debug Window:** Allows to modify certain objects at a certain level.
* **TIP:** You can load and unload, or load multiple scenes at the same time. You can also get real-time data while testing while in play mode. File explorer gives are explicit detail when copying and pasting assets.
* **Canvas:** Serves as the UI space of the object.
	* **World Space:** Relative to origin
	* **Canvas Space/Screen Space:** Relative to camera-view
* **TIP:** Make sure that dependencies are checked and have safeguards in place. **Readme:** Objects can serve as formal documentation within the editor.
* **Menu Settings:** Provides various windows and settings to adjust your project.
