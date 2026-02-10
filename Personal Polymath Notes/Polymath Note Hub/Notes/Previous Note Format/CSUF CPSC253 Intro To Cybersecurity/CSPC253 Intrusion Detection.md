___
**Summary**
* How do we know if there is a security breach?
___
**Security**
* **Security Intrusion** Unauthorized set of bypasses of a security mechanisms.
* **Intrusion Detection:** The systems that are built to detect security intrusion
___
**Classes Of Intruders**
* **Cybercriminals:** Organized crime to get a financial award.
* **Activist/Hacktivists:** There are looking for a social or political award or cause.
* **State-Sponsored Organizations:** Groups of hackers that are hired from the government to do espionage.
* **Others:** Technical people, ethical hackers, etc.
___
**Intruder Skill Levels**
* **Apprentice:** Hackers with minimal knowledge.
* **Journeyman:** Novice Knowledge
* **Masters:** Makes their own knowledge to be utilized.
___
**Examples Of Intrusion**
* Remote Root Compromise
* Guessing And Cracking Passwords
* Copying Database Data
* Distributing Pirated Software
* Unsecured Modems
* Impersonating An Employee
___
**Intruder Behavior**
* Target Acquisition and Information Gathering
* Initial Access
* Privilege Escalation
* Information Gathering & Exploitation
* Maintain Access
* Covering Tracks
___
**Intrusion Detection System**
* Systems that are installed hardware & software to help monitor and detect intrusions.
* **Sensors:** Collect Data
* **Analyzers:** Determine if intrusion has occurred utilizing the data from the **sensors** and other **analyzers**.
* **Interface:** View output of control system behavior.
___
**IDS Classification**
* Depends on the source and type of data analyzed.
* **Host-Base IDS:** Monitors that characteristics of a single host.
* **Network-Based IDS:** Monitors the network
* **Distributed Or Hybrid IDS:** Monitors both host and networks simultaneously.
___
**IDS Requirements**
* There is fine balance between alerts and detections of systems. False alarms should be minimal.
* **Run Continually:** Minimal human supervision and run continually.
* **Be Fault Tolerant:** Should be able to recover from crashes, software, and hardware faults.
* **Resist Subversion:** Should be able to defend itself from malicious attacks.
* **Impose A Minimal Overhead:** Isn't too performant heavy
* **Configured According To System Security Policies**
* **Must Be Scalable**
* **Provide Graceful Degradation Of Service:** Allows the components to work simultaneously.
* **Dynamic Configuration:** Allows the IDS to reconfigured while its active.
___
**Analysis Approaches**
* **Anomaly Detection:** Collects data over time and creates a normal behavior. Then looks at current behaviors and then compares if this is normal or an intrusion.
* **Signature/Heuristic Detection:** Uses preconfigured malicious data patterns to compare if there is an attack.
___
**Anomaly Detection**
* **Training Phase:** Providing normal data
* **Detection Phase:** Comparing normal behavior with current behavior.
* Often Statistical, Knowledge-Based, Machine-Learning
___
**Signature Or Heuristic Detection**
* Compared know malicious pattern to system or network data.
* Pros: Low cost and doesn't use much resources
* Cons: Don't identify new malware and signatures
* **SNORT:** NIDS that detects all potential threats based on rules
___
**Data Sources And Sensors**
* Common Data Sources
	* System Call Traces: Where is the data coming from?
	* Audit Log Files: What is happening?
	* File Integrity Checksum: Virtual Signatured
	* Registry Access.
___
**Logging Of Alerts**
* TImestamp
* Connection Or Session ID
* Event Or Alter Type
* Rating
* Network, Transport, and Application Layer Protocols, etc.
___
**Architecture For Distributed Intrusion Detection**
___
**NIDS**
* Monitors network traffic and collects the packets metadata.
* **Monitoring Interface:**
___
**Stateful Protocol Analysis**
* Collect data from 3rd party so get a better detection of models and threats.
* This utilizes a lot of resources and headroom
___
**Honeypots**
* A vulnerable system that attracts malicious users
	* Low Interaction Honeypot: A fake system
	* High Interaction Honeypot: A real system
____
