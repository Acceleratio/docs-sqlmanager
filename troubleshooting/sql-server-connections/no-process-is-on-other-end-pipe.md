---
title: No process is on the other end of the pipe
description: This article describes how to resolve the named pipe error when connecting to SQL server if the server has not enabled pipe support.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
No process is on the other end of the pipe. A connection was successfully established with the server, but then an error occurred during the login process.

### Solution:
Check that Named Pipe is enabled in SQL Server Configuration Manager and that TCP is set before named pipes in the protocol order list. Make sure you have either SQL Server Authentication or Mixed Mode enabled.