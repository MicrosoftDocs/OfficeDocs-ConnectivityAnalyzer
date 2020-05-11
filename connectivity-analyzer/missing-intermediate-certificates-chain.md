---
title: Missing Intermediate Certificates in Chain
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

# Missing Intermediate Certificates in Chain

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-09-01_

The Microsoft Exchange Analyzer tool queries the Server Certificate object in the Exchange server system to retrieve various properties on X509 certificates. In order for the Exchange Remote Connectivity Analyzer tool to validate a given X509 certificate, it must trust the root Certificate Authority (CA) that issued the certificate. If the Exchange Remote Connectivity Analyzer is unable to follow the certificate chain to the trusted root, then it displays an error that the certificate is not trusted.

This issue may occur because an intermediate certification authority (CA) certificate is not present on the device or on the Exchange Server with which you are synchronizing.

This issue is particularly common with Go Daddy certificates because either the root CA certificate or the intermediate CA certificate is missing from the certificate store on the server that is running Windows Server 2003 or Windows Server 2008. This issue also frequently occurs with VeriSign certificates because the intermediate CA certificate in the certificate store on the Windows Server is expired.

Common symptoms of this issue include the following:

When you try to synchronize a Microsoft Windows Mobile-based device by using Exchange ActiveSync for Microsoft Exchange Server 2003 or for Microsoft Exchange Server 2007, synchronization is not successful and you receive one of the following error messages.

  - Synchronization failed. The security certificate on the server has expired. Check that the date and time on the device is correct and try again. Error code: 80072f05 or 0x80072f05.

  - The security certificate on the server is invalid. Contact your Exchange Server administrator or ISP to install a valid certificate on the server. Support Code: 80072F0D or 0x80072f0d.

<div>

## For More Information

You can use the SSLChainSaver utility to determine which certificates are missing. To learn more about the SSLChainSaver utility, refer to the following topics:

  - For more information about the SSLChainSaver utility from the Windows Mobile team, see the Windows Mobile team blog posts, "[Introducing the SslChainSaver](https://go.microsoft.com/fwlink/?linkid=161816)" and "[SSLChainSaver v2 released](https://go.microsoft.com/fwlink/?linkid=161817)."

  - Click [here](https://go.microsoft.com/fwlink/?linkid=161818) to obtain the Windows Mobile SSLChainSaver from the Microsoft download site.

  - For more information about this issue, see Microsoft Knowledge Base article, ["Error message when you try to synchronize a Windows Mobile-based device by using Exchange ActiveSync for Exchange 2003 or for Exchange 2007: 'Synchronization failed'](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=927465)."

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

