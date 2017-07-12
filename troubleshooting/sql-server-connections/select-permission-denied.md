---
title: The SELECT permission was denied
description: 
author: Petra Filipi
date: 12/07/2017
---

### Problem:
The SELECT permission was denied on the object ‘sysssispackages’, database ‘msdb’, schema ‘dbo’.
### Solution:
The user you configured to retrieve information about this SQL Server Integration Services instances. Check the account permissions and grant the user the select permission on the table ‘sysssispackages’.