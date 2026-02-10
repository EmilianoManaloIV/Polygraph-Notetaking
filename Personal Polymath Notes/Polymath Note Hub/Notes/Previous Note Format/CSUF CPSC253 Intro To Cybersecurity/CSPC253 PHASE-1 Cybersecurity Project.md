___
**Topic Selection**
Event: [**GhostAction Campaign (September 2025)**](https://blog.gitguardian.com/ghostaction-campaign-3-325-secrets-stolen/)
CVE: https://nvd.nist.gov/vuln/detail/cve-2025-30066
___
**Research And Analysis**
___
**CVE Research**
* **Provide A Detailed Description Of CVE**
	* The CVE described a **network** based attack that lead to many GitHub repository secretes being leaked. The attacker achieved this by maliciously committing code into the Git repositories that had the tags *v1* through *v45.0.7* and reading the logs of said repositories. The commit pointed to 0e58ed8 which had the malicious update features code that allowed the logs to output secrets and keys. The CNA: MITRE score was at an 8.6 and also pointed to the attack as low complexity.
* **Discuss The Vulnerability, Including Technical Details And Impact**
	* For context, GitHub is a platform to collaborate and even host certain software in raw code form. On this platform there is an action called "tj-actions/changed-files" which keeps track of changed files and keeps record of the change; is essential in CI/CD workflows. The attacker then targeted the tj-action bot account which often has higher permissions and is used as a middlle-man to maintain tj-actions/changed-files. The attacker then somehow got the Personal Access Token, which allows the user to essentially "login" as the bot (think of the password of someone's GitHub account). This gave the permissions and thus injected a malicious commit into the code. This commit then called on software to be forcibly downloaded and start scanning any key information such as API keys, GitHub PATs, npm tokens, and RSA keys. All this data to be extracted was then dumped into the logs so that the attacker can collect the private information. 
	* The vulnerability was that even through the key was compromised, there wasn't any way to verify that this PAT is directly linked to a certain user. The resulted in malicious code being injected and private sensitive information being extracted. This often points to how workflows without proper authentication processes can lead to not only private information being leaked, but unverified changes that can do serious damage to any data storage or software system.
* **Explain the attack vector and potential exploitation methods**
	* The attack vector was done remotely using the network as the main platform of attack. This was done by attaining a PAT key and not having any verification method to verify that this attacker is *not* the bot which lead to permissions being granted to someone other than the bot. This can be ascertained through listening techniques, brute force methods, and unencrypted data being leaked. Confidentiality and Integrity where key components of the CIA triad that where effected. 
* **Describe the affected systems and software.**
	* Several software where effected in this attack not in functionality but in confidential information. Since API keys among other things where leaked in the public logs, secrets essentially have been effectively exposed which depending on the information can endanger software infrastructure and data integrity. In this case, it really does depend on what information was dumped in the logs and can interfere with the CIA triad among other sub-systems.
___
**Current Event Analysis**
* **Summarize The Selected Event**
	* The event followed by this attack effected many repositories within github. This then essentially leaked important information to maintain github based software. The attackers utilizing automated bots gave themselves exclusive roles to overwrite and push malicious commits that dumped critical confidential information into the logs. 
* **Relation**
	* This relation is in direct contact with CVE-2025-30066 and are exactly coordinated. This CVE is the result of this event.
* **Implications For Cybersecurity Practices And Policies
	* **Access Control:** There should be stronger restrictions when it comes to accessing or changing systems. Especially when it comes to letting a bot automatically commit certain pieces of code into a primary system.
	* **Awareness And Training:** There should be more training in how automation can be used without undermining needed security in certain situations.
	* **Audit And Accountability:** There should be careful considering what is considered private or public logs, especially it can be accessible without needing roll specific requirements.
	* **Certification, Accreditation, And Security Assessments:** There should be a certification or security regarding automated systems.
	* **Configuration Management:** Absolutely a much needed refinement as the attackers where allowed to access files that exposed many secrets by dumping data into the logs.
	* **Contingency Planning:** Allow the use of overwrite of previous files or a way to maintain current activation and carpmentalize the security breach.
	* **Identification And Authentication:** This is a need as allowing a bot with accesses that allow malicious code is unacceptable.
	* **Incident Response:** Establish proper systems in place in order to maintain bot security.
	* **Maintenance:** Mayhaps do a bot test to determine if the bot has exlusive access that can be utilized my a malicious attacker.
	* **Media Protection:** Looks like the media was secured, but underlining system was breached.
	* **Physical And Environment Protection:** 
	* **System And Services Acquisition:** 
	* **System And Communications Protection:**
	* **System And Information Integrity:*
___
Phase-1 Report Compilation**
* Briefly introduce the importance of threat intelligence and CVE analysis.
	* L.K. (2000). CVE: An alert by any other name. _EWeek_, _17_(46), 142.
	* Omer Eltayeb, O. E. (2024). The Crucial Significance of Cyber Threat Intelligence in Mitigating Cyber Attacks. _Pakistan Journal of Life & Social Sciences_, _22_(2), 1760–1772. https://doi.org/10.57239/PJLSS-2024-22.2.00123
	* Santos, P., Abreu, R., Reis, M. J. C. S., Serôdio, C., & Branco, F. (2025). A Systematic Review of Cyber Threat Intelligence: The Effectiveness of Technologies, Strategies, and Collaborations in Combating Modern Threats. _Sensors (14248220)_, _25_(14), 4272. https://doi.org/10.3390/s25144272
* Detailed explanation of the CVE (as researched above)
	* https://blog.gitguardian.com/compromised-tj-actions/
	* https://www.stream.security/post/github-action-supply-chain-attack-exposes-secrets-what-you-need-to-know-and-how-to-respond
	* https://www.wiz.io/blog/github-action-tj-actions-changed-files-supply-chain-attack-cve-2025-30066
* Summary and analysis of the related current cybersecurity event.
	* Direct relationship to the GhostAction campaign event on GitHub (CVE is directly related)
* 


