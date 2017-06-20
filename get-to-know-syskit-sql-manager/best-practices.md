---
Title: Best Practices
Author: Iva Novoselić
Description: This article describes what are best practices to create reports
Date: 13/06/17
---

The Best Practices section contains built-in reports that help SQL Server administrators check whether their SQL Server environment has been configured according to community best practices.

SysKit SQL Manager allows administrators to create their own best practice reports.

Available best practices are grouped into several segments: __Configuration, Databases__, __Hardware Requirements__, __Maintenance, Model DB, Security__, __SQL Server Agent__, __Temp DB__, and __Updates__.

[Learn more](https://www.sqldockit.com/resources/sql-server-best-practices-library/) about best practices in SysKit SQL Manager.

## Configuration

__Auditing Login Failures__: On SQL Servers, the Auditing of Login Failures option is enabled by default. This report checks if the Auditing of Login Failures is enabled on the SQL Server instance.

__Blocked Process Threshold__: The report tells you if the value specified for the blocked process threshold option is low. That means you should tweak the blocked process threshold option to a value of 5 or higher.

__Data Backup Volume__: If the volume that contains the database files fails, you cannot restore from the backup because the backup is also on the same volume.

__Disk Allocation Size__: This report checks whether the block size equals 64 and whether the following calculation (Partition Offset / Block Size) comes up with an integer value as a result. In most cases, this is a storage best practice; however, you should refer to the storage documentation to determine whether this rule applies to your storage.

__Max Degree Of Parallelism__: The Microsoft SQL Server max degree of parallelism (MAXDOP) configuration option controls the number of processors that are used for the execution of a query in a parallel plan. Some applications like SharePoint, Dynamics NAV, SAP, BizTalk has the need to use MAXDOP = 1. Please confirm that your instance is not supporting one of these applications prior to changing the MAXDOP.

__Max Worker Threads__: Using incorrect values for the max worker threads option can result in poor performance and application responsiveness, or even memory loss issues.

__Remote Access__: Remote Access is an obscure SQL Server to SQL Server communication feature that is deprecated. Community best practice is that you ought to avoid it. The report checks whether the ‘remote access’ Server Configuration Option is enabled or not.

__SQL Server Memory__: The minimum and maximum SQL memory values should be configured, and they should differ from the default values.

## Databases

__Auto Close On__: On busy systems, repeated opening and closing of the database can result in performance problems and timeout issues. If the database is used regularly, disable the AUTO_CLOSE option.

__Auto Shrink On__: Configure the database files for sizes required by application and maintenance usage. Avoid using the AUTO_SHRINK option to manage the database file sizes.

__Database Capacity__: Always track the growth of data and log files. A database that is close to full capacity may need attention to avoid initiating growth during critical hours. The report shows thresholds which you can use to spot potentially problematic databases.

__Database Autogrowth__: We recommend that you proactively manage the growth of data and log files by pre-growing all data and log files to their anticipated final size as much as possible. We also recommend that you enable autogrowth for safety reasons. Do not rely on the default autogrowth settings.

__Database Collation__: The report compares Database Collations to Server Collation.

__Database Files__: Database files and transaction logs should not be on the primary drive; they should be on separate drives.

__Simple Recovery Model__: Use the FULL or BULK-LOGGED recovery model when dealing with production servers.

__Virtual Log File Count__: Too many virtual log files can cause transaction log backups to slow down and can also slow down database recovery and, in extreme cases, even affect insert/update/delete performance.

## Hardware Requirements

__Free Disk Space__: The report determines if all servers have enough free disk space. You should be keeping an eye on the available disk space to avoid system failure.

__RAM__: This determines the minimum and recommended amount of RAM for use with a SQL server.

## Maintenance

__Active Directory Valid Logins__:Keep your logins accurate and up to date by removing SQL Server logins that are used by Active Directory users that are either disabled or removed from the domain.

__Database Backups__: The report checks whether the databases have been recently backed up.

## Model DB

__ModelDB Recovery Model__: Set the modelDB’s recovery model to FULL.

__ModelDB Files Initial Size__: The modelDB’s initial size should be set to a value larger than the default. Don’t use the default settings. Also, these values should be set in accordance with your environment.

__ModelDB Files Autogrowth__: The modelDB’s autogrowth should be in megabytes and set to a value larger than the default. Don’t use the default settings. Also, these values should be set in accordance with your environment.

## Security

__Guest Permissions__: You can’t drop the guest user. However, you can run the REVOKE CONNECT FROM GUEST within any database other than the master or tempDB database. This will revoke the guest user’s CONNECT permission as well as disable the user.

__Public Role Not Granted Server Permissions__: The report checks if server permission is granted to the Public role.

__SQL Server User Password Policy__: The report checks if you have the password policy option enabled.Password complexity policies are designed to deter brute force attacks by increasing the number of possible passwords. Password expiration policies are used to manage the lifespan of a password. When SQL Server enforces password expiration policy, users are reminded to change old passwords, and accounts that have expired passwords are disabled.

__SQL Server Users With The Simple Password__: The report checks if you have a password that can be easily guessed. SysKit SQL Manager checks for the following rules: the password is not blank, the password does not equal to the account name of the user, the password does not equal to some of the most common passwords (password, sa, dev, test, admin).

__Trustworthy Bit On__: The default trustworthy bit option is not a best practice. If the trustworthy bit is turned on, a privileged database user can elevate the permission level to the sysadmin role. That leaves the door open for security breaches and unsafe assemblies that can compromise the system.

## SQL Server Agent 

__SQL Agent Service Account__: Running the SQL Server Agent service under a highly-privileged account is a security risk and a bad practice. The report checks whether the SQL Agent account on the server has administrator privileges.

__SQL Server Job Owner__: Checks SQL Server Agent Job owners against a login to validate which jobs do not match that owner. Customize Best Practices to set default job owner.

## Temp DB

__TempDB Files__: Each tempDB file should be on a separate drive.

__TempDB Size__: The size of the tempDB should be at least 10% of the largest database on the SQL server.

__TempDB Files Configuration__: The number of tempdb files should be the same as the number of processor cores present on the SQL server and no larger than eight. Additionally, all file sizes should be equal.

__TempDB Response Times__: The write response times for tempDB should be less than 20 ms and read response times should be less than 20 ms.

__TempDB Recovery Model__: The tempDB’s recovery model should be set to SIMPLE.

__TempDB Files Growth__: Set the file growth increment to a reasonable size to avoid the tempDB database files from growing by too small a value. If the tempDB file size is under 200 MB, set the File Growth to Megabytes value, otherwise set the File Growth to Percent value.

__Temp DB Separate Drive__: By default, the TempDB files are put on the same drive as the SQL Server binaries. Even if the user chooses a custom install, TempDB still goes on the same drive as the other data files, and that’s a bad practice. Instead, the TempDB data files should be on a dedicated drive.

## Updates

__Windows Updates__: This report checks whether any servers have Windows updates that are not installed.

__Is SQL Server up to Date__: The report check whether servers in your environment are up to date. SQL Server cumulative updates are released regularly, so this report also checks the Microsoft SQL Server Update Center for the latest updates.
