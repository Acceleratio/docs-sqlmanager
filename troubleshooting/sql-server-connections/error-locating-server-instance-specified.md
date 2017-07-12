---
title: Error Locating Server/Instance Specified
description: This article describes how to resolve issue when locating server/instance specified error occurred while establishing a connection to SQL Server.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: SQL Network Interfaces, error: 26 – Error Locating Server/Instance Specified)


### Solution:
If you are using named instance on a port other than the default, make sure SQL Browser is running, or configure the custom port in the SysKit SQL Manager UI.

