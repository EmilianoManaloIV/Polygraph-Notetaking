___
**Message Authentication**
* Message Authentication: MAC
* User Authentication: MFA
* Data Authentication: Hash
* Entity Authentication: Digital Certificates
___
**User Authentication**
* The process of establishing confidence is under identities that are presented electronically to an information system.
* Two Parts Of The Process:
	* Enrollment and identity proofing
		* Applicant: Applies to the credential service provider and asks for identity proof, CSP responds with a token to applicant which then turns into a subscriber.
		* Subscriber: CSP and subscriber establishes the authentication session and promotes the subscriber to a claimant.
		* Claimant: After the CSP confirms with the verifier.
	* Digital Authentication
___
![[004__Ch03_Ch04_Combined.pdf]]
___
**Risk Assessment For User Authentication**
* Assurance Level: You are almost certainly confident the system is protected?
* Potential Impact: What will be effect?
* Areas Of Risk: Where is the places that will be effected?
___
**Assurance Level**
* Certainty that the user has presented a credential that refers his or her identity.
* Degree of confidence we have that this person is genuine and the right person we have identified.
___
**Levels Of Assurance**
* Level One: Little to no confidence (Message Board)
* Level Two: Some confidence (Password)
* Level Three: Confidence in the asserted identity (Legal Documents)
* Level Four: Needed confidence in the asserted identity's validity. (Medical Records).
___
**Levels Of Impact**
* Low: Limited adverse effect on organizational operations (Pot-luck flyer)
* Moderate: May have a serious adverse effect (Future Promotions)
* High: Severe or catastrophic impact (Government secrets, company secrets)
* Used in most levels of gauge severity of secrets
___
**Password-Based Authentication**
* Uses a password verses user ID to determine the user's privilege.
___
**Unix Password Scheme**
* Salt: random data fed an an additional input to create harder difficulty to guess.
* Maintains difficulty to guess the password and increases complexity by adding more unique avenues to solve.
___
**Password Cracking**
* Dictionary Attack: Uses all passwords against the password file
* Rainbow table attack: Dictionary of the salts
* Password Cracker: Social cues and social media
* John The Ripper: Opensource password cracker
___
**Password Selection Strategies**
* The user must understand the importance of an established ideal password policy to make it difficult to guess.
* The computer may also make-up a password.
* Reactive password checking maintains if a password may have been breached.
___
**Proactive Password Checking**
* A rule is often enforced upon a password that most be followed.
* Password checker, utilized a dictionary to check if a password has been breached.
* Bloom filter is utilized to check if a password has been breached,
___
**Types Of Cards Used As Tokens**
* Smart Card: has a processor (more secure/expensive)
* Memory Card: only holds data (less secure/expensive)
___
**Biometric Authentication**
* Physical characteristics that have difficulty being replicated or his literally impossible. Often based on a cost to accuracy chart.
___
**Biometric Authentication System**
* Enrollment: creates an association with a certain biometric object, then it is saved in biometric database.
* Identification: Details if the biometric object is then related to a biometric profile in the database, sent to system with several profiles.
* Verification: Compares with biometric database and determines if individual through biometric data is who they are.
___
**Remote User Authentication**
* Accessing a computer away from the computer itself, often accessing through the network.
* There is several more threats that can occur when things are done through the network.
* Attacks such as:
	* **Eavesdropping:** someone physically snooping and assuming or guessing your password.
	* **Host Attack:** attacking the password file to get access to passwords and secrets.
	* **Replay Attack:** When someone capture your authentication and then poses as you.
	* **Client Attacks:** Tries to use your local machine to get your passwords and secrets.
	* **Trojan Horse:** Installs an application or device that its soul purpose to collect passwords and secrets.
	* **Denial-Of-Service:** Attempts to disable a suer authentication by overwhelming a server system that uses some type of authentication.
___
**User Access Control**
* **NISTIR7298:** process of permission granting in regards to obtain information or deny physical facilities.
* **RFC4949:** The regulation of users, programs, processes, or other systems and what is or is not allowed.
___
**Access Control Principles**
* Authorization: provides what resources is allowed
* Authentication: clears if that this individual is genuine
___
**Access Control Policies**
* **Discretionary Access Control (DAC):** Controls access based on the identity and rules provided.
* **Role-Based Access Control (RRAC):** Controls based on role-assignment and the roles provide what an individual can or cannot do.
* **Mandatory Access Control (MAC):** Allows only access to certain labels given by the media.
* **Attribute-Based Access Control (ABAC):** Access based on attributes of the user such as business hours or if someone is a client or not.
___
**Components Of Access Control**
* Subject: Entity of capable of accessing Objects
* Object: Items to be accessed
* Roles: Gives the subject what objects it has access to and what actions it can do with the objects.