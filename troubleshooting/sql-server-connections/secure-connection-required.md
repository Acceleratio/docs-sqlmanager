---
title: The operation you are attempting requires a secure connection
description: This article describes how to resolve the error that occurs while report generation when you're trying to connect to reporting services with an HTTP connection, and the reporting services is configured to accept connections only via HTTPS.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Microsoft.ReportingServices.Diagnostics.Utilities.SecureConnectionRequiredException: The operation you are attempting requires a secure connection (HTTPS).

### Solution:
The error occurs because the SSRS server is configured to accept connections only via HTTPS, and a call is made to the report server over a standard HTTP connection.. Check out this [MSDN article](https://support.microsoft.com/en-us/help/2011889/error-setup-failed-to-validate-specified-reporting-services-report-server-occurs-when-you-install-microsoft-dynamics-crm) on how to reconfigure Reporting Services.