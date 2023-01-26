---
title: ADFS SSL Certificate Name Mismatch
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer tool returns the following warning if the FDQN does not match the host address or URL that the client uses to make a connection with the server: SSL Certificate Name Mismatch'
ms.date: 05/08/2020
---

# ADFS SSL Certificate Name Mismatch


_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint name that the client requires for authentication. The endpoint will be a Secure Sockets Layer (SSL) connection, which will have a certificate in place. The tool evaluates the fully qualified domain name (FQDN) that was assigned to the certificate (for example, STS.Contoso.com).

The Microsoft Remote Connectivity Analyzer tool returns the following warning if the FDQN does not match the host address or URL that the client uses to make a connection with the server.


<table>
<colgroup>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>SSL Certificate Name Mismatch</p></td>
</tr>
</tbody>
</table>

The name mismatch warning means that users might not be able to authenticate correctly to their Office 365 resources. If this issue occurs, the passive (Internet Explorer) access to the Office 365 services display a certificate warning when the user accesses the services. Only after the certificate warning is accepted can the Passive client connect. The Outlook client is not presented with this certificate security warning, and the client fails to connect.

<div>

## More Information

For information about how to troubleshoot this issue, see the Microsoft Knowledge Base article 2523494, [You receive a certificate warning when you try to access Microsoft Office 365 resources by using an identity-federated account](https://support.microsoft.com/kb/2523494)

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

