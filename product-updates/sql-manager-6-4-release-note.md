---
title: SQLDocKit 6.4.0 - Release Note
description: This article describes features and improvements delivered in SQLDocKit 6.4.0
author: Petra Filipi
date: 07/12/2016
---

We have shipped SQLDocKit 6.4! This is a minor release with a lot of new features and improvements.
We’ve been listening closely to all your feedback since our release in August, and as of today you’ll find that SQLDocKit is more powerful than ever!

Product version: 6.4.0  
Build number: 2481  
Release date: Tuesday, December 7, 2016

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)

## Features
* __Inventory SQL Servers from Multiple Domains__ – SQLDocKit now includes the ability to gather complete inventory information from SQL server instances and services across multiple domains. Use multiple credentials to discover all running SQL Servers in any domain, not only in the domain in which your SQLDocKit is installed. We added a dialog that allows you to specify credentials for each of the domains in your environment. If your domains are not trusted, you can define different credentials for any domain you have, so SQLDocKit can impersonate on the non-trusted domain and discover all SQL servers within it. You can also specify a different service account for each domain. SQLDocKit allows you to manage all your domains in a single place and saves you the trouble of logging in to several different servers in multiple domains.
* Discover, inventory and document your entire __SQL Server Business Intelligence (BI) environment__, including SQL Server Integration Services (SSIS), SQL Server Analysis Services (SSAS) and SQL Server Reporting Services (SSRS). [Take a snapshot](#internal/how-to/server-environment-snapshots/take-manual-snapshots) of your server environment, or use the __Live Explorer__ to see these new reports in action.
* The __Role Membership__ report lists all database users, logins mapped to database user accounts, and roles.
* __Document your SQL Agent__ – SQLDocKit now helps you retrieve the complete information related to SQL Server Agent Jobs such as: General and Advanced configuration information, History, Job List, Job Steps and Tasks, Job Names, Enabled\Disabled State for the job and schedule, the list of Schedules created/available with the details (Occurrence, Recurrence, Frequency, etc.), Operators and Alerts.
* Entire SQL Server documentation – including new SQL Server BI and SQL Server Agent reports plus an overview of SQL environment differences – is now exportable to Excel.

## Improvements
* UI improvements, including new headers and icons next to the server types. To help you distinguish servers that have been manually added from those that have been auto-discovered, auto-detected servers now have an orange circle next to the Server Type icon while manually added servers have a blue circle next to the icon.
* Improved Configuration Wizard – which now displays the actions the application performs while configuring all settings.

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)
