---
title: Missing Intermediate Certificates in Chain
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: Intermediate certificates missing in chain
ms.date: 05/08/2020
---

# Missing Intermediate Certificates in Chain


_**Topic Last Modified:** 2009-09-01_

The Microsoft Remote Connectivity Analyzer queries the Server Certificate object in the Exchange server system to retrieve various properties on X509 certificates. In order for the Microsoft Remote Connectivity Analyzer tool to validate a given X509 certificate, it must trust the root Certificate Authority (CA) that issued the certificate. If the Microsoft Remote Connectivity Analyzer is unable to follow the certificate chain to the trusted root, then it displays an error that the certificate is not trusted.

This issue may occur because an intermediate certification authority (CA) certificate is not present on the device or on the Exchange Server with which you are synchronizing.

This issue is particularly common with Go Daddy certificates because either the root CA certificate or the intermediate CA certificate is missing from the certificate store on the server that is running Windows Server 2003 or Windows Server 2008. This issue also frequently occurs with VeriSign certificates because the intermediate CA certificate in the certificate store on the Windows Server is expired.

Common symptoms of this issue include the following:

When you try to synchronize a Microsoft Windows Mobile-based device by using Exchange ActiveSync for Microsoft Exchange Server 2003 or for Microsoft Exchange Server 2007, synchronization is not successful and you receive one of the following error messages.

  - Synchronization failed. The security certificate on the server has expired. Check that the date and time on the device is correct and try again. Error code: 80072f05 or 0x80072f05.

  - The security certificate on the server is invalid. Contact your Exchange Server administrator or ISP to install a valid certificate on the server. Support Code: 80072F0D or 0x80072f0d.

## For More Information

Consult the guidance provided by your certificate authority for how to install your certificate and choose the most compatible certificate chain for your clients. Some certificate authorities have utilities that can check your certificate installation and select which chain to send (if there are multiple options).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
