---
title: Unknown Username or bad password
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

# Unknown Username or bad password

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to simulate the token retrieval process from the on-premise ADFS server. To perform the test, you must type the correct username and password so that the tool retrieves the token correctly on behalf of the user.

The Remote Connectivity Analyzer displays the following warning message if the user is not authenticated correctly:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The Security Token Service indicated that the authentication failed. Check the username and password and try again.</p></td>
</tr>
</tbody>
</table>

This message indicates a logon failure when you try to authenticate at the ADFS endpoint. This error can occur for any of the following reasons:

  - Users enter a bad password

  - Users enter a bad username

  - Users do not have the identity federated domain set as their UPN

<div class="subSection">

You can address these issues in the on-premise Active Directory Users and Computers MMC.

</div>

</div>

<div>

## More Information

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

<span> </span>

</div>

</div>

</div>

