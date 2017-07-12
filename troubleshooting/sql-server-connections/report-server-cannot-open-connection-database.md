---
title: Report Server Database Unavailable
description: This article describes how to resolve problem connecting report server to report server database in SSRS.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Microsoft.ReportingServices.Library.ReportServerDatabaseUnavailableException: The report server cannot open a connection to the report server database. A connection to the database is required for all requests and processing.
### Solution:
This error indicates that SysKit SQL Manager cannot connect to the underlying Reporting Services database. Make sure Reporting Services are properly configured (use the Reporting Services Configuration Manager to validate your configuration) and make sure that the SysKit SQL Manager account used to retrieve information about this Reporting Services instance has the right privileges to read from the Reporting Services database.