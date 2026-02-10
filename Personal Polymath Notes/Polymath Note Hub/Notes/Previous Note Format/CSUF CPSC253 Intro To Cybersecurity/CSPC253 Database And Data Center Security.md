___
**Data Types**
* Structured: Databases, Tables, 
* Semi-Structured: Tables
* Unstructured: Videos, messages, emails
___
**Data Is The Weakness**
* Data is the Weakest point in any system or organization, this is why we use encryption, and without security Databases will collapse.
___
**Data Base Security**
* Complexity of databases are increasing while security hasn't evolved as quickly.
* There is SQL vulnerabilities
* There is often diverse environments and use of cloud software makes it even more complex.
___
**Database**
* Structured collection of data stored in one or applications.
* Stores relationships between data items and groups of data items.
* **Database Management System:** Used for constructing and maintaining the database.
___
![[005__01__CH05_Ch22_COMBINED.pdf]]
___
**Relational Databases**
* Table of data consisting of rows and columns that often has components that reference to other tables.
* Primary ID has to be completely unique.
* The VIEW provides a way to see data that's within the scope of the table system/database; data is not changed!
___
**Relational Database Elements**
* View/Virtual Table (Result of query)
* Primary Key: A unique key that represents a row
* Foreign Key: Attributes
* Formal Name: 
* Relation
___
**Structured Query Language (SQL)**
* Used to modify or query the data of a database.
	* Create Tables
	* Insert and delete data in tables
	* Create Views
	* Retrieve data with query statements
___
**SQLI**
* SQL injection refers to an attack where a cybercriminal attempts to use an input filed to write and run malicious SQL statements.
* Allows the malicious actor use an input field to access a database without having proper authentication.
	* Targets data exactly using sequel commands.
	* Used in bulk extraction of data.
* Can modify or delete data, execute OS system code, launch DoS attacks.
___
**Injection Technique**
* Goes through a text string and add "--". to make a certain piece of code as commented.
* This is useful for hackers as it allows to bypass password or other authentication methods to access data.
___
**Authorization Tables**
* Stores data that regards what users can have what access.
* **Principle Of Least Privilege:** Only certain permissions are given based on how much a user needs.
___
**Database Access Control**
* Determines the access level of the user and if they can create, insert, delete, update, read, write, etc.
* **Centralized Administration:** An admin cannot edit but can access who or what accesses the data.
* **Ownership-Based Administration:** Create of a table can edit the resource.
* **Decentralized Administration:** May grant or revoke authorization.
___
**SQL Access Controls**
* **RBAC:** Create and delete roles, define permissions for the role, assign and cancel assignment of users to roles.
___
**Categories Of A Database:**
* **Application Owner:** End user who owns database objects
* **End User:** Operates on database objects
* **Administrator:** Takes responsibility for everything in the database.
___
**Database Encryption**
* Encryption is only worth it for uber sensitive data.
	* Can be applied in various different methods.
* Key management may be too heavy to manage and increases in complexity.
___
**Data Center Security**
* Houses databases and has many redundant systems to maintain the accessibility of the database.
___
**Data Center Security Model**
* Encryption, Password Policy, etc.
* Network Security
* Physical Security
* Site Security
___
**TIA-492**
* Specifies the minimum requirements to secure a data center.
___
