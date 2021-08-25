---
title: Anonymous Authentication Enabled for Virtual Directory
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

# Anonymous Authentication Enabled for Virtual Directory

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an anonymous HTTP request from the remote server to the URL being tested. If the request succeeds but anonymous access should not be allowed on this virtual directory, then the Microsoft Remote Connectivity Analyzer tool displays the following error message.

"Anonymous authentication enabled for virtual directory."

Outlook Web Access, Exchange ActiveSync, Outlook Anywhere or RPC over HTTPS, Autodiscover and other Exchange Web Services including the Availability Service and Web-distributed Offline Address Books require specific authentication methods. If Anonymous access is allowed in lieu of, or in addition to, other required authentication methods, then your server isn't as secure from a security perspective and unexpected results can occur.

<div>

## For More Information

To resolve this issue, review the following documentation and confirm that the virtual directories on your Exchange server have the proper authentication methods enabled for each application or service.

  - To see a list of the default authentication methods for Exchange Server 2007 applications and services, see [Default settings for Exchange-related virtual directories in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=161402).

  - For information about the supported authentication methods available for managing Exchange applications hosted on an Exchange 2007 Client Access Server, see the following documentation on TechNet: [Managing Client Access Security](https://go.microsoft.com/fwlink/?linkid=100585).

  - For more information about configuring authentication specific to Exchange 2007 Outlook Anywhere, see [How to Configure Authentication for Outlook Anywhere](https://go.microsoft.com/fwlink/?linkid=161403).

  - For information about configuring authentication for Web applications on Exchange Server 2003 and Exchange 2000 Server, see [Front-End and Back-End Server Topology Guide for Microsoft Exchange Server 2003 and Exchange 2000 Server](https://go.microsoft.com/fwlink/?linkid=161404).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

