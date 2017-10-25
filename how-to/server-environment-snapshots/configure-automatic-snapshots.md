---
title: Configure Automatic Snapshots
description: This article explains how administrators can configure a schedule to create automatic server environment snapshots using SysKit SQL Manager.
author: Petra Filipi
date: 26/06/2017
---

SysKit SQL Manager allows administrators to configure a schedule to automatic SQL Server environment snapshots. Once configured, the SysKit SQL Manager Service can save your environment settings send report subscriptions and alerts to selected users, document libraries, or network locations.

1. Navigate to the __Backstage Configuration Screen__ and click __Configure__.
1. Skip to the __Service Settings__ option, select the __Enable Service__ checkbox and type in the service account details. Click __Validate Account__ and then __Next__ to continue.
3. Once the Configuration Wizard is finished, navigate to the __Backstage Configuration Screen__ > __Options__ > __Service Settings__. Define the period for creating snapshots with the Data Collection Interval. Click __Save__ when finished.
4. Skip to the __Snapshot Options__ and customize the snapshot options that are going to be used by the SysKit SQL Manager Service, such as __Load Options__ and __Load Performance__. Click __Save__ when finished. Also, choose what you would like to load each time that SysKit SQL Manager Service crawls your environment.
You can use the load performance slider to switch between low resource usage and a high-performance load. Click Save when finished.
5. Go to __Load Target__ to select the scope on which SysKit SQL Manager Service will crawl for data.
6. Click Save to apply changes and finish configuring the automatic SysKit SQL Manager Service for creating an automatic snapshot of your environment.

If you wish to receive an email notification after automatically-taken environment snapshots, follow these instructions:
1.	Navigate to the __Backstage Configure Screen > Options > Subscription Settings__.
2.	Check in __Subscriptions Enabled__ box, and select the __Enable email sending__ checkbox to enable email to be sent. Fill out the necessary details, then click __Test email settings__ to make sure that the email alert is set up properly. 
3.	Click __Save__ to close the Options wizard and apply the changes. After that you need to create a new subscription. 


