---
title: Miscellaneous
description: This article describes how to troubleshoot various issues that may appear during the usage of SysKit SQL Manager.
author: Tomislav Sirovec
date: 13/6/2017
---

## SysKit SQL Manager Connections

There are a couple of errors that may be encountered when SysKit SQL Manager attempts to connect and create inventory of your SQL Servers.

### Error Locating Server/Instance Specified

#### Problem: 

A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: SQL Network Interfaces, error: 26 – Error Locating Server/Instance Specified)

#### Solution:

If you are using named instance on a port other than the default, make sure SQL Browser is running, or configure the custom port in the SysKit SQL Manager UI.

### Cannot open database “model” requested by the login. The login failed. Login failed for user  ‘CONTOSO\walterwhite’

#### Problem:

Cannot open database “model” requested by the login. The login failed. Login failed for user ‘CONTOSO\walterwhite’.

#### Solution:

The user running SysKit SQL Manager and creating a snapshot must be sysadmin on the SQL Server in order to retrieve info from user and system databases.

For more information, refer to [User Permission Requirements](#internal/requirements/user-permission-requirements/).

### The service ‘MSSQL$SQLEXPRESS’ not running on ‘SERVER’.

#### Problem:

The service ‘MSSQL$SQLEXPRESS’ not running on ‘SERVER’.

#### Solution:

Use SQL Server Configuration Manager to ensure the SQL Service is running before attempting to inventory this server.

### Report Server Web Service is not configured.

#### Problem:

Report Server Web Service is not configured.

#### Solution:

SysKit SQL Manager cannot connect to an instance that has not been configured. Use the Reporting Services Configuration Manager to configure Reporting Services.

### Microsoft.ReportingServices.Library.ReportServerDatabaseUnavailableException: The report server cannot open a connection to the report server database. A connection to the database is required for all requests and processing

#### Problem:

Microsoft.ReportingServices.Library.ReportServerDatabaseUnavailableException: The report server cannot open a connection to the report server database. A connection to the database is required for all requests and processing

#### Solution:

This error indicates that SysKit SQL Manager cannot connect to the underlying Reporting Services database. Make sure Reporting Services are properly configured (use the Reporting Services Configuration Manager to validate your configuration) and make sure that the SysKit SQL Manager account used to retrieve information about this Reporting Services instance has the right privileges to read from the Reporting Services database.

### Client found response content type of “, but expected ‘text/xml’. The request failed with an empty response. The report server has encountered a configuration error. (rsServerConfigurationError)

#### Problem:

Client found response content type of “, but expected ‘text/xml’. The request failed with an empty response. The report server has encountered a configuration error. (rsServerConfigurationError)

#### Solution:

This error indicates that there is a general configuration error with Reporting Services. Please refer to [this MSDN article](https://docs.microsoft.com/en-us/sql/reporting-services/troubleshooting/rsserverconfigurationerror-reporting-services-error) for more details.

### Unable to connect to the remote server.

#### Problem:

Unable to connect to the remote server.

#### Solution:

Use the Reporting Services Configuration Manager to validate the URLs used for Reporting Services. Make sure these are accessible from the server or workstation where SysKit SQL Manager is installed.

### The network path was not found

#### Problem:

The network path was not found

#### Solution:

The user has no permission to read the registry or the path does not exist. User needs to have access to the Windows Registry, which can be found under Local Machine hive.

### Microsoft.ReportingServices.Diagnostics.Utilities.SecureConnectionRequiredException: The operation you are attempting requires a secure connection (HTTPS).

#### Problem:

Microsoft.ReportingServices.Diagnostics.Utilities.SecureConnectionRequiredException: The operation you are attempting requires a secure connection (HTTPS).

#### Solution:

The error occurs because the SSRS server is configured to accept connections only via HTTPS. Check out [this MSDN article](https://support.microsoft.com/en-us/help/2011889/error-setup-failed-to-validate-specified-reporting-services-report-server-occurs-when-you-install-microsoft-dynamics-crm) on how to reconfigure Reporting Services.

### The SELECT permission was denied on the object ‘sysssispackages’, database ‘msdb’, schema ‘dbo’.

#### Problem:

The SELECT permission was denied on the object ‘sysssispackages’, database ‘msdb’, schema ‘dbo’.

#### Solution:

The user you configured to retrieve information about this SQL Server Integration Services instances. Check the account permissions and grant the user the select permission on the table ‘sysssispackages’.

### The user does not have permission to perform this action.

#### Problem:

The user does not have permission to perform this action.

#### Solution:

The user that is being used to run SysKit SQL Manager and retrieve server information needs to be a local admin on the machine and a member of the sysadmin, processadmin or serveradmin role on this server.

### A connection cannot be made to redirector. Ensure that ‘SQL Browser’ service is running.

#### Problem:

A connection cannot be made to redirector. Ensure that ‘SQL Browser’ service is running.

#### Solution:

This could indicate that your SQL Browser service is not running on the SQL Server or the account that is being used to run the SQL Browser service cannot access the configuration files for Analysis Services. Check out [this article](https://blogs.msdn.microsoft.com/karang/2013/02/20/connectivity-issue-a-connection-cannot-be-made-to-redirector-ensure-that-sql-browser-service-is-running/) to learn more.

### Timeout expired

#### Problem:

Connection timeout expired. Server is taking too long to respond.

#### Solution:

Try retaking the snapshot at a later time.

### Error validating encrypted data.

#### Problem:

Error validating encrypted data.

#### Solution:

The report server is unable to decrypt and use any data that is encrypted with the current key. Delete your encryption keys, and re-add the credentials to data sources on the affected instance using the Reporting Services Configuration tool.

### Reporting Services instance ID fetching failed.

#### Problem:

Reporting Services instance ID fetching failed.

#### Solution:

User needs to have access to the Windows Registry, which can be found under Local Machine hive.

### Report server installation is not initialized.

#### Problem:

Report server installation is not initialized.

#### Solution:

To initialize a report server, use the Reporting Services Configuration tool.

### Attempted to perform an unauthorized operation.

#### Problem:

Attempted to perform an unauthorized operation.

#### Solution:

User needs to have access to the Windows Registry, which can be found under Local Machine hive.

### Configuration file problem.

#### Problem:

Configuration file problem.

#### Solution:

User needs to have access to the Windows Registry, which can be found under Local Machine hive.
User needs to have read access to the configuration file.

### No SQL credentials found for this Azure server.

#### Problem:

No SQL credentials found for this Azure server.

#### Solution:

Make sure you entered the credentials correctly for this server, or edit the server with the correct credentials.

