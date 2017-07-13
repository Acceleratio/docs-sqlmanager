---
title: Unauthorized request
description: This article describes how to resolve error that occurs when the user is not authorized to the Report Server. 
author: Petra Filipi
date: 12/07/2017
---

### Problem:
The request failed with HTTP status 401: Unauthorized.

### Solution:
Make sure that the credentials used to retrieve information about this Reporting Services instance have the right privileges to read from the Reporting Service. Make sure that the user's Windows account is not locked out.