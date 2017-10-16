---
title: Compare Wizard
description: This article explains SysKit SQL Manager Compare Wizard and available comparison types.
author: Petra Filipi
date: 18/09/2017
---
Compare Wizard provides the possibility to track SQL Server environment configuration changes and compare different servers and databases. With a couple of easy steps you can view the desired differences and export the result.

* [Entire Snapshots](#internal/docs-sqlmanager/how-to/compare-wizard/compare-snapshots) - compare SQL Server environment settings between two saved snapshots.
* [SQL Servers](#internal/docs-sqlmanager/how-to/compare-wizard/compare-single-sql-server) - compare differences between two SQL Servers in your environment or track the changes that were made to a server over time.
* [Databases](#internal/docs-sqlmanager/how-to/compare-wizard/compare-databases) - Compare and track changes made on the structure of your databases.

    * __Compare Databases With a Previous Snapshot__ - Track all changes on database schema at different points in time. This will compare all the information contained in the snapshot about loaded objects and their settings. This will give you a simple way of determining if any change to the structure of the database happened between the selected dates (eg. a column was added to a table or an index was dropped).
    * __Compare two Different Databases__ - Compare database structure between any two selected databases.

* [Security](#internal/docs-sqlmanager/how-to/compare-wizard/compare-security) -  Compare and track changes to SQL role permissions and user memberships.
    *  __Track Differences over Time__ 
        * __User Differences__ - Check if database users or their role memberships have changed. This can be useful if you want to view differences in database users at different points in time.
        * __Role Differences__ - Track all database role changes on the selected SQL Server. This report will provide an easy overview of any changes to objects that are granted by security roles in selected databases and any differences in permission types on these objects.
    * __Database to Database Compare__
         * __Users Compare__ - Compare database users and their memberships between any two selected databases.
         * __Roles Compare__ - Compare database roles and their securables between any two selected databases.

_Learn more about comparing objects by clicking on the feature you're interested in._

