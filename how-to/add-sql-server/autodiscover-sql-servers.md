---
title: Autodiscover SQL Servers
description: This section will show you how you can enable an autodetect option to auto-detect servers from your domains before each snapshot.
author: Petra Filipi
date: 08/06/2017
---
This section will show you how you can enable an autodetect option to auto-detect servers from your domains before each snapshot.

Besides manually adding SQL Servers there is an option for auto-discovering all SQL Servers within your environment before each snapshot. If you choose to enable the autodetect option without specifying any credentials or domains, only servers from the default domain will be detected.

Use the __Options__ wizard to adjust and change your Snapshot [Options](#internal/get-to-know-syskit-sql-manager/backstage-screen/options-wizard).

### Follow these steps to enable or disable autodetect option:
1. Navigate to the __Backstage Actions Screen__ and click __Administration__.
2. To enable or disable autodetect option use the corresponding button in the Environment ribbon or use [Target Options](#internal/get-to-know-syskit-sql-manager/backstage-screen/options-wizard).

You can also [add multiple domains](#internal/how-to/add-sql-server/manage-domains-credentials/) and multiple credentials so that SysKit SQL Manager can auto-discover servers from multiple domains.

__Note__: Auto-detected SQL Servers will have a blue circle next to the Server Type icon in the SQL Servers grid so you can easily distinguish them from manually added servers, which will have an orange circle next to the icon.