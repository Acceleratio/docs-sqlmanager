---
title: Login failed for user 'CONTOSO\walterwhite'
description: This article describes how to resolve issue when a network-related or instance-specific error occurred while establishing a connection to SQL Server.
author: Petra Filipi
date: 07/6/2017
---

### Problem:

Login failed for user _‘CONTOSO\walterwhite‘_.

### Solution:

The user running SysKit SQL Manager and creating a snapshot must be sysadmin on the SQL Server in order to retrieve info from user and system databases.
For more information, refer to [User Permission Requirements.](#internal/requirements/user-permission-requirements)
