___
**Review Of Existing VMs**
**Kali Linux Cyberlab VM**
* Establish proper connection pipelines (setup firewall and configure ports).
* In addition to connections, proper logging of every interaction that is done with the virtual machine.
* Have proper systems in place to avoid brute force attacks on admin roles.
* Setup proper RBAC systems, using a "guest account" with least privilege (Directory access & SUDO commands.)
* Disable dangerous software on Kali that may be used for malicious purposes.
* Possibly implement honeypot to ward away malicious users (with logging capabilities).
* Implement brute force attack safeguards such as logging-in attempts or possibly using MFA methodologies.
* Follow modern NIST guidelines that apply to these cybersecurity guidelines. 
* Implement anti-malware systems.
* Implement intrusion detection/prevention systems.
* Utilize disk encryption.
* Lean towards SSH an TLS networked solutions.
* Test on local machine before deploying into a cloud environment.
* Utilize backup systems in case of ransomware or system instability. 
* Let logs be read only, no modification can occur, even admin privileges can't overwrite logs.
___
**Identified And Crafted A Cloud Environment**
* Utilize Azure as the migration tool to setup VM.
* Test on local machine before pushing to cloud (figure out security measures of Azure and migration tools)
* Implement logging sub-systems and NIST guidelines for virtual machines hosted on the cloud.
___
**Draft A Timeline Of The Cloud Migration Project**
**Kali Linux Cyberlab VM**
* 12/1-2/2025 NIST Standard Research List and Azure Research
* 12/3-4/2025 Migration And Implementation
* 12/5-7/20205 Testing, Security Audit, And Deployment
**Batch VMs Timeline (Count 30)**
* 12/8-10/2025 NIST Standard Research and Azure Research.
* 12/11-14/2025 Migration And Implementation (Local Testing)
* 12/15-19/2025 Cloud Testing And Security Auditing 
___
**Post-Completion Writeup**
**N/A**
**Cost Analysis For Two Weeks**
**Lessons Learned**
___
**Migration Plan Document**
* Secure connection protocol: When connected to the cloud there is risk of intrusion and listening attacks. To mitigate this issue we plan to use only encryption channels and secure SSH key based access. 
* Mitigate Brute Force Attacks: Utilize proper lockout procedures if wrong credential is given. Log interaction and possibly utilize MFA systems to verify users. 
* Implement least-privilege methodologies: Utilize proper RBAC systems. Separate between guest user and admin command permissions. Extra authentication for admin permissions. Disable software that may be a risk; isolate environment for cybersecurity testing.
* Harden private access to virtual machine: Using Azure use private Subnet (Azure Virtual Network).
* Setup virtual machine cloud firewalls: Certain SSH interactions, deny other bands of traffic, logging and monitoring systems. Utilize **Azure Firewall**.
* Utilize Azure Monitor Agent to log all interactions with the virtual machine.
___
**Video Presentation**
___
**Actions Taken**
* Update Kali to current Kernal version using 
  ```bash
  #Get Current Kernal Key
  sudo wget bash https://archive.kali.org/archive-keyring.gpg -O /usr/share/keyrings/kali-archive-keyring.gpg
  #Force Update The Operating System
  sudo apt update && sudo apt full-upgrade -y
  #Utilized finally when packages are installed 
  sudo apt upgrade
  #Also utilized the following commands too, and this method worked best
  sudo apt-get update && sudo apt-get upgrade
  #Proceeded to clear extra dependencies that where not necessary
  sudo apt autoremove --purge
  sudo autoclean
  sudo clean
  ```
	* Issues: is that IP server couldn't communicate properly to install packages. Causing major dependency errors. I then proceeded to clear unused dependencies using
	* Issues: Needed to repeat the update command since the wifi here on campus is spotty. Decided that is may best to script a premade system to keep force updating if the program holds for too long.
* Installed UFW firewall and then proceeded to specify open ports.
	```bash
	#Used to install ufw
	sudo apt-get install ufw
	#List currently used services on this machine
	sudo ufw app list
	#Check firewall Status
	sudo ufw status
	#Enable firewall
	sudo ufw enable
	#Enable set permissions
	sudo ufw allow 443/tcp #Allows traffic on https
	sudo ufw allow 3389/tcp #Allows traffic for remote desktop protocol
	sudo ufw allow 22/tcp #ALlows traffic for SSH keys
	sudo ufw deny 80/tcp #Deny traffic for unsecured websites explicitly 
	```
* Installed SNORT IDS to compliment ufw firewall utilizing
```bash
#Install latest SNORT software
sudo apt install snort -y
#Activate IDS with logging on root accout
sudo snort -A console -i eth0 -q -c /etc/snort/snort.conf
#Offical activate snort device in terminal
snort -c /etc/snort/snort.lua -i eth0
```
	* Utilize static IP for device in snort.lua and utilize proper setup procedures.
* Implemented backup system utilizing "BackInTime"
```bash
#Make sure you have the dependency associated with this software
sudo apt install kali-desktop-xfce
#Install the main backintime software
sudo apt install backintime-qt -y
```
	* Implimented backups everyday at 12:00 AM, will be implimenting root kernal backups at the same time too.
* Added new account profile with restriced non-sudo permissions and directory access
```bash
#Add new guest user with limited permissions
sudo adduser cyberguest
#Give password to cyberguest
donthackme
#Restrict any access to sensitive files
sudo chmod 700 /home/cyberstudent/Backups #Local file backup
sudo chmod 700 /Backups #System Backups
sudo chmod 700 /var/log/ #Disable access to logs except system admin
sudo chmod 711 / #Restrict all read and write access
sudo chmod 770 /home/cyberguest/ #Allow read, write, and execute on local file system
```
* Added SSH protocol to access admin account without needing any degree of a password remotely and communicate securely.
```bash
sudo apt install ssh #Install SSH protocol
sudo ssh-keygen #Utilize key generation application and use default root access, create keys on both local host and remote host
oshardening #Passphrase for key
#Impliment open ssh-server if not impliment already
sudo apt install openssh-server -y
#Enable the service
sudo systemctl enable ssh
#Make sure to disable password login if possible using sshd_config
0342 #Password of admin user
#Setup authenticator files so that certain devices can access the admin account by creating authorized_file

```
	* We can now use this key to make access to host PC utilize SSH, instead of password based loggin in
* Added multifactor authentication utilizing google to provide access to admin account.
```bash
sudo install google-authenticator #Install library for google MFA
google-authenticator #Setup google MFA and scan QR code
#---COPY EMERGENCY CODES---
58931282
48140444
52047776
44869530
40209281
#Agree to built in systems to defend against brute force attacks and update ssh settings.
#Edit LightDM PAM, SSHD files, polkit-1,sudo, or any restricted access systems using
auth required pam_google_authenticator.so nullok
#Restart service to impliment changes
sudo systemctl restart lightdm
```
* Prepare VM for cloud migration
```bash
#Remove VM ware tools
sudo systemctl stop open-vm-tools || true
sudo apt remove -y open-vm-tools open-vm-tools-desktop || true
#Make sure /etc/network/interfaces uses dhcp for server assignment and specify using ethernet
```
	* Utilize "StarWind V2V Converter" to take linux VM and turn it into a compatiable VHD azure can use.
	* Utilize Azure to create a storage account and create blob holding vhd converted Linux Machine
___
\paragraph{Concern 1} Regarding the current VMs that ACME corporation has provided, there are several cybersecurity concerns that need to be addressed in order to utilize these VMs in the cloud. The first order of concern is the lack of RBAC systems. There are no exclusive roles to control which users have admin privileges or restricted access. This poses a significant risk as this oversight can be a serious risk for our ACME virtual machine infrastructure. 
\paragraph{Concern 2} There is also a lack of confidential channels within these VMs. When uploaded to the cloud, data between the local host and the cloud is not encrypted or secure. This can lead to leaks of confidential information that may be critical here at ACME Corporation. Even risking important credentials that are used in ACME Coporation cybersecurity practices.
\paragraph{Concern 3} In addition to unsecured connections between the host and the cloud-based virtual machine. There are no safeguards in restricted admin access from certain machines or accounts. Lack of proper safeguards against unauthorized access may provide bad actors with opportunities to fully take control of the system, posing a significant risk to ACME Corporation.
\paragraph{Concern 4} Another cloud concern is the lack of systems to regularly save data in case of system failure or ransomware attacks. Lack of systems in place to back up VM settings or asset files poses a significant risk to our cloud and on-site data. Systems should be set in place to counter this cybersecurity threat.
\paragraph{Concern 5} There is also a lack of logging or IDS systems in place to find anomalous interactions. Lacking detailed records of network interactions and lost-cloud interactions may cause difficulties in identifying cybersecurity attacks and conducting proper audits. As such, extensive logging systems both on and off the network are required here at ACME corporation.
\paragraph{Concern 6} These operating systems have not been up to date since their creation. Having outdated libraries and operating systems may cause unnecessary risk for the ACME corporation. Ample updating periods and patch checks should be implemented if possible. 
\paragraph{Applied Methods} To address these cybersecurity concerns \textit{before} uploading to the cloud. Operations such as updating and patching the current version of the Kali Linux operating system. Installing firewalls to minimize attack surfaces. Include IDS systems like snort to log and keep track of on-system and network interactions. Utilize backup version controls with tools like "backinttime". Utilize Linux RBAC systems to distinguish between a superuser and a regular guest user. Use SSH protocol to securely communicate with the system to avoid sniffing attacks. Utilize MFA using Google Authenticator to protect against brute force attacks and unauthorized access.
