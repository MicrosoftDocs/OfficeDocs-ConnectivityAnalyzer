---
title: Token Signing Certificate Expired
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

# Token Signing Certificate Expired

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Exchange Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to simulate the authentication process that a client uses to authenticate by using identity federation. Occasionally, a Outlook client or a Microsoft Internet Explorer connection fails because of an expired Token Signing certificate.

When this issue occurs you will see an error similar to the following if you were using the Passive authentication type (Internet Explorer)

There was a problem accessing the site. Try to browse to the site again.If the problem persists, contact the administrator of this site and provide the reference number to identify the problem.Reference number: \<GUID\>

The Remote Connectivity Analyzer displays a warning message if the authentication fails. The issue can be caused by an expired token signing certificate. This can occur because ADFS can auto-renew a self-signed token signing certificate by default. The advantage of this functionality is that it minimizes the maintenance required by the ADFS environment. However, the same functionality can affect identity federation because the Authentication Platform in the cloud is not aware of this new token signing certificate.

<div>

## More Information

For more information about how to troubleeshoot this issue, see Microsoft Knowledge Base article 2383983, [A token-signing certificate has expired or was renewed for Office 365 Identity Federation](https://support.microsoft.com/kb/2383983).

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/en-us/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/en-us/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

