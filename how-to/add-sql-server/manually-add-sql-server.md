---
title: Manually Add SQL Servers
description: This section describes how you can manually add SQL servers in SQLDocKit.
author: Petra Filipi
date: 12/6/2017
---
This section describes how you can manually add SQL servers in SQLDocKit.

## Add an SQL Server

1. Navigate to the __Backstage Actions Screen__ and click the __SQL Servers__ button.
1. Click the __Add__ button.
1. Choose __Server type__ (Database Engine, Analysis Service, Integration Services, Reporting Services, Azure or All detected instances) and enter the __Server name__.
1. Specify credentials.
   * The currently supported authentication types are Windows Authentication and SQL Servers Authentication for Database Engine.
   * Analysis Services, Integration Services, and Reporting Services only support Windows Authentication.
  * Azure only supports SQL Server Authentication.
1. Click __OK.__

__Note:__ Manually added SQL Servers will have an orange circle next to the Server Type icon in the SQL Servers grid so you can easily distinguish them from auto-detected servers, which will have a blue circle next to the icon.