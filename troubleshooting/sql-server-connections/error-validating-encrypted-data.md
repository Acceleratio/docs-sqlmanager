---
title: Error validating encrypted data
description: This article describes how to resolve the error validating encrypted data.
author: Petra Filipi
date: 12/07/2017
---

### Problem:
Error validating encrypted data.

### Solution:
The report server is unable to decrypt and use any data that is encrypted with the current key. Delete your encryption keys, and re-add the credentials to data sources on the affected instance using the Reporting Services Configuration tool.