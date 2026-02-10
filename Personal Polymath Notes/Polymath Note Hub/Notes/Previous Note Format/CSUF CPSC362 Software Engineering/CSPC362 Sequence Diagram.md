___
**Sequence Diagram**
* How does the actor interact with the system, how does the other systems interact with each other. 
* Components:
	* **Actor:** external user (stick figure "user")
	* **Object/System Components:** system (boxes "subsystems")
	* **Lifeline:** Determines the flow of action that originated at an object. Dotted line represents a "reply" from a system down the line. Often is manipulated by conditionals.
	* **Actionable:** Rectangular lifeline means that this system is active during this portion.
	* **Frame/Fragmentation:** Show the sequence of interactions for an object.
* Types Of Messages:
	* Synchronous: waits for the next reply to execute the next step.
	* Asynchronous: works independently from the rest of the system or without input.
	* Lost & Found: a conditional where if any output to another system is terminated or originating from somewhere unknown.
	* Self Messages: the object calls itself to do something.
___
**Instruction For Sequence Diagram**
* Active Actor
* Controller: provides the execution of the workflow
* Participating Objects
* Passive Actor
___
**Fragmentation Operators**
* "alt" used for if then else or switch cases.
* "opt" if then
* "loop" loop a certain amount of times
* "guard" a testable condition
* "break" terminate the action based on some conditional
* "par" congruent tasks
* "ref" represent another sequence diagram or an abstraction of another process
___
**Traceability Engineering**
* Use Case Diagram -> Use Case -> Use Case Description -> (Class Diagram, Sequence Diagram, Program Code)
* We focus on the links between systems and components and how they operate together.
___
**Activity Diagram**
* **Components:**
	* **Initialization**
	* **Conditional**
	* **Forks** (Concurrent/Parallel)
	* **Joins** (Two Or More Flows Combining To Create One Flow)
	* **Final State** (Activity Concludes/Terminates)
* Depicts how the operations or systems are executed.
___
**Midterm**
* 40 Questions
	* Fill in the blanks
	* Matching
	* Multiple Choice
	* Canvas
* Cheat Sheet Allowed (1 A4 Paper/Front & Back, Can Be Printed/Handwritten)
* In-Person