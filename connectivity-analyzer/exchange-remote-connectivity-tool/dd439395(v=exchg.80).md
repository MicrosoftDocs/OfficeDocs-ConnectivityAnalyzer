---
title: Anonymous Authentication Enabled for Virtual Directory
TOCTitle: Anonymous Authentication Enabled for Virtual Directory
ms:assetid: ed0d4b63-43b8-4a06-bb01-ee7ec1fd9650
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439395(v=EXCHG.80)
ms:contentKeyID: 20045842
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Anonymous Authentication Enabled for Virtual Directory

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer tool sends an anonymous HTTP request from the remote server to the URL being tested. If the request succeeds but anonymous access should not be allowed on this virtual directory, then the Exchange Remote Connectivity Analyzer tool displays the following error message.

"Anonymous authentication enabled for virtual directory."

Outlook Web Access, Exchange ActiveSync, Outlook Anywhere or RPC over HTTPS, Autodiscover and other Exchange Web Services including the Availability Service and Web-distributed Offline Address Books require specific authentication methods. If Anonymous access is allowed in lieu of, or in addition to, other required authentication methods, then your server isn't as secure from a security perspective and unexpected results can occur.

<div>

## For More Information

To resolve this issue, review the following documentation and confirm that the virtual directories on your Exchange server have the proper authentication methods enabled for each application or service.

  - To see a list of the default authentication methods for Exchange Server 2007 applications and services, see [Default settings for Exchange-related virtual directories in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=161402).

  - For information about the supported authentication methods available for managing Exchange applications hosted on an Exchange 2007 Client Access Server, see the following documentation on TechNet: [Managing Client Access Security](http://go.microsoft.com/fwlink/?linkid=100585).

  - For more information about configuring authentication specific to Exchange 2007 Outlook Anywhere, see [How to Configure Authentication for Outlook Anywhere](http://go.microsoft.com/fwlink/?linkid=161403).

  - For information about configuring authentication for Web applications on Exchange Server 2003 and Exchange 2000 Server, see [Front-End and Back-End Server Topology Guide for Microsoft Exchange Server 2003 and Exchange 2000 Server](http://go.microsoft.com/fwlink/?linkid=161404).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

