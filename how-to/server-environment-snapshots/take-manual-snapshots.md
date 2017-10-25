---
title: Take Manual Snapshots
author: Petra Filipi
description: This article explains how administrators can take manual snapshots of the SQL Server environment.
date: 14/06/2017
---
This section describes how you can use the SysKit SQL Manager Snapshot wizard to collect SQL Server environment settings settings. Please note! Adjustments and settings you make using this wizard apply to the current snapshot-taking process only. If you wish to configure a default snapshot-taking setting, use the Options wizard. The selection you make there will be used as a default load template.

1. Navigate to the __Backstage Actions Screen__ and click the __Take Snapshot__ button.
1.	Select the snapshot mode you wish the application to execute. There are three choices:
    * __Default__ – Performs a load using the setup provided in the Snapshot Options and Load Target. This includes server information, database engine settings, database role memberships, database object details (basic information about tables, views, programmability object in database), SQL Server Agent, Analysis Services, Integration Services, Reporting Services and can be changed by the user at any time in the Options Wizard.
    * __Custom__ – Allows the user to specify exactly what information should be loaded It can be the fastest load option if the user wishes to have access only to specific data, and is aware what data he is interested in. This mode is recommended for more advanced users who are looking to generate specific reports.
    * __Full__– Performs a load that collects all available information. This is the recommended load mode if you don’t mind waiting and want to be sure you have all the data once the load finishes.
__Please note!__ What you choose to take a snapshot of, within the Custom mode, applies only to the current load and does not affect loading executed by the SysKit SQL Manager service.
3. Choose what you would like to load. This page is only available if you have chosen the Custom mode; otherwise it will be skipped together with the Target page.

You can use the load performance slider to switch between low resource usage and a high-performance load.

4. Select the snapshot target.
Again, this step will be skipped unless you chose the Custom snapshot mode.
5. Click Next and the loading will start. Wait for the SysKit SQL Manager wizard to finish, then environment settings and reports will be ready for use!