---
title: Upgrade to the Latest Version
description: This article explains how to upgrade SysKit SQL Manager to the latest major version.
author: Tomislav Sirovec
date: 12/6/2017
---
This article explains how to upgrade SysKit SQL Manager to the latest major version. The SysKit SQL Manager database, snapshots and application settings will be preserved by the upgrade.

### Preparation

1. The account running the application should have __db_owner__ privileges on the SysKit SQL Manager database for the upgrade to be successful. If you are also changing the SysKit SQL Manager Service account to one that is different from the account that was assigned to the previous application version, the account running the upgrade should also have the __securityadmin__ role on the preferred SQL Server. This role will allow the account to [grant the right privileges to the new service account](#internal/requirements/user-permission-requirements/).
2. __Back up the database__ before proceeding with the upgrade, especially if upgrading to the latest version of SysKit SQL Manager.

## Instructions

1. [Download](https://www.sqldockit.com/download/) the application.
2. The __Installation Wizard__ will inform you that the previous version will be __uninstalled automatically__.
3. Click __I Accept the terms of the license agreement__ to accept the license and then click __Next__ > to proceed.
4. Choose the installation folder, e.g. __C:\Program Files\Acceleratio\SysKitSQLManager__.Click __Next__ > to proceed.
5. Select the location for the application shortcuts and the preferred availability option (__Anyone or Only me__). Click __Next__ > to proceed.
6. The Installation Wizard will unpack your files and you will be able to run the application from: __Start__ > __All Programs__ > __SPDocKit__. If you check Run __SysKit SQL Manager now__ then the application will start automatically when you click __Finish__.
7. The __Configuration Wizard__ window will appear and ask if you want to use the same settings as before. Leave __Yes, use the same settings__ checked and click __Next__ to continue.
8. Confirm that the credentials for the __Service Account__ are correct and click __Next__ to finish the wizard.

## Tips&Tricks

If during the installation you encounter any problems and wish to enable logging to help you resolve the problems, you can start the installation using the command prompt with the following argument :

* /l=”full path” will create a log file in the specified location.
* /log will create a log file in the installation directory.
Note that this will work for both .exe and .msi installation files.