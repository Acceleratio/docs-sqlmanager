---
title: Administration
author: Petra Filipi
description: This article outlines all the options for the successful administration of SQL Servers that are being monitored with SysKit SQL Manager.
date: 25/10/2017
---
If you click on the Administration tab in the left navigation, the Administration – SQL Servers section will be displayed.

Administration – SQL Servers
This report displays all SQL Servers in your domains and their characteristics, such as Server Type, Server, Port, Edition, Monitoring Status and assigned Tags. 
The Server Type column displays the SQL Server type. The type can be Database Engine, Analysis Service, Integration Service, Reporting Service or Azure.
The SQL Server Tags column displays all tags assigned to the selected SQL Server. One or more tags can be assigned to a server.
The Port column displays the SQL Server port.
The Edition column displays the SQL Server edition.
The Log on As column displays the credentials used while connecting to the selected SQL Server.
Detected SQL Servers can have enabled or disabled Monitoring Status in the Administration tab:
•	Enabled – Server instance will be included in snapshots and Live Explorer.
•	Disabled –  Server instance will not be included in snapshots or Live Explorer.
The Licenses Used (Required Licenses) above the grid shows the number of used or required SysKit SQL Manager licenses. Licenses for SQL Server Express and Developer editions are complimentary.

Administration – Domains
This report displays all Domains in your environment. 
You can add multiple domains to start detecting SQL Servers from multiple domains. If you don't add a domain, the default domain will be used for SQL Servers detection. Also, you can enable or disable  the Domain Status. If the Domain Status is disabled, SQL Servers from that domain will be automatically excluded from snapshots and the Live Explorer.
•	Add Domain – Add a domain to start detecting SQL Servers from.
•	Edit Domain – Edit credentials or organizational units for the selected domain.
•	Delete Domain – Delete a domain to stop detecting servers from it. For the default domain you can only change the status (Enabled or Disabled).
•	Enable Domain Status – Enable the Domain Status to detect SQL Servers.
•	Disable Domain Status – Disable the Domain Status to exclude servers from snapshots and Live Explorer.
Administration – Credentials
This report displays a list of all credentials: display names, usernames and Authentication types.
•	Add Credential – Add credentials to the credentials list.
•	Edit Credential – Edit credentials.
•	Delete Credential – Delete credentials from the credentials list.
Administration – Comments

Administration – Tags

Administration Ribbon
Use the Administration ribbon to take actions such as:
•	Detect – automatically detect all SQL Servers from enabled domains.
•	Enable/Disable auto detect option
•	Manually add SQL Servers
•	Tag and untag SQL Servers  – Quickly assign a tag to the desired server.
•	Enable/Disable Monitoring Status 
•	Manage domains and credentials
•	Go to Explorer – View and manage your SQL Servers and databases live, without taking a snapshot.
•	Go to Dashboard – View the live dashboard for the currently selected SQL Server.
