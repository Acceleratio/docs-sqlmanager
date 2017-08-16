---
title: SQLDocKit 7.1.0 - Release Note
description: This article describes features, improvements and bug fixes delivered in SQLDocKit 7.1.0
author: Petra Filipi
date: 20/06/2017
---

We have shipped SQLDocKit 7.1.0. This is a minor release that brings documentation for SQL Servers Always On Availability Groups and database-level objects, as well as some bug fixes and improvements.

As always, we’d be pleased to [hear your thoughts](https://www.syskit.com/contact-us) on these new features.

Product version: 7.1.0  
Build number: 4870  
Release date: Tuesday, June 20, 2017

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)

## Features
* Having __SQL Server Always On Availability Groups__ implemented gives you more flexibility and more granular control over your environment and helps you achieve high-availability requirements and eliminate single points of failure. SQLDocKit now gives SQL administrators this in-depth information on Always On Availability Groups. We have extended SQLDocKit documentation to support these groups so you can keep track of your replicated environment: __availability groups, primary and secondary databases__ (synchronization state, health, database state), __availability replicas, roles, availability group listeners__ (subnet, IP address, listener port, state), and __availability modes__. Check the new reports, and ensure that your environment is correctly configured. Examine the possible failover modes. Determine when the last failover or last switchover happened and analyze the reason. Easily identify databases that fail over together and much more. All the documentation can be exported to .docx or .xlsx format for further examination.
* Get deeper insight into your SQL database environment by documenting not only the databases, but all the __SQL Server Database Objects__, including tables, views, functions, stored procedures, and table indexes in a single document.
    * __Tables__ – Now you can document all tables (including size, column names, data type, and length) in all databases.
        * __Columns__ – List all columns in all tables in all databases on the server instance.
        * __Keys__ – Retrieve primary and foreign key information. Determine what columns are in the primary key and identify foreign key constraints.
        * __Constraints__ – Check all constraints, their types, and definitions.
        * __Triggers__ – Document database triggers, their types, and execution order.
        * __Indexes and Index Columns__ – Get all indexes, index type, space used, index fill factor, fragmentation, and detailed information about index columns such as sorting order, identity, data type etc.
        * __Statistics__ – Identify SQL Server table statistics. View statistical information about the distribution of values in one or more columns of a table or an index.
    * __Views__ – Check out all the details of database views.
        * __Columns__ – List all columns in all views in all databases on the server instance.
        * __Triggers__ – Document triggers that are defined on a view, their types, and execution order.
        * __Indexes__ – Get all indexes, index type, space used, index fill factor, fragmentation, and detailed information about index columns such as sorting order, identity, data type etc.
        * __Statistics__ – Identify SQL Server index view statistics.
    * __Programmability__ – Check out the __Programmability__ and __Parameters__ reports to get detailed information about stored procedure and function parameters. Generate a full parameter list for all SQL Server stored procedures and functions. Analyze the parameters and the associated data types.
    * __Security Roles__ – Get a list of all __security roles__, __role members__, and __role mappings__ for all databases. Check all __role securables__ along with all permissions for an associated role.
* New built-in __best practices__ reports have been added to SQLDocKit. Avoid poor system performance by following new configuration best practices. The __SQL Server Max Memory__ report shows the percentage of memory assigned to an SQL Server and checks whether the operating system has memory available. Running different services under the same account is considered a security risk. The __Different SQL Service Account__ report checks whether separate accounts are used for different SQL Server services. Visit our [Best Practices Library](https://syskit.com/products/sql-manager/resources/sql-server-best-practices-library/) to check the full list of available best practices reports.

## Improvements
* We added some UX enhancements to the SQL Servers dialog: tooltips explaining the button actions, new icons, and a warning in case the autodetect option is enabled. Also, the Monitoring Status column takes the place of the Excluded from Snapshot column for a more intuitive user interface and easy identification of the servers you monitor.
* It’s now possible to exclude/include just one instance from/in the snapshot, and Security Management is enabled, instead of excluding/including the whole server.
* Currently processed servers are now displayed during the detection process in the Progress form.
* We added smaller design updates and UX enhancements to the Loading Progress step in the Snapshot Wizard.
* You can now see how long it took for SQLDocKit to take a snapshot of your environment with the Load Duration column in the Snapshots tab.
* Now, you can track what the SQLDocKit Service is doing in the background. We’ve added its status details in the lower right corner.
* Source and target server names will now be visible in the Compare Wizard exported results.
* Snapshot Options UI has been redesigned. New load options have been added and arranged in a more logical order.
* The TempDB Files Configuration best practice is now improved, with a new description and a Learn More link.
* A tooltip button was added to the Enable Detect on Workstations option.
* Tooltip text was added to the Number of Required Licenses below the SQL Servers grid.
* The mouse pointer now changes to a hand when moving over the License Details section.

## Bug fixes
* Now you can add more logins with different passwords and display names. Before, you could not use the same login with different passwords for different servers because the first login was overwritten.
* SQLDocKit wasn’t correctly detecting running SQL services in some cases. Before, there were only checks for Database Engine, so BI services could be wrongly detected as not running. Now, additional checks have been added for running SQL services during the load progress.
* The use of integers instead of unsigned integers meant that servers with a port greater than 32,767 could not be added. Now, the port number is an unsigned 16-bit integer, so up to 65,535 is available for assigning port numbers.
* A problem with scheduling security management actions with names that are too long has been resolved. Before, actions with long names failed.

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)
