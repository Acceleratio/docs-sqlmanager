---
title: SQL Server Configuration Prerequisites
description: This article describes which are the SQL Server Configuration prerequisities for SysKit SQL Manager.
author: Tomislav Sirovec
date: 06/06/2017
---
### Remote Connections

In order for SysKit SQL Manager agent to connect to a SQL Server (or instance), the remote connections need to be enabled. The following should be done in the SQL Management Studio:

* Right-click the Server or Instance name
* Click __Properties__.
* From the left-hand side, choose __Connection__.
* Make sure the __Allow remote connections to this server__ check box is selected.

### SQL Server Protocols

You will need to enable both TCP/IP and Named Pipes protocol in order to properly perform an inventory of your SQL Server. Here is what you need to do:

* Use RDP to connect to the computer that hosts the SQL Server
* Open “SQL Server Configuration Manager”
* Navigate to SQL Server Network Configuration
* Expand the Protocols for __Instance_Name__
* Make sure both TCP/IP and Named Pipes protocol are enabled

You will need to restart your SQL Server once you enable these protocols.

#### Additional resources

* Follow [this guide](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/configure-client-protocols) to learn more about SQL Server protocols.
* Learn more about [SQL Server configuration](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/enable-or-disable-a-server-network-protocol).
* On some computers that have a 32bit SQL Server installed on a 64bit machine you might encounter the following error: “Cannot connect to WMI provider. You do not have permission or the server is unreachable”. Follow [this guide](https://support.microsoft.com/en-us/help/956013/error-message-when-you-open-sql-server-configuration-manager-in-sql-server-cannot-connect-to-wmi-provider.-you-do-not-have-permission-or-the-server-is-unreachable) to resolve the issue.

### Ports Used For SQL Server

The default SQL Server instance uses the TCP/IP port 1433. But depending on your configuration and if there are whether multiple or named instances, your SQL Server could be using a different port.

If a predefined port is being used, you can see this value in the SQL Server Configuration Manager > Protocols for SQL Server (or your instance name) > TCP/IP Protocol properties > IP Address and TCP Port property.

If a dynamic port is being used, you can use the following code to retrieve its information. Use SQL Server Management Studio to execute it:

> USE master  
> GO  
> xp_readerrorlog 0, 1, N'Server is listening on'  
> GO  

If you cannot run the above-mentioned command, the alternative way to retrieve port information is to run the following command in the Command Prompt:

> netstat -ano | findstr 1234

Replace the numbers (1234) in the command with the SQL Server Process ID. Process Id of the SQL Server process. If your SQL Server is using different ports, you should remember these ports and open them in the firewall. The next section provides instructions for the configuration of firewall ports and allowing SysKit SQL Manager to discover these servers.

### Firewall Configuration

If firewall is enabled on the computer that has SQL Server installed, you will need to make sure the ports used by the SQL Server allow inbound traffic. By default, SQL Server uses ports 1433 and 1434, but could also be using other ports.

Open firewall network ports are required for gathering the data.

If you have a firewall between the server hosting the application and the SQL servers that are being discovered, you will need the following ports open:

* WMI uses RPC TCP 135 and a random UDP port over 1024. We use WMI to get the data about the underlying Windows Server like OS version, IP address, server free space etc. This is standard and usually you don’t need to configure anything because Windows Servers rely a lot on WMI.
* SQL Server default instance running over TCP port 1433.
* SQL Server named instances running on a dynamic port determined at the time the Database Engine starts.
* SQL Server named instances when they are configured to use a fixed port. The TCP port number is configured by the administrator.

Follow [this guide](https://docs.microsoft.com/en-us/sql/sql-server/install/configure-the-windows-firewall-to-allow-sql-server-access) to learn more about firewall configuration.

### Servers With Multiple Instelled and Named Instances

If there is more than one instance of SysKit SQL Manager installed on a single computer (e.g. “COMPUTER” and “COMPUTER\OFFICESERVERS”), or if a named instance is installed on a computer (e.g. “COMPUTER\SQLEXPRESS”), SQLDocKit is not going to be able to connect to the instance automagically. One of the following must be configured:

* Use the SQL Server Configuration Manager to enable SQL Server Browser service on this machine. Make sure it is configured to run Automatically when Windows starts. You can enable it in SQL Server Configuration Manager under SQL Server Services.
* Find the exact port number used by each instance and then enter port number in the SysKit SQL Manager > SQL Servers dialog for this instance.