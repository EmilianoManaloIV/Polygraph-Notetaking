---
NoteType: Annotations
NoteCreation: 2026-02-04
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 332 - Introduction To File Systems And Databases]]
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
___
## Creating User Accounts
* Lets create an Admin account other than a root users!
* Administration -> Add Account
* Select a name that you want to use for this account (utilize sha2 password hashing)
* Utilize "localhost" to what is limited
* Administrative Roles
	* Use a predefined role combination to best serve your interaction with the database.
* Now you can add a new connection with the account
___
## Hostnames And Wildcards
```MySQL
#Create a user 
CREATE USER 'name'symbol'host'
#How to dictate how a user logged in
#Returns a user utilize host
SELECT CURRENT_USER()
#Returns a host utilizing a user
SELECT USER()
```
___
## Database Access Privileges
* Login into a certain account and create a new user of your own volition, depending on the privilege.
* **Schema Privileges**: Limits what database can and cannot be used
	* It also limits read and write access
___
## Access Roles
* A method to create predefined layers of permissions, by creating them in the query
```MySQL
#Gives all permissions to the album database
CREATE ROLE 'app_dev'
GRANT ALL album.* TO 'app_dev'

#You can also create users at runtime with a given password
CREATE USER 'read1'@'LocalHost' IDENTIFIED BY 'temppass'
#Grant permissions
GRANT 'app_dev' TO 'read1'@'localHost'
```
* You can login with multiple users within the MySQL system.
```MySQL
#Activate the role to other connections
SET DEFAULT ROLE 'app_dev' to 'read1'@'localHost'
```
* Status and system variables, you can change the persistent data within the server system.
* Delete a given user within a query
```MySQL
#Remove a user
DROP USER 'read1'@'localhost';
#Remove a role
DROP ROLE 'app_dev','app_write';
```
___
## Password Expiration
* How to expire the password of a given account
```MySQL
#How to expire a password using a database query
ALTER USER 'tempurser'@'localhost' PASSWORD EXPIRE INTERVAL 90 DAY;
```
* You will need to create a new password to help support security policies.
___
## MySQL Storage Engines Overview
* **InnoDB**: Default system
* **MyISAM:** Index sequential based
* **Memory:** Great for temporary objects
* **CSV**: Comma separated values for importing and exporting
* **BLACKHOLE**: Helps with local data systems
* **Archive:** Great for archival information
* **Merge:** Creates a merge operation between ISAM values
* **Performance Schema:** Used to monitor the server at an internal level
* **Federated:** Utilized for clustering systems.
---
## The CREATE TABLE statement
```MySQL
#Show the asscoiated storage engines with your database
SELECT talbe_name, engine FROM information_schema.tables WHERE table_schema = 'scratch'
```
* How to create a table for your selected database and what storage engine it should use
```MySQL
CREATE TABLE testTable (
id INT AUTO_INCREMENT PRIMARY KEY,
cname VARCHAR(128),
localname VARCHAR(128))
)
```
___
## InnoDB
* Rock Locking
* Foreign Key Constraints
* Multi-Version Concurrency Control
___
## MyISAM
* Old version of the engine to keep legacy systems active
* Indexed Sequential Access Method
* **No** transaction and foreign keys
* More important to read than to write (efficiency constraints)
___
## Memory Storage Engine
* Temporary storage or caching data
* If program stops, data will be lost 
* Limited memory scope and fixed state
* Cannot store strings.