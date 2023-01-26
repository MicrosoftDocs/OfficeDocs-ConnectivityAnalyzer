---
title: SSL Certificate Name Mismatch
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer displays the following warning when the FDQN does not match the host address or URL that the client uses to make a connection with the server: SSL Certificate Name Mismatch"'
ms.date: 05/08/2020
---

# SSL Certificate Name Mismatch


_**Topic Last Modified:** 2011-06-13_

The Microsoft Analyzer tool queries the Server Certificate object in the Exchange Server system to retrieve various properties on X509 certificates. For each Secure Sockets Layer (SSL) certificate found, the Remote Connectivity Analyzer tool evaluates the fully qualified domain name (FQDN) that was assigned to the certificate. For example, the tool evaluates https://www.microsoft.com.

The Microsoft Remote Connectivity Analyzer displays the following warning when the FDQN does not match the host address or URL that the client uses to make a connection with the server:


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

The name mismatch warning indicates that users might not be able to connect to their mailboxes by using Outlook Anywhere or Exchange ActiveSync for Exchange Server 2007. If this issue occurs, Microsoft Office Outlook 2007 clients receive the following certificate warning:


<table>
<colgroup>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>The name of the security certificate is invalid or does not match the name of the site.</p></td>
</tr>
</tbody>
</table>

Mobile devices typically receive an error message that resembles the following message:


<table>
<colgroup>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>The security certificate on the server is not valid. Support code: 0x80072f0d</p></td>
</tr>
</tbody>
</table>

If you are testing the Single Sign-On function within the Remote Connectivity Analyzer, you may receive a similar certificate warning. The tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. The endpoint will be a Secure Sockets Layer (SSL) connection, which will have a certificate in place. The Remote Connectivity Analyzer evaluates the fully qualified domain name (FQDN) that was assigned to the certificate. For example, the tool evaluates STS.Contoso.com.

This is a test against the Secure Communications certificate, which should not be confused with the token signing or token decrypting certificates that are used for identity federation. The token signing and decrypting certificates are not used for communications over SSL. Also, those certificates can be self-signed. The Secure Communication certificate must be a third-party certificate in order for single the sign-on process to work in most cases.

The Remote Connectivity Analyzer also displays the certificate warning if the FDQN does not match the host address or URL that the client uses to make a connection with the server. To resolve this Microsoft Office 365 issue, see Microsoft Knowledge Base article 2523494, [You receive a certificate warning when you try to access Microsoft Office 365 resources by using an identity-federated account](https://support.microsoft.com/kb/2523494)

<div>

## For More Information

  - For more information about how this error affects Outlook 2007 clients, see Microsoft Knowledge Base article 940726, [Security warning when you start Outlook 2007 and then connect to a mailbox that is hosted on a server that is running Exchange Server 2007 or Exchange Server 2010: "The name of the security certificate is invalid or does not match the name of the site"](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=940726).

  - For more information about how this error affects mobile devices that connect by using Exchange ActiveSync, see [Install SSL Certificates on a Windows Mobile Phone](https://go.microsoft.com/fwlink/?linkid=161942).

  - For more information about how to use certificates with virtual servers in Exchange Server 2003, see Microsoft Knowledge Base article 823024, [How to Use Certificates with Virtual Servers in Exchange Server 2003](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=823024).

  - For more information about how to use SSL with Exchange 2007 Client Access servers, see [White Paper: Exchange 2007 Client Access and SSL](https://go.microsoft.com/fwlink/?linkid=161943).

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors that you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why your effort failed at this point. If you require technical assistance, please create a post in the appropriate forum at [Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?linkid=73420) or contact Microsoft Product Support Services at [Fix a Technical Problem](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

