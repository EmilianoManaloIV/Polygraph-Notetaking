___
**Midterm Review**
* The final may have questions from slides and also be based on scenario.
* Final will be not cumulative and starting now will be covered (Week 8 - Onwards)
* December 16 is the final exam
___
**Project Deliverables**
* Include all diagrams and some description
* State Machine and Data Flow will be a group assignment, based off group assignment.
* Look into cloud services.
___
**Cloud Native Development**
* Creating application on a cloud environment and then immediately deploying it on the cloud.
* Building Blocks
	* Compute
	* Network
	* Storage
* SQL (Structured Data), noSQL (Non-Structured Data), how is the data being stored?
* CI/CD
* Conternization/Docker
* Kubenates
___
**Architecture**
* Describes the high-level components of the software. Defines the system organization , interaction, and principles.
* Gives a high-level overview to the stakeholders.
* Provides a blueprint and facilitates clearer ideas between teams.
___
**Architectural Design Process**
* Identiy requirements
* Architecture Patters
* Design components and interfaces
* Validates architecture through prototypes and reviews.
___
**Architectural Styles**
* There is several architectural styles that often improve a system but not necessarily solves a problem.
* **Monolithic:** A singular repository to hold all components of your software. They are all closely related to each other.
	* Pros: Easy to deploy, Simple Repo, Easily Deployable
	* Cons: The entire application must be moved all at once and redeployed.
* **Layered (N-Tier):** Application is divided into layers that add certain components to the software. They are compartmentalized. Some systems can fail and some systems can operate.
	* Pros: Deployment is fast and easy to test
	* Cons: Reduced performance and the layers are still coupled. Communication overhead and difficult to maintain.
___
**Phase 2 Deliverables**
* Architecture
	* Components
	* Services
	* Underlying Systems
* Implementation
	* Tech stack
	* Programming Language
* Testing
	* Testing processes
* Deployment
	* Deployment diagram
* **December 8: DUE**
* **December 9 & 11:** Presentation
* **December 16:** Final
* **15-20 minutes for the presentation**
* **200 Points**
	* 130 pts Application Documentation
	* 20 pts SCRUM Artifacts
	* 50 pts Presentation
___
**Testing**
* Manual Testing: Going through the application and testing it directly
* Automatic Testing: Creating a procedure that automatically tests the system through code.
___
**Model-View-Controller Pattern**
* Often focused with the presentation layer of an application
* Three parts
	* Model
	* View
	* Controller
___
**Model-View-ViewModel Pattern**
* Also is concerned with the presentation layer of an application
* Three Parts
	* ViewModel
	* Model
	* View(s)
___
**Microkernal Architecture**
* Operating system and IDEs
* A core system is given ends of components that interact with other sub-systems
___
**Pipe And Filter Architecture**
* Deals with how data is manipulated throughout the system via pipelines.
___
**Event-Bus Pattern**
* Relates an action or event that then relates that event to the relationship between the action and consumer.
___
**Space-Based Architecture**
* Utilizes real-time processing that scales with hardware to make data manipulation and retrieval more efficient.
___
**Clean Architecture**
* You divide everything into parts that are part of the whole. There is a hierarchy when it comes to the center application outwards.
___
**Serverless Architecture**
* Cloud provider manages your system. You still have to implement your own logic when it comes to interacting with the system.
___
**CQRS**
* Separation of read and write methods. There is a separation that increases scalability but makes the system potentially complex.
___
**Event Sourcing Pattern**
* State based application the stores a series of events within the application.
___
**Repository Patterns**
* Abstracts the system into versions of itself.
___
**Adapter Pattern**
* Creates a wrapper that bridges the systems between new and older interfaces. Creating compatibility but increases complexity.
___
**Observer Pattern**
* Based on an update function that links with an observer that then invokes a function that changes the base object that invoked the event.
___
**Singleton Pattern**
* Creates a centralized system that takes all components into one stream.
___
**Factory Pattern**
* Based on the subclasses will dictate what object should be created. And how it should be used in the system.
___
