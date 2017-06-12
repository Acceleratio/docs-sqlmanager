---
title: Autodiscover SQL Servers
description: This section will show you how you can enable an autodetect option to auto-detect servers from your domains before each snapshot.
author: Petra Filipi
date: 08/6/2017
---
This section will show you how you can enable an autodetect option to auto-detect servers from your domains before each snapshot.

Besides manually adding SQL Servers there is an option for auto-discovering all SQL Servers within your environment before each snapshot. If you choose to enable the autodetect option without specifying any credentials or domains, only servers from the default domain will be detected.

Use the __Options__ wizard to adjust and change your Snapshot [Options](#internal/get-to-know-syskit-sql-manager/backstage-screen/options-wizard).

### Follow these steps to enable or disable autodetect option:
1. Navigate to the __Snapshot__ options.
2. Check or uncheck the __Enable autodetect__ option.
3. Click __Save__.


You can also add multiple credentials and multiple domains so that SysKit SQL Manager can auto-discover servers from multiple domains.

### Manage Domains
Follow these steps to  manage domains which SysKit SQL Manager will use when loading server data:

1. Navigate to the __Backstage Actions Screen__ and click the __Manage Domains__ button.
1. Click the __Add Domain__ button.
1. Specify a domain/domain controller or choose to use your current domain.
1. Specify credentials.
   *  If you want to add multiple credentials click the __Edit__ button next to the __Specify Service Account__ option.
1. Choose the __Organizational Units__ from which you want to discover servers.
1. Click __OK.__
1. Follow steps 2-6  to add multiple domains and credentials.

__Note__: Auto-detected SQL Servers will have a blue circle next to the Server Type icon in the SQL Servers grid so you can easily distinguish them from manually added servers, which will have an orange circle next to the icon.
