---
title: Manage Domains and Credentials
description: This section describes how you can add multiple domains and credentials in SysKit SQL Manager.
author: Petra Filipi
date: 11/07/2017
---
This section will show you how you can add multiple credentials and multiple domains so that SysKit SQL Manager can auto-discover servers from multiple domains.

## Manage Domains
Follow these steps to manage domains which SysKit SQL Manager will use when loading server data:

1. Navigate to the __Backstage Actions Screen__ and click the __Administration__ button.
2. Click the __Add Domain__ button.
3. Specify a __Domain__ or __Domain controller__ or choose to use your current domain.
4. Select the credentials.
    * You can use the __Current Account__ option (credentials of the user who runs application), __Specify Service Account__ or __Specify Credentials__ you want.
    * Specified credentials will be added to the __Credentials List__ where you can view and manage the credentials that SysKit SQL Manager will use when loading server data and taking snapshots. 
    * Click the __Edit__ button next to the __Specify Service Account__ option to view and manage credentials.
    * Click __Test Credentials__ to test your credentials.
5. Discover servers from entire domain or choose the Specific Organizational Units from which you want to discover servers.
6. Click OK.
7. Follow steps 2-6 to add multiple domains and credentials.

## Manage Credentials
Follow these steps to manage credentials which SysKit SQL Manager will use when loading server data:

1. Navigate to the __Backstage Actions Screen__ and click the __Administration__ button.
2. Click the __Add Credentials__ button.
3. Choose an __Authentication mode__ (Windows Authentication or SQL Server Authentication)
4. Enter your desired __Display name__, __User name__ and __Password__.
5. Click __Save and Close__.