---
title: The domain is a federated domain but the user <User>@contoso.com is not known by Office 365
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# The domain is a federated domain but the user \<User\>\@contoso.com is not known by Office 365

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-10-25_

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. Occasionally, the realm discovery process runs but still displays a warning message.

Realm discovery runs to generate the identity provider for the user. After the domain name passes the realm discovery check, an additional process runs to determine whether the user has an account in the Microsoft Office 365 environment. This additional check will not cause the test to fail, but it can cause an error that would generate a warning message.

The Remote Connectivity Analyzer displays the following warning message if the domain was federated but the user account was not enabled in the Office 365 environment:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The domain is a federated domain but the user apollo@contoso.com is not known by Office 365</p></td>
</tr>
</tbody>
</table>

You can safely ignore this warning message.

<div>

## More Information

For more information about how to resolve this issue, see Microsoft Knowledge Base article 2523192, [The user principal names (UPN), email addresses, or proxy addresses of users contain an Office 365 domain after synchronization](https://support.microsoft.com/kb/2523192)

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

<span> </span>

</div>

</div>

</div>

