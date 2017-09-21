---
title: SQLDocKit 7.0.0 – Release Note
description: This article describes features, improvements and bug fixes delivered in SQLDocKit 7.0.0
author: Petra Filipi
date: 04/04/2017
---

We are pleased to present the newest version of SQLDocKit!
This is a major release that offers many powerful features, including support for Azure SQL servers and databases, security management, new best practices, and other enhancements.

Product version: 7.0.0  
Build number: 4080  
Release date: Apr 4, 2017

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)

## Features
* SQLDocKit now supports Azure SQL servers and databases, allowing you access to valuable information about your __Azure SQL server environment__, such as server versions, memory, processor info and a list of all databases associated with an Azure SQL server, editions, statuses, logins, roles, created firewall rules at the server and database level, and much more.
To enable access and retrieve data, use the Windows Azure Management Portal or run __sp_set_firewall_rule__ on the master database to create a firewall rule for your IP address. Then, go to the SQL Servers dialog and [add the Azure SQL server](#internal/how-to/add-sql-server/manually-add-sql-server). Take a snapshot, create documentation, or use the Security Management option to view and manage Azure databases.
* The feature you’ve all been waiting for has arrived – __Security Management__! Now you can __grant and revoke server principal permissions__ on multiple database engines and __drop logins__ using the [Security Management Wizard](#internal/security-management/security-management-wizard). But that’s not all – you can also choose to either grant/revoke permissions immediately after finishing the wizard or specify an exact time when these actions will be executed automatically by SQLDocKit Service. The [Scheduled Actions](#internal/security-management/scheduled-actions) dialog lists all the actions that have been scheduled so that you can view all scheduled actions and cancel or delete them if you change your mind.
* Keep your SQL Server environment in top shape by following a number of new best practice reports, such as __Auditing Login Failures__, __Blocked Process Threshold__, and __Virtual Log File Count__. Make SQL Server security your top priority by checking security best practices, such as __Guest Permissions__, __User Password Policy__, and __Users with the Simple Passwords__. To learn more about new best practices, check our [best practices library](https://www.syskit.com/products/sql-manager/resources/sql-server-best-practices-library/).
* We’ve added a new detect option in the [Options Wizard](#internal/get-to-know-syskit-sql-manager/backstage-screen/options-wizard) so that you can now discover not only SQL Servers that you have on your servers but also on workstations. This new option is disabled by default, so be sure to enable it in case your developers have installed multiple SQL Server instances on their machines that you want to monitor.

## Improvements
* SQL Servers dialog UX improvements: checkmarks instead of checkboxes in the grid, a more intuitive arrangement of the toolbar buttons, and a new option to manually add all instances at once (database engine plus all detected BI roles).
* The Refresh button has been added to the Snapshots ribbon.
* The Ignore Best Practice button has been added to the Best Practices Configuration ribbon so that you can ignore the best practices that you don’t want to monitor on your dashboard.

## Bug fixes
* Issue fixed regarding duplicate servers in snapshots and the SQL Servers dialog.
* Corrected an issue in detection of whether a load has finished successfully or not. Before, the application sometimes showed “Failed,” even though all the information was gathered in reports.
The SQL Server Info report is no longer missing information.
* Fixed the default settings in documentation templates. Just general settings are now included in the Simple and Regular template by default instead of all the BI roles reports.
* The Servers List report is no longer selected by default on the SQL Inventory and is now on the Discovered SQL Servers report.
* Now able to detect SQL servers from servers that are not in the domain but in the work group.
* Info release no longer missing; SQL accounts are in the SQL Servers Info.
* Fixed issues with the Database Files and TempDB best practices. The condition from the description was not respected.

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)
