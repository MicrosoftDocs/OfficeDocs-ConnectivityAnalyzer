---
title: ADFS SSL Certificate Expired
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

# ADFS SSL Certificate Expired

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-13_

<div id="sectionSection0" class="section">

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. The endpoint will be a Secure Sockets Layer (SSL) connection, which will have a certificate in place. The tool evaluates the fully qualified domain name (FQDN) that was assigned to the certificate (for example, STS.Contoso.com).

The Remote Connectivity Analyzer displays a certificate trust warning when the certificate that is used for SSL has expired. This indicates that the certificate is not valid and that users will not be able to authenticate correctly to their Office 365 resources. If this issue occurs, the passive (Internet Explorer) access to the Office 365 services fails to connect, and it generates a similar warning when the user tries to access a web page.

<div>

## More Information

For information about how to troubleshoot this issue, see Microsoft Knowledge Base article 2523494, [You receive a certificate warning when you try to access Microsoft Office 365 resources by using an identity-federated account](https://support.microsoft.com/kb/2523494)

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

