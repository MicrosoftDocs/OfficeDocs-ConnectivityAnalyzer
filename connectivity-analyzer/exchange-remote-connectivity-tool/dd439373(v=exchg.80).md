---
title: Access is Denied Error was Thrown by the RPC Runtime
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

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Access is Denied Error was Thrown by the RPC Runtime

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2010-08-26_

The Microsoft Exchange Best Practices Analyzer Tool issues an RPC ping to each of the RPC interfaces that are used by Microsoft Office Outlook to connect to the Mailbox server. When the RPC ping request fails with the RPC status 0x5, the Exchange Remote Connectivity Analyzer tool displays the following error message:

"Access is denied error (0x5) was thrown by the RPC runtime."

<div>

## For More Information

**To correct this error**

1.  Analyze the LAN Manager Authentication Level (LMCompatibilityLevel) on the Outlook Clients, the Exchange Servers, and the Global Catalog Servers. Make sure that these settings are configured in a compatible combination.

2.  Make sure that replication is working properly between domain controllers. This especially important if you have multiple domains in your forest. Check the directory service logs on the domain controllers and use the DCDIAG tool to check your domain controllers for errors.

3.  Make sure appropriate user rights are granted for the Exchange mailbox or back-end server in question. For example, "Access this computer from the network" is a required right to be able to log in correctly.

For more information about how to configure the security settings that are mentioned in this topic, see Microsoft Knowledge Base article, [Client, service, and program incompatibilities that may occur when you modify security settings and user rights assignments](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=823659).

For more information about the use and analysis of the DCDIAG tool, see [Dcdiag Overview](http://go.microsoft.com/fwlink/?linkid=68936).

The Exchange Remote Connectivity Analyzer is a new tool that has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional information about why you failed at this point. If you require technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

