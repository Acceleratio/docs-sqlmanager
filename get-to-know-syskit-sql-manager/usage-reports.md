---
title: Usage Reports
description: This article explains how to use SQLDocKit usage reports to track SQL Server database status, disk usage and database sizes.
---

SQLDocKit reports cover usage, namely disk usage and database sizes.

__Disk Usage:__ This report displays disk usage over time. It has a forecast option to estimate disk usage, and it uses current trends to help you manage disk growth in the future.

__DB Size:__ This reports tracks database size over time. It has a forecast option to predict the size of databases using current trends, and it helps admins manage database growth more easily.

__Logs Size:__ This report displays the size of database logs over time. The forecast option can be used to predict database log sizes based on previous usage.

__Storage Metrics:__ This report tracks the storage space used by SQL Server. With this report, you can view a database’s size relative to the total space used on the SQL Server to find larger logs right away.

__Orphaned Databases:__ This report lists all the databases with orphaned owners. For example, databases with owners who have been disabled in or deleted from the AD.

__Unused Databases:__ This report tracks databases that have not been used in a long time based on the data of the last read/write activity. Note that the time range resets each time you restart a SQL Server.
 
Visit [Report Examples](https://www.sqldockit.com/resources/report-examples/) to see what these reports look like when they have been exported.