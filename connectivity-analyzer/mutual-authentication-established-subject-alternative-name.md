---
title: Mutual Authentication Established by Subject Alternative Name
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

# Mutual Authentication Established by Subject Alternative Name

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-02-07_

The Microsoft Remote Connectivity Analyzer tool negotiates a Secure Sockets Layer (SSL) connection together with the remote host to retrieve various properties on X509 certificates. The tool evaluates the Subject attribute and Subject Alternative Name extension to identify the principal names that are assigned to the certificate (for example, mail.contoso.com).

If the certificate Common Name does not match the Mutual Authentication (msstd:) string that is obtained by the Remote Connectivity Analyzer when it tests Microsoft Outlook Anywhere functionality, but one of the Subject Alternative Name extensions does match the Mutual Authentication string, the tool displays the following error message:

"The certificate common name doesn't match the mutual authentication string provided; however, a match was found in the subject alternative name extension."

The Mutual Authentication string is equivalent to the "Only connect to proxy servers that have this principal name in their certificate" setting in the **Exchange Proxy Settings** dialog box in Outlook. The Remote Procedure Call (RPC) component in Windows uses this value to validate the certificate. Prior to Windows Vista Service Pack 1, the Windows platform validated the Mutual Authentication string only against the certificate common name and not against the Subject Alternative Name entries.

The following symptoms may be experienced by Windows XP clients and by Windows Vista RTM clients in this configuration.

  - You are repeatedly prompted for credentials, and you cannot connect to Microsoft Exchange Server by using Outlook Anywhere.

  - You receive the following error message when you let Outlook 2007 create the Outlook profile by using Autodiscover:
    
    An encrypted connection to your mail server is not available. Click Next to attempt using an unencrypted connection.

If you plan to support only clients that run Windows Vista Service Pack 1 and newer versions of Windows, you can safely ignore this warning.

<div>

## For More Information

  - For more information about this issue, see [Mutual Authentication Could Not be Established](mutual-authentication-could-not-be-established.md).

  - To learn more about Mutual Authentication Principal Names, see [Principal Names](https://go.microsoft.com/fwlink/?linkid=93417).

  - To learn more about Exchange 2007 Outlook Providers, see the following topic and Microsoft Exchange Team Blog article:
    
      - [Set-OutlookProvider](https://go.microsoft.com/fwlink/?linkid=161815)
    
      - [The Autodiscover Service and Outlook Providers - how does this stuff work?](https://go.microsoft.com/fwlink/?linkid=161811)

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors that you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why your efforts failed at this point.  If you require technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

