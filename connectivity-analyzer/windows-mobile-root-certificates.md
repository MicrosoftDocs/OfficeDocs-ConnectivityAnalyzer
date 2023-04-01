---
title: Windows Mobile Root Certificates
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'If the Microsoft Remote Connectivity Analyzer is unable to follow the certificate chain to the trusted root, then it displays the following error: "The security certificate on the server is not valid. Support code: 0x80072f0d."'
ms.date: 05/08/2020
---

# Windows Mobile Root Certificates


_**Topic Last Modified:** 2009-09-01_

The Microsoft Remote Connectivity Analyzer queries the Server Certificate object in the Exchange Server system to retrieve various properties on X509 certificates. In order for the Microsoft Remote Connectivity Analyzer to validate a given X509 certificate, it must trust the root Certificate Authority (CA) that issued the certificate. If the Microsoft Remote Connectivity Analyzer is unable to follow the certificate chain to the trusted root, then it displays the following error:

"The security certificate on the server is not valid. Support code: 0x80072f0d."

This issue typically occurs when the Web server certificate on the Exchange 2007 Client Access server is a self-signed certificate or one created using a private or internal PKI. If you are using a self-signed or a certificate from an internal PKI, then you must install the root certificate on the mobile device. If you have already done this step, then you can choose the "Ignore Trust for SSL" option in the Microsoft Remote Connectivity Analyzer to bypass this check.

This issue can also occur when the certificate chain of your certificate does not end in a root certificate that is trusted on your version of Windows Mobile.

The following table shows which root certificates from public certificate authorities ship with each version of Windows Mobile.

Certificate Authority | 5.0 | 5.0 + MSFP | 6.0
----------------------|-----|------------|-----
Thawte Server CA| Yes | Yes | Yes | 
Thawte Premium Server CA | Yes | Yes | Yes
GTE CyberTrust Root | Yes | Yes | Yes
GTE CyberTrust Global Root | Yes | Yes |Yes
Secure Server Certification Authority (RSA) | Yes | Yes | Yes
GlobalSign Root CA | Yes | Yes | Yes
Entrust.net Secure Server Certification Authority | Yes | Yes |Yes
Entrust.net Certification Authority (2048) | Yes | Yes | Yes
Verisign Class 3 Public Primary Certification Authority | Yes | Yes | Yes
Verisign Class 2 Public Primary Certification Authority | Yes | Yes | Yes
Equifax Secure Certificate Authority | Yes | Yes | Yes
ValiCert Class 2 Policy Validation Authority | No | Yes | Yes
AAA Certificate Services (Comodo CA Limited) | No | No | Yes
AddTrust External CA Root | No | No | Yes
Baltimore CyberTrust Root | No | No | Yes
Go Daddy Class 2 Certification Authority | No | No | Yes
Starfield Class 2 Certification Authority | No | No | Yes

> [!NOTE]
> Some of the Certificate Authorities mentioned have CA certificates that are signed by another Certificate Authority. Though some root certificates are not trusted on older versions of Windows Mobile, this does not mean that the certificates issued from a given company do not chain up to a trusted root on that Windows Mobile version. You should contact your Certificate Authority if you have questions about which root certificates your certificate can chain to.

## For More Information

To learn more about certificates and validation, see to the following topics:

  - For more information about using certificates for securing communications between a client and a Client Access server, see [Understanding SSL for Client Access Servers](https://go.microsoft.com/fwlink/?linkid=115184).

  - For more information about the use of certificates in Exchange Server 2007, see [Certificate Use in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=119030).

  - For more information about self-signed certificates in Exchange Server 2007, see [Understanding the Self-Signed Certificate in Exchange 2007](https://go.microsoft.com/fwlink/?linkid=161990).

  - For more information about installing digital root certificates on mobile devices, see [How to Install Root Certification Authority Certificates on a Windows Mobile-based Device](https://go.microsoft.com/fwlink/?linkid=161942).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
