---
title: No process is on the other end of the pipe
description: 
author: Petra Filipi
date: 12/07/2017
---

### Problem:
A connection was successfully established with the server, but then an error occurred during the login process.

### Solution:
Check that Named Pipe is enabled in SQL Server Configuration Manager and that TCP is set before named pipes in the protocol order list. Make sure you have either SQL Server Authentication or Mixed Mode enabled.