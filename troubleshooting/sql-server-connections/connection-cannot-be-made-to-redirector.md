---
title: A connection cannot be made to redirector
description: This article describes how to resolve SQL Server connectivity issue.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
A connection cannot be made to redirector. Ensure that ‘SQL Browser’ service is running.
### Solution:
This could indicate that your SQL Browser service is not running on the SQL Server or the account that is being used to run the SQL Browser service cannot access the configuration files for Analysis Services. Check out this [MSDN article](https://blogs.msdn.microsoft.com/karang/2013/02/20/connectivity-issue-a-connection-cannot-be-made-to-redirector-ensure-that-sql-browser-service-is-running/) to learn more.