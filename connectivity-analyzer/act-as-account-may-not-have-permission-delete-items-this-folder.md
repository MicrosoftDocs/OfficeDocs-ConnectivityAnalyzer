---
title: The Act As Account May Not Have Permission to Delete Items in this Folder
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# The Act As Account May Not Have Permission to Delete Items in this Folder

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-05-23_

The Microsoft Remote Connectivity Analyzer sends a [DeleteItem Operation](https://go.microsoft.com/fwlink/?linkid=161962) XML/HTTP request to the Exchange Web Services service using the Exchange Web Services API to delete a test item in a mailbox or public folder. When an access denied error status message is present in the response, the Microsoft Remote Connectivity Analyzer generates the following error.

"ErrorCannotDeleteObject, the Act As account may not have permission to delete items in this folder."

The Microsoft Remote Connectivity Analyzer uses the [DeleteItem Operation](https://go.microsoft.com/fwlink/?linkid=161962) of Exchange Web Services to delete a test mail message in a mailbox or public folder to test whether the account specified has permissions to write to the specified folder.

The Act As Account is the account used by Exchange to authorize the execution of Exchange Web Services commands. In most cases, this is the account issuing the Exchange Web Services requests. However, if [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) (also known as [Server-to-Server Authorization](https://go.microsoft.com/fwlink/?linkid=161951)) is being used, then the account being impersonated is the Act As Account.

<div>

## For More Information

To resolve this issue, the Act As account must have permission to create items in the specified folder. To make sure the Act As account has the appropriate permissions, do the following:

1.  Grant the Act As account full mailbox permissions to the folder’s mailbox via the [Add-MailboxPermission](https://go.microsoft.com/fwlink/?linkid=76497) command. Or, see [How to Allow Mailbox Access](https://go.microsoft.com/fwlink/?linkid=76535).

2.  Grant the Act As account permission to delete items in the public folder via the [Add-PublicFolderClientPermission](https://go.microsoft.com/fwlink/?linkid=123666) command. Also, see [Configuring Public Folder Permissions](https://go.microsoft.com/fwlink/?linkid=123665).

3.  Grant the Act As account permission to delete items in the specific mailbox or public folder in Microsoft Office Outlook. For more information, see [Outlook folder permissions](https://go.microsoft.com/fwlink/?linkid=86319).

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

