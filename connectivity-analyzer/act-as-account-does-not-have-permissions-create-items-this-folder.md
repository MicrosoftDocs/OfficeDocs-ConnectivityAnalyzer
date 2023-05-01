---
title: The Act As Account Does Not Have Permissions to Create Items in this Folder
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'ErrorCreateItemAccessDenied, the Act As Account does not have permissions to create items in this folder.'
ms.date: 05/08/2020
---

# The Act As Account Does Not Have Permissions to Create Items in this Folder


_**Topic Last Modified:** 2012-05-23_

The Microsoft Remote Connectivity Analyzer sends a CreateItem XML/HTTP request to the Exchange Web Services service using the Exchange Web Services API to create a test item in a mailbox or public folder. When an access denied error status message is present in the response, the Microsoft Remote Connectivity Analyzer generates the following error:

"ErrorCreateItemAccessDenied, the Act As Account does not have permissions to create items in this folder."

The Microsoft Remote Connectivity Analyzer uses the [CreateItem Operation](https://go.microsoft.com/fwlink/?linkid=161972) of Exchange Web Services to create a simple mail message in a mailbox or public folder to test whether the account specified has permissions to write to the specified folder.

The "Act As Account" is the account used by Exchange to authorize the execution of Exchange Web Services commands. In most cases, this is the account issuing the Exchange Web Services requests; however, if [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) (also known as [Server-to-Server Authorization](https://go.microsoft.com/fwlink/?linkid=161951)) is being used, then the account being impersonated is the "Act As account".

## For More Information

To resolve this issue, the Act As account must have permission to create items in the folder specified. To make sure the Act As account has the appropriate permissions, do the following:

1.  Grant the Act As account full mailbox permissions to the folder's mailbox via the [Add-MailboxPermission](https://go.microsoft.com/fwlink/?linkid=76497) command. Or, see [How to Allow Mailbox Access](https://go.microsoft.com/fwlink/?linkid=76535).

2.  Grant the Act As account permissions to create items in the public folder via the [Add-PublicFolderClientPermission](https://go.microsoft.com/fwlink/?linkid=123666) command. Also, see [Configuring Public Folder Permissions](https://go.microsoft.com/fwlink/?linkid=123665).

3.  Grant the Act As account permission to create items in the specified mailbox or public folder in Outlook by editing the [Outlook folder permissions](https://go.microsoft.com/fwlink/?linkid=86319).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
