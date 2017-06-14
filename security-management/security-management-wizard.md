---
Title:Security Managment Wizard
Description:This article describes how to grant permissions to the desired principal on specific SQL servers (database engines).
Author:Iva Novoselić
Date:14/06/17
---

This article describes how to grant permissions to the desired principal on specific SQL servers (database engines). You can also revoke permissions from the desired principals and drop logins from SQL Servers.

### Grant Server Permission

1. Navigate to __Security Management__ and click on the __Security Wizard__ in the __Manage__ ribbon.
1. Select __Grant server permissions__ and __Next__ to continue.
1. The __Server__ step allows you to specify the target database engines for which the changes will be made. Select the SQL Server database engines for which you want to grant server permissions and click __OK__. Click __Next__ to continue. 
1. The __Logins and Roles__ step allows you to select the principals who will be granted permissions and the server roles you wish to grant for those principals. If a login does not exist on any of the selected servers, it will be created. Click __Next__ to continue.
1. In the __Options__ step, you can choose either to grant permissions immediately after finishing the wizard using the __Run now__ option or to grant and/or revoke permissions automatically on the required date and time. 
If you choose the __Run on Schedule__ option, the SysKit SQL Manager Service will perform the selected actions at the specified time.
To delay the __Grant server permissions__ action, select the __Grant Permissions On__ checkbox, and then click the required date and time. You can also specify the time to revoke automatically previously granted server permissions and drop created logins by selecting the __Revoke Permissions__ On checkbox, and then clicking the required date and time.If you choose to revoke permissions only, the permissions will be granted immediately after finishing the wizard, and revoked at the specified time. After you finish the wizard, all scheduled actions will be visible with the __Pending__ status in the __Scheduled Actions__ form. If you decide later that you do not want to execute any of the pending actions, you can cancel and delete them using the __Delete__ link in the Scheduled Actions form.
1. If you have configured the automatic permissions management, you can specify the email address that will receive an email notification of the actions performed in the __Send Result To__ step. 
1. In the __Preview__ step, make sure that the pending changes will do exactly what you want and have specified in the previous steps of this wizard.
1. The last step shows the changes that were made. If there are errors, they will be displayed here. It is possible to save this log to disk as a .txt file using the __Save Log__ button.

### Revoke server permissions

1. Navigate to the __Security Management__ and click on the __Security Wizard__ in the __Manage__ ribbon.
1. Select __Revoke server permissions__ and __Next__ to continue. 
1. The __Server__ step allows you to specify the target database engines for which the changes will be made. Select the SQL Server database engines for which you want to revoke server permissions and click __OK__. Click __Next__ to continue. 
1. The __Logins and Roles__ step allows you select the principals from which permissions will be revoked and the server roles you wish to revoke from those principals. Click __Next__ to continue. 
1. In the __Options__ step, you can choose either to revoke permissions immediately after finishing the wizard using the __Run now__ option or to revoke permissions automatically on the required date and time. If you choose the __Run on Schedule__ option, the SysKit SQL Manager Service will perform the selected actions at the specified time.
To delay the Revoke server permissions action, select the __Revoke Permissions On__ checkbox, and then click the required date and time.
After you finish the wizard, all scheduled actions will be visible with the __Pending__ status in the Scheduled Actions form. If you decide later that you do not want to execute any of the __Scheduled actions__, you can cancel them using the __Delete__ link in the Scheduled Actions form. 
1. If you have configured the automatic permissions management, you can specify the email address that will receive an email notification of the actions performed in the __Send Result To__ step. 
1. In the __Preview step__, make sure that the pending changes will do exactly what you want and have specified in the previous steps of this wizard. 
1. The last step shows the changes that were made. If there are errors, they will be displayed here. It is possible to save this log to disk as a .txt file using the __Save Log__ button.

### Drop logins

1. Navigate to __Security Management__ and click on the __Security Wizard__ in the __Manage__ ribbon.
1. Select __Drop logins__ and __Next__ to continue. 
1. The __Server__ step allows you to specify the target database engines for which the changes will be made. Select the SQL Server database engines from which you want to drop logins and click __OK__. Click __Next__ to continue. 
1. The __Logins and Roles__ step allows you to select the principals from which permissions logins will be dropped and server roles you wish to revoke from those principals. Click __Next__ to continue. 
1. n the __Options__ step, you can choose either to revoke permissions immediately after finishing the wizard using the __Run now__ option or to revoke permissions automatically on the required date and time. If you choose the __Run on Schedule__ option, the SysKit SQL Manager Service will perform the selected actions at the specified time.
To delay the Drop logins action, select the __Drop Logins On__ checkbox, and then click the required date and time.
After you finish the wizard, all scheduled actions will be visible with the __Pending__ status in the __Scheduled Actions__ form. If you decide later that you do not want to execute any of the scheduled actions, you can cancel them using the __Delete__ link in the Scheduled Actions form. 
1. If you have configured the automatic permissions management, you can specify the email address that will receive an email notification of the actions performed in the __Send Result To__ step. 
1. In the __Preview__ step, make sure that the pending changes will do exactly what you want and have specified in the previous steps of this wizard.
1. The last step shows the changes that were made. If there are errors, they will be displayed here. It is possible to save this log to disk as a .txt file using the __Save Log__ button.