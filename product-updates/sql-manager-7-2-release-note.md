---
title: SysKit SQL Manager 7.2.0 - Release Note
description: This article describes features, improvements and bug fixes delivered in SysKit SQL Manager 7.2.0
author: Petra Filipi
date: 01/09/2017
---

We are proud to present a new, refreshed version of  __SysKit SQL Manager__, which comes with a new name and logo! We felt like a change and, with a move to new office space, we decided we might do a bit more than just remodeling and changing of our address. In the rebranding process, we’ve gone all out by changing the company name, logo, and names of all our products. 

Our company name has been changed from __Acceleratio__ to __SysKit__! We’ve also renamed our SQL server documentation tool, from SQLDocKit to SysKit SQL Manager. You can read the back story to these changes in the [Rebranding Announcement]() blog post. 

Product version: 7.2.0
Build number: 5074
Release date: Friday, September 1, 2017

[Click here to download the new release.](https://www.syskit.com/products/sql-manager/download)

## Features
* Check out the new report, a graphical representation of all tables participating in at least one foreign key relationship. The  __Table Dependencies Graph__ displays foreign key connections between all tables so you can easily review database structure, detect tables with a large number of foreign key references, and track foreign key paths linking the tables, which can be helpful while analyzing the results of the ON DELETE CASCADE option.  
* Before, we introduced you to the SQL Server Database Objects documentation feature. Now, we also support  __Azure SQL Database Objects Documentation__, which provides deeper insight into your Azure SQL database environment by documenting not only the databases, but all the __Azure SQL Server Database Objects__, including tables, views, functions, stored procedures, and table indexes in a single document. 
* SysKit SQL Manager is now able to recognize  __SQL Clusters__ and __Nodes__ that belong to a given cluster. If you have implemented __Failover Clustering__, now you can explore new reports that show you a complete overview of your clustered environment from a single UI: 
    * __General__ – Shows general information about your clustered environment, such as Qourum Type, Owning Node and Shared Drives.
    * __Nodes__ – Shows all nodes that belong to the selected failover cluster and their states.
    * __Disk Partitions__ –  Shows disk partitions information such as Volume Label, Path, Total Size and Free Space.
    * __Network Interfaces__ – Shows network information, IP Addresses and States.
    * __Resource Groups__ – Shows all resource groups, Owner Nodes and States.
    * __Resources__ – Shows all resources, Owner Groups, Owner Nodes, Types and States. 

## Improvements
* You may notice a few visual changes following our rebranding – __SysKit SQL Manager__ now has a new name, skin, logo, and splash screen!
* More information about SQL Server __Always On__ is now available. Use the new Always On __Replicas Performance__ report to monitor performance for Always On Availability Groups, __Synchronization Performance__, __Estimated Recovery Time__ and more

## Bug fixes
* Fixed Run now option at the end of configuration wizard.
* In some cases, index size and data size in database objects reports were not well-calculated. 
* Some statistics in the Statistics report were missing from snapshot.
* The Best Practices Dashboard was not reflecting the correct result from the SQL Server Job Owner best practices report.  



[Click here to download the new release.](https://www.syskit.com/products/slq-manager/download)
