---
title: User Permission Requirements
description: This article lists all of the required privileges to load the SQL Server settings using SysKit SQL Manager.
author: Tomislav Sirovec
date: 06/06/2017
---
# User Permission Requirements

SysKit SQL Manager is a completely agentless install. Only a single instance of SysKit SQL Manager must be deployed in your environment in order to document all the SQL Servers in your organization. In order to do so, you must make sure your system has been properly configured.

There are two modes of taking a snapshot with SysKit SQL Manager. You can do so “manually” from the UI; in this case, the SQL discovery and data gathering will be performed through the user that is currently logged in. The other approach is to configure a service to create automatic snapshots on predetermined schedule. In the latter case, the SQL discovery and data gathering will be executed through the defined service user. Unless otherwise specified, both users are required to have all the privileges listed further in this article.

To run SysKit SQL Manager and retrieve all the SQL Server settings you want to document, the user needs to have proper privileges. Here is the list of required privileges to load the SQL Server settings:

1. __Local Administrators__ group on every machine. (required to retrieve the information about RAM, processors, disk space and other)
2. Sysadmin SQL Server role on all monitored SQL Servers
3. Special privileges for the __Service Account__. (Service account needs to have the privileges listed above along with the __Log on as a Service right__.)

### Instructions

Follow these steps to give a user these privileges:

1. To add a user account to the __Local Administrators__ group
  * On the server, click __Start__, right-click __Computer__ and then click __Manage__.
  * Navigate to __Configuration__, expand __Local Users and Groups__, and then click __Groups__.
  * Right-click the __Administrators__ group and then click __Add to Group__.
  * In the __Administrators__ Properties dialog box, click __Add__.
  * In the __Select User__, Computers, or Groups dialog box, type the account name on which you want your worker process to run (for example, DomainName\__YourAccount__) in the __Enter the object names to select__ box and then click __OK__.
  * In the __Administrators__ dialog box, click __OK__.
  * Close the __Server Manager__ screen.
2. To give a user account a __SQL Server sysadmin role__:
  * Connect to the SQL Server using SQL Server Management Studio.
  * Under Security, go to Logins, find the desired user, and right-click Properties.
  * Under Server Roles, make sure sysadmin is checked and click __OK__.

### SysKit SQL Manager database requirements

#### Creating a new database

To create a new SysKit SQL Manager dedicated database, the user account running the installation and configuration wizard (i.e. the install account) should be granted __dbcreator__ and __securityadmin__ roles on the preferred SQL Server. This allows the account to create a new database and assign proper privileges after creation. The install account will be automatically given __db_owner__ privileges on the newly created database if possible. Otherwise, the account should be given that privilege manually, because it is needed to upgrade the database.

#### Privileges required to run the application

These privileges will be granted automatically when a new SysKit SQL Manager database is created or during a database upgrade.

* The SysKit SQL Manager service account needs to be granted __SPDocKit_service_role__ role in the SysKit SQL Manager database. This role will give the member of the service account __db_datawriter__  and  __db_datareader__ roles and grant __execute__ permissions on all the stored procedures in the database.
* The account running the load from the SysKit SQL Manager console must have the same privileges as the SysKit SQL Manager service account (see above).

### Active Directory Permissions

If you plan to use the Auto-discovery feature, the user that is creating a snapshot must have the ability to read objects (computers) from the Active Directory. If the user does not have read privileges on the entire directory, you can choose to discover objects only within a predefined set of Organizational Units.

This permission is required so that we can gather all the computers in your organization. Apply OU filtering if you would like to discover SQL Servers only on a particular set of computers in your organization.

### Windows Server Privileges

The user running the tool must to be part of the local Administrators group on each computer that has the SQL Server installed. This privilege is required in order to obtain the list of installed SQL Server instances, components, and statuses.

If you are running the tool for the first time and would like to perform an initial discovery of all SQL Servers in your organization, we would recommend running the tools as a Domain Admin user.

### SQL Server Privileges

The user running the tool must have a sysadmin role on each SQL Server and instance in order to retrieve information about SQL Server configuration, system, and user databases. When a new SQL Server is discovered, the user will be alerted if information about its settings could not be retrieved.
 
 #### Additional resources

* [Connect to SQL Server When System Administrators Are Locked Out](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out)
* To grant yourself admin access over SQL Server, use the [Add User to Sys Admin script](https://github.com/Acceleratio/SQLScripts/blob/master/AddUserToSysAdmin.bat
).
