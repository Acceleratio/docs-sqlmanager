---
title: Could not open a connection to SQL Server
description: This article describes how to resolve issue when a network-related or instance-specific error occurred while establishing a connection to SQL Server.
author: Petra Filipi
date: 07/06/2017
---

### Problem:
A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 – Could not open a connection to SQL Server)

### Solution:
SysKit SQL Manager cannot connect to your instance due to one of the following problems:

* TCP/IP or Named Pipes protocols are disabled
* Remote Connections are not enabled
* The firewall is blocking access to the SQL Server, check firewall configuration for the port you are using
* The server is offline. Please make sure your server is online.

For more information, refer to [SQL Server Configuration Prerequisites.](#internal/requirements/sql-server-configuration)