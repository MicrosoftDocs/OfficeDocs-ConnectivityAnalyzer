---
title: An Unexpected Redirect Response was Received
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

# An Unexpected Redirect Response was Received

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer Tool sends an HTTP request to the Exchange Server to verify that it can successfully connect to features including Outlook Web Access, Exchange ActiveSync, and Outlook Anywhere. A successful response should appear as an HTTP 200 (or 207). When the Exchange Remote Connectivity Analyzer receives a redirect response (that is, 301, 302, 302) instead of a 200 or 207, it displays the following error message.

"An unexpected Redirect Response was received."

This error message indicates that you have an HTTP redirect configured in IIS for one or more Exchange applications in a manner that is not expected or supported.

<div>

## For More Information

  - For more information about configuring redirection for Outlook Web Access, see [How to Simplify the Outlook Web Access URL](http://go.microsoft.com/fwlink/?linkid=130623).

  - For more information about configuring redirection for Autodiscover, see [White Paper: Exchange 2007 Autodiscover Service](http://go.microsoft.com/fwlink/?linkid=85214).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

