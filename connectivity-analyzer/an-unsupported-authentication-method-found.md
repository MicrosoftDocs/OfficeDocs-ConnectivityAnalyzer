---
title: An Unsupported Authentication Method was Found
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# An Unsupported Authentication Method was Found

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an HTTP GET request to test the authentication methods of the specified service using the URL entered during the test. When the Exchange Server receives the request, it responds with a list of accepted authentication methods. This list is contained in the WWW-Authenticate field of the response header. If an unsupported authentication method is returned in this list, then the following error may be displayed.

"Authentication method "0" is enabled but is not an allowed Authentication method for this service."

Where "0" is replaced with the unsupported authentication method(s) that were found.

This error will prevent users from being able to successfully connect to the specified service.

<div>

## For More Information

The primary reason this error is reported is when testing Exchange ActiveSync and Integrated Windows Authentication is advertised by the server. Integrated Windows Authentication is not a supported Authentication method for Exchange ActiveSync and can cause Windows Mobile devices previous to Windows Mobile 6.0 to fail to connect.

<div class="alert">


> [!NOTE]
> If you are using ISA Server to perform pre-authentication, Integrated Authentication may be enabled on the Web Listener. If you do not plan to support devices older than Windows Mobile 6.0 (or if you are not experiencing problems), then you can ignore this error.


</div>

**To correct this error**

1.  Confirm that the proper authentication methods are selected for the virtual directories in IIS.

2.  To see a list of the default authentication methods for Exchange Server 2007 applications and services, see [Default settings for Exchange-related virtual directories in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=161402)

3.  For information about the supported authentication methods available for managing Exchange applications hosted on an Exchange 2007 Client Access Server, see [Managing Client Access Security](https://go.microsoft.com/fwlink/?linkid=100585).

4.  For more information about configuring authentication specific to Exchange 2007 Outlook Anywhere, see [How to Configure Authentication for Outlook Anywhere](https://go.microsoft.com/fwlink/?linkid=161403).

5.  For information about configuring authentication for Web applications on Exchange Server 2003 and Exchange 2000 Server, see [Front-End and Back-End Server Topology Guide for Microsoft Exchange Server 2003 and Exchange 2000 Server](https://go.microsoft.com/fwlink/?linkid=161404).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

