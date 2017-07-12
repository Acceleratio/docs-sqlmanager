---
title: The operation you are attempting requires a secure connection
description:
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Microsoft.ReportingServices.Diagnostics.Utilities.SecureConnectionRequiredException: The operation you are attempting requires a secure connection (HTTPS).

### Solution:
The error occurs because the SSRS server is configured to accept connections only via HTTPS. Check out this [MSDN article](https://support.microsoft.com/en-us/help/2011889/error-setup-failed-to-validate-specified-reporting-services-report-server-occurs-when-you-install-microsoft-dynamics-crm) on how to reconfigure Reporting Services.