---
title: The SELECT permission was denied
description: This article describes how to resolve the error when the user you have created does not have the sufficient privileges to access your tables in database.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
The SELECT permission was denied on the object ‘sysssispackages’, database ‘msdb’, schema ‘dbo’.

### Solution:
The user you configured to retrieve information about this SQL Server Integration Services instances does not have the sufficient privileges to access your tables in database. Check the account permissions and grant the user the select permission on the table ‘sysssispackages’.