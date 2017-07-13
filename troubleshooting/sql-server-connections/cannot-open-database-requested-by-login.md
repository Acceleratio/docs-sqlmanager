---
title: Cannot open database “model” requested by the login
description: This article describes how to resolve the issue when trying to connect to SQL Server with the account that is not allowed to connect to SQL Server.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Cannot open database “model” requested by the login. The login failed. Login failed for user ‘CONTOSO\walterwhite’.

### Solution:
The user running SysKit SQL Manager and creating a snapshot must be sysadmin on the SQL Server in order to retrieve info from user and system databases.

For more information, refer to [User Permission Requirements](#internal/requirements/user-permission-requirements).