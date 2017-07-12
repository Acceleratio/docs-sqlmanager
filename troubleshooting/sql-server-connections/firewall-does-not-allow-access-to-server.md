---
title: Firewall does not allow access to this server from current IP address
description: 
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Cannot open ‘SERVER’ requested by the login. Client with current IP address is not allowed to access the server.

### Solution:
To enable access, use the Windows Azure Management Portal or run sp_set_firewall_rule on the master database to create a firewall rule for this IP address or address range. It may take up to five minutes for this change to take effect. Check out this [MSDN article](https://blogs.msdn.microsoft.com/azuresqldbsupport/2015/04/29/configuring-the-firewall-for-client-access/) article to learn more.