---
title: General issues that may occur for one or all users
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# General issues that may occur for one or all users

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-02-24_

<div id="sectionSection0" class="section">

The Microsoft Exchange Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. The tool performs the authentication on behalf of the user to simulate authentication to the Office 365 environment.

If the Remote Connectivity Analyzer tool displays a warning at this stage, the message can indicate any of several different issues. Because the authentication process involves many steps, the solution that is required for a returned error or warning is not always obvious. For example, you might receive one of the following messages:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>There was a problem accessing the site. Try to browse to the site again.</p></td>
</tr>
<tr class="even">
<td><p>Your organization could not sign you in to this service</p></td>
</tr>
</tbody>
</table>

The following are some of the issues that can cause such generic errors:

  - Stale Identity Federation information in the Office 365 environment

  - Incorrect Identity Federation information in the Office 365 environment

  - Recent UPN change issues

  - Various Firewall settings at the ADFS endpoint

Because errors such as these are fairly generic, the solutions will vary widely. The “More information” section includes several different methods for resolving these issues.

<div>

## More Information

For more information about how to troubleshoot issues that have unidentified causes, see the following Microsoft Knowledge Base articles:

  - [How to reestablish trust with the Office 365 authentication platform after the AD FS 2.0 server stops responding](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2521057)

  - [Internet-based client computers cannot authenticate after you configure Active Directory Federation Services (AD FS) in a "firewall-published" configuration](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2535789)

  - ["Your organization could not sign you in to this service" error message occurs when a user tries to sign in to the Office 365 portal as a federated user](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2535191)

  - [A federated user is prompted for credentials or cannot sign in to Microsoft Online Services setting up single sign-on for an organization](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2392130)

For more information about how to plan for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

