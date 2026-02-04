---
NoteType: Annotations
NoteCreation: 2026-02-04
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[Landing Page]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Origins
* Open source and works on several different operating systems.
* Most cloud providers utilize SQL for their systems.
* Its fully api-compatible, allowing flexibility to be used in already existing database systems.
___
## Installing Community Server On MacOS
* Check system preferences to determine mySQL isn't running or existing.
* Download mySQL from the website on the mySQL website. (Community Addition)
	* Community Server
	* MySQL Workbench
	* Use mac executable
* Create a permanent root user server password and install the community server.
```bash
sudo ln -s /usr/local/mysql/bin/mysql /usr/local/bin
password:
mysql 
mysql -u root -p
Enter password:
show databases
```
___
## Installing mySQL Workbench On Mac
* Same process when downloading the server onto your device.
* Configure the preferences and uncheck "safe-updates" so that you can teach yourself.
* Access your instance of the server and navigate the editor.
```MySQL
SHOW DATABASES;
```
___
## Installing MySQL Server On Windows
* Install MySQL server community edition onto your system
* Use Custom Setup and install what you want, such as the server, workbench, documentation, and samples.
* Utilize the standalone server, not the cluster
* Use strong password encryption and set a root user password
* Utilize this as a windows service and make a default program startup for windows.
* Pin the unicode terminal MySQL interface
___
## Configuring MySQL Workbench On Windows
* Make sure to turn off safe-updates
* Utilize your instance and client of the root password
___
## Installing Example Databases
* Schemas are used as databases, but also serve as schemas, which is a little confusing.
```MySQL
#Ctrl + Shift + Enter = Execute Command
```