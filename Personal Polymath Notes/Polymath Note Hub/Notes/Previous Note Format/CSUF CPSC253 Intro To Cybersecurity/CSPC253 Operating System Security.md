___
* **CIA-Triad:** Confidentiality, Integrity, and accessibility (always used for protecting information system assets)
* We will be looking at the firmware (operating system, server kernel, etc.)
___
**Computer System Layers**
* Hardware (storage, graphics cards, RAM, display, etc.) based on what's needed.
* Operating system (constant process and bridge) kernel and bios (startup), how the underlying system works with the hardware. 
* User applications (programs we use for a certain task or purpose)
___
**Top Four Strategies Of Prevention**
* White-list approved applications: applications are given permissions and considered safe. Focused on the unknowns.
* Patch Third-Party Applications: Actively patching vulnerabilities that show up; avoids operating system vulnerabilities.
* Restrict Administrative Privileges: Give access to those who need it. Rather than giving everyone administrative relative.
* Create a defense-in-depth system, make multiple defensive layers.
___
**Operating System Security**
* System freshly installed means it can be compromised. Install software and search for patches. Utilize a **planned deployment process.**
	* What are the current risks of deploying the system
	* Secure the operating system and key applications
	* All additional critical content is secured
	* Maintain a current patch and software version
	* Ensure appropriate constant security maintainability.
___ 
**Windows Security**
* Patch Management (Installing latest windows update), sets the ground in the update.
* Users admin and access control (least privilege access).
* Windows defines its own permissions in order to add more security layers.
* User account control, offers permissions when necessary.
* Application and service configuration is monolithic by nature.
* Antivirus and built-in countermeasures are also available on windows
___
**Virtualization Security**
* Abstracts resources used by software that is simulated & supports multiple operating systems.
* Hypervisor serves as the liaison between the base operating systems and simulated operated system (virtual machines)
* Can help with testing software on other operating systems.
___
**Containers**
* Similar to VMs, but only contain the application itself.
___
**Virtualized Infrastructure Security**
* Uses of firewalls, access control, and configuration files is what maintains a virtual environment.
___
**Linux Security**
* Core system maintenance and configuration
	* Minimize attack surface
	* Include controls of the underlying system such as network and hardware
	* Patch management is used to maintain modern protections to patch any unknown or possible.
	* Disable services that are unneeded.
	* Logging and log rotations, knowing what is going on with the machine.
* File systems and access control
	* Maintain least privilege access on the system
	* #! first line of any script that is used to determine what interpreter would be used.
* Network Process and isolation
	* Defining what services have remote access, where to promote countermeasures like firewalls.
	* Chroot jail, fake root that isolates the intruder.