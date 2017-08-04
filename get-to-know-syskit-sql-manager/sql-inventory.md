---
title: SQL Server Inventory
author: Iva Novoselić
description: This article describes what SQL Server Inventory includes.
date: 13/06/2017
---

SysKit SQL Manager crawls your entire domain and gathers information about all your servers. Once it creates a snapshot of the environment, SQL Inventory includes all the details you need for successful SQL Server management.

## SQL Server

__Discovered SQL Servers__: This report lists all discovered SQL Servers, as well the servers on which SQL Server instances are running, their load status, the last load errors, and a help link.

## Database Engines

__SQL Server Info__: This report displays details for each SQL Server discovered in your domain. It contains information about the SQL Server’s name, version, release, SQL account, and whether it’s part of a SQL Server cluster.

__General Settings__: This report displays data for different property categories such as the use AWE to allocate memory, minimum and maximum server memory in MBs, index creation memory in KBs, and minimum server memory per query in KBs.

__Memory__: This report displays data for different property categories such as the use AWE to allocate memory, minimum and maximum server memory in MBs, index creation memory in KBs, and minimum server memory per query in KBs.

__Processors Info__: This report displays information about SQL Server processors. It contains values for the automatically set processor affinity mask for all processors, the automatically set I/O affinity mask for all processors, the maximum worker threads, boosts to SQL Server priority, and Windows fibers (lightweight pooling).
  * Processors Affinity: This report displays running processors and their configured values, as well as the running I/O affinity and configured values for each server core.

__Security__: This report displays values for each discovered SQL Server based on server authentication. It also shows login auditing, whether the server proxy account is enabled, proxy account status, whether Common Criteria compliance is enabled, whether C2 audit tracing is enabled, and the cross-database ownership chaining status.

__Connections__: This report gathers information about the maximum number of concurrent connections, usage of the query governor to prevent long-running queries, the query governor cost limit, whether remote connections are allowed on a particular server, the remote query timeout, and whether it requires distributed transactions for server-to-server communications.
  * Default Connection Options: This gathers running and configured values for settings such as default constraint checking, implicit transactions, cursor close on commit, ANSI warnings, ANSI padding, ANSI nulls, arithmetic ignore, quoted identifier, no count, ANSI null default on, ANSI null default off, contact null yields null, numeric round abort, and xact-abort.

__Database Settings__: This report gathers insights such as the default index fill factor, default backup media retention (in days), compressed backup, internal recovery (in minutes), database default data location, database default log location, and database default backup location.

__Advanced Settings__: This report lists information such as whether contained databases are enabled, the FILESTREAM access level, the FILESTREAM share name, whether triggers to fire others are allowed, and values for the blocked process threshold, the cursor threshold, the default full-text language, the default language, full-text upgrade option, the max text replication size, optimize for ad hoc workloads, scan for startup procs, two-digit year cutoff, network packet size, remote login timeout, cost threshold for parallelism, locks, max degree of parallelism, and query wait.

__SQL Service Accounts__: This report lists the service accounts on each SQL Server in the domain as well as the usernames.

__Logins & Roles__: This report lists the login name, login type, and permission to connect status. It also gathers information whether users are members of the following role groups: bulk admin, DB creator, process admin, security admin, setup admin, and sys admin.

## Databases

__Database List__: This report lists all the databases and provides additional details about the databases, such as the owner, when the database was created, its size, its compatibility level, whether it is a read-only database, its status, its recovery model, the database ID, when the last backup was performed, its space used in %, when it was last used, its owner status, and the number of days since the last backup. Explore and document the whole structure of your SQL Server databases. Use __Tables__, __Views__, __Programmability__, and __Security Roles__ reports to discover more about database objects in your environment.

__Database Files__: This report tracks databases on each SQL Server in the domain and gathers information about the database’s online status, file growth value, file size in MBs, max file size, file path, and database ID.

__Temporary Database__: This report lists SQL Server sizes in MBs and shows the recovery model, read response time in ms, and write response time in ms.

__Temporary Database Files__: This report displays the database name, file type, online status, file growth, file growth value, file size, max file size, file path, write response time, and read response time.

__Model Database__: This report displays SQL Servers and information about their recovery models.

__Model Database Files__: This report displays the database name, file type, file growth, file growth value, initial size, and file path for a particular SQL Server.

__Role Membership__: This report lists all database users, logins mapped to database user accounts, and roles.

## SQL Server Agent

The __SQL Server Agent__ reports give you complete information about SQL Server Agent jobs such as general and advanced configuration information, histories, job lists, job steps and tasks, job names, enabled/disabled state for each job and schedule, schedules created and available with details (occurrence, recurrence, frequency, etc.), operators, and alerts.

## Analysis Services

__Analysis Services__ is an online analytical data engine used in decision support and business analytics. It provides analytical data for business reports and client applications such as Power BI, Excel, Reporting Services reports, and other data visualization tools. SysKit SQL Manager provides general information about your analysis services, language/collation, roles, members, and reports on all Analysis Services databases (properties, data sources, data source views, cubes, dimensions etc.).

## Integration Services

The __Integration Services__ reports list all the service accounts as well as the usernames displayed in the __Service Account__ report. The __Packages__ report lists all packages (their location, version-related information and a root folder) deployed in the MSDB database on your SQL Server.

## Reporting Service

__Reporting Services__ is a server-based solution for building enterprise reports that draw content from a variety of relational and multidimensional data sources. It publishes reports that can be viewed in various formats, and centrally manages security and subscriptions. SysKit SQL Manager provides reports with general information about your reporting services, configuration, properties, reports, folders, and servers.

## Azure

SysKit SQL Manager provides valuable information about your __Azure SQL server environment__, such as server versions, memory, processor info and a list of all databases associated with an Azure SQL server, editions, statuses, logins, roles, created __firewall rules__ at the server and database level, and more.

## Always On
Keep track of your availability groups, primary and secondary databases (synchronization state, health, database state), availability replicas, roles, availability group listeners (subnet, IP address, listener port, state), and availability modes.

## Failover Cluster
SysKit SQL Manager is able to recognize __SQL Clusters__ and __Nodes__ that belong to a given cluster. If you have implemented __Failover Clustering__, you can explore reports that show you a complete overview of your clustered environment: General Information, Nodes, Disk Partitions, Network Interfaces, Resource Groups and Resources.

## Servers

__Servers List__: This report lists servers in the domain, server OS, memory in GBs, number of processors, number of cores, IP address, FQDN, and system drive.

__Local Admins__: This report displays the server administrators in the server environment.
Processors Info: This report gathers detailed information about server processors, such as the device ID, name, max clock speed in GHz, number of cores, and CPU manufacturer.

__Disks List__: This report gathers detailed information about disk usage per server, such as the device ID, name, volume name, size in GBs, free space in GBs, block size, and starting offset.

__Available Windows Updates__: This report shows available updates listed per server and provides you the update ID, title, severity, whether the updated is mandatory, and whether it was downloaded.

__Programs List__: This report gathers information about all the programs installed on a particular server. It contains data such as the program name, version, publisher, install date, install location, a help link, and whether the program was updated.

Check out how some of these reports look like when exported: [Report Examples](https://www.syskit.com/products/sql-manager/resources/report-examples).
