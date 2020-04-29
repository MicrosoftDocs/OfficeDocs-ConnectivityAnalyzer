---
title: ADFS SSL Certificate Trust
TOCTitle: ADFS SSL Certificate Trust
ms:assetid: 19604d13-e410-4874-961c-1900ab391d66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh241330(v=EXCHG.80)
ms:contentKeyID: 36021329
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# ADFS SSL Certificate Trust

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Exchange Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. The endpoint will be a Secure Sockets Layer (SSL) connection, which will have a certificate in place. The tool evaluates the fully qualified domain name (FQDN) that was assigned to the certificate (for example, STS.Contoso.com).

The Remote Connectivity Analyzer displays a warning when the certificate that is used for SSL cannot be trusted up to the root. This indicates that the certificate is not trusted by the Office 365 environment. In many cases, this condition exists because the certificate is a self-signed certificate that is not valid for this form of authentication.

The certificate trust warning means that users might not be able to authenticate correctly to their Office 365 resources. If this issue occurs, the passive (Internet Explorer) access to the Office 365 services display a certificate warning when the user accesses the services. Only after the certificate warning is accepted can the Passive client connect. The Outlook client is not presented with this certificate security warning, and the client fails to connect.

<div>

## More information

For information about how to troubleshoot this issue, see the Microsoft Knowledge Base article, [You receive a certificate warning when you try to access Microsoft Office 365 resources by using an identity-federated account](http://support.microsoft.com/kb/2523494)

For more information planning for identity federation, see [Prepare for single sign-on](http://onlinehelp.microsoft.com/en-us/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](http://technet.microsoft.com/en-us/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

