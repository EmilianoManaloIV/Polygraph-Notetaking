---
NoteType: Theory
NoteCreation: 2026-01-28
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 386 - Introduction To Game Design]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Half Real
* Video games are a subset of games, which means, real world "rules" determines the actions and goals of the game. They highlight key points:
	* **Intractability**
	* **Easy Goal Setting**
	* **Key information or actions.**
* We want to **mitigate friction** between the game and the user or users.
* This "fictional world" can be **presented as is** or utilize the **experience the immersion and imagination of the player**.
___
## Player Vs Games
* **Play**: Its free form, just the action itself and having a pleasurable experience.
* **Rules**: Creates restrictions that creates unique or dynamic experiences.
	* There is an meta awareness of the game; which causes all parties to understand the rules and goals dictating the game.
* There is direct feedback with one's consequences which tells the player what they are good at and where they can improve.
	* This feedback can give a "reward" in regards to **overcoming the challenge**
	* There is an experience of community around a game: socializing/competition: appeals to the players.
___
## Games Vs Rules
* In a game there is something to overcome which requires some degree of skill and improvement.
* Video game rules having the benefit of having **definite, unambiguous, and easy to use**
* There is a degree of **progression** and **emergence** and these traits will cause variation within the game.
	* Rouge likes are very good and embracing this dynamic
	* Simple components for complex interactions
	* Progression is natural when it comes to overcoming challenges in different ways; even in sequential scenarios.
	* All of these things promote replay ability
___
## Games As Fiction
* The game may not be always realistic, things that are fundamentally fictional (There is a balance between fiction and rules):
	* Death and respawning
	* Creating things from nothing
	* Dying and loading
	* Characters discussing controls with the player
* The player tends to forget other fictional elements when the rules take priority for the player.
	* Multiplayer actions
	* Graphical Fidelity
	* Progression may influence the character to pay more attention to the fiction.
___
## Classic Game Model
1. Rule based formal system
2. Variable and quantifiable outcomes
3. Different outcomes have different results
4. Players need to put in effort to see results
5. Player is emotionally attracted to the outcome
6. Consequences are optional and negotiable
* Must be fulfilled to be considered a game
	* The game itself has a set of rules
	* Level of the player's relation to the game
	* Relation between the activity of playing the game and the rest of the world.
___
## Games Vs Players
* Games with rules to itself and how does that influence the player?
* People always select unenforced rules that the player often chooses and how its translated.
	* This creates variation as these rules can diverge from the original rules provided.
	* Furthermore, the creation of these things can create strategies meta-gaming
* Choosing to play a game is a meaningful choice even if the rules are different.
___
## Rules Or Fiction
* **Rules of irrelevance**: if the representation is different the rules still apply.
* They are both rules and fiction, since they coherently work together.
* The meaning of the game is arbitrary, you can represent it in many ways:
	* altering the graphics can give it a different meaning
	* Space invades with other space ships with public figureheads.
___
## Other Analytical Axes
* Narratology (as a story) vs Ludology (As your own experience)
* Ontology (what games are) bs Aesthetics (What makes a game enjoyable)
___
## More About Unity
* **Scenes**: Loads multiple objects at once
* **Game objects:** Logical entities that contains **components** (behaviors of a game object):
	* **Transform:** All positional data, scale, and rotation
	* **Sprite Rendered:** Draws the sprite of an object
	* **Collider2D**: Provides the collision logic of an object
	* **Rigidbody2D**: Provides the physics property of an object
		* **Dynamic:** Fully simulated, gravity
		* **Kinematic:** Object that exists without forces, but can interact with other physics object.
		* **Static:** Doesn't move an object, but still creates a collision based system
	* **Camera:** Renders the scene within the perspective of the player
* **Tags And Layers:** Provides object finding, sorting, and dynamics; organizational tools
* **Object Parenting**: Children will inherit certain properties from its parent; and adding components to its child may interact differently than its object.