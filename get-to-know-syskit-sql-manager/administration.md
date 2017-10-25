---
title: Administration
author: Petra Filipi
description: This article outlines all the options for the successful administration of SQL Servers that are being monitored with SysKit SQL Manager.
date: 25/10/2017
---
If you click on the Administration tab in the left navigation, the Administration – SQL Servers section will be displayed.

## Administration – SQL Servers
This report displays all SQL Servers in your domains and their characteristics, such as Server Type, Server, Port, Edition, Monitoring Status and assigned Tags.

The __Server Type__ column displays the SQL Server type. The type can be __Database Engine, Analysis Service, Integration Service, Reporting Service__ or __Azure__.

The __SQL Server Tags__ column displays all tags assigned to the selected SQL Server. One or more tags can be assigned to a server.

The __Port__ column displays the SQL Server port.

The __Edition__ column displays the SQL Server edition.

The __Log on As__ column displays the credentials used while connecting to the selected SQL Server.

Detected SQL Servers can have enabled or disabled __Monitoring Status__ in the Administration tab:
* __Enabled__ – Server instance will be included in snapshots and Live Explorer.
* __Disabled__ –  Server instance will not be included in snapshots or Live Explorer.
The Licenses Used (Required Licenses) above the grid shows the number of used or required SysKit SQL Manager licenses. Licenses for SQL Server Express and Developer editions are complimentary.

## Administration – Domains
This report displays all __Domains__ in your environment. 
You can add multiple domains to start detecting SQL Servers from multiple domains. If you don't add a domain, the default domain will be used for SQL Servers detection. Also, you can enable or disable  the Domain Status. If the Domain Status is disabled, SQL Servers from that domain will be automatically excluded from snapshots and the Live Explorer.
* __Add Domain__ – Add a domain to start detecting SQL Servers from.
* __Edit Domain__ – Edit credentials or organizational units for the selected domain.
* __Delete Domain__ – Delete a domain to stop detecting servers from it. For the default domain you can only change the status (Enabled or Disabled).
* __Enable Domain Status__ – Enable the Domain Status to detect SQL Servers.
* __Disable Domain Status__ – Disable the Domain Status to exclude servers from snapshots and Live Explorer.
## Administration – Credentials
This report displays a list of all credentials: display names, usernames and Authentication types.
* __Add Credential__ – Add credentials to the credentials list.
* __Edit Credential__ – Edit credentials.
* __Delete Credential__ – Delete credentials from the credentials list.
## Administration – Comments

## Administration – Tags

### __Administration Ribbon__
Use the Administration ribbon to take actions such as:
* Detect – automatically detect all SQL Servers from enabled domains.
* Enable/Disable auto detect option
* Manually add SQL Servers
* Tag and untag SQL Servers  – Quickly assign a tag to the desired server.
* Enable/Disable Monitoring Status 
* Manage domains and credentials
* Go to Explorer – View and manage your SQL Servers and databases live, without taking a snapshot.
* Go to Dashboard – View the live dashboard for the currently selected SQL Server.
