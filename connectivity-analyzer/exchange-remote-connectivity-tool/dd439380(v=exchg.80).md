---
title: A Positive HTTP Response Other than a Redirect Response was Received
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

# A Positive HTTP Response Other than a Redirect Response was Received

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-17_

The Microsoft Exchange Analyzer Tool sends an HTTP request to the Client Access Server when attempting to contact Autodiscover via the HTTP redirect method. During this test, the only acceptable type of response is an HTTP redirection; any other status code indicates a problem. An expected redirect response would be a status code of 301, 302, or 307. When any other response is received, the Exchange Remote Connectivity Analyzer reports the following error:

"A positive HTTP response other than a redirect response was received."

<div>

## For More Information

  - For more information about configuring redirection for Outlook Web Access, see "How to Simplify the Outlook Web Access URL" (<http://go.microsoft.com/fwlink/?linkid=130623>).

For more information about configuring redirection for Autodiscover, see "White Paper: Exchange 2007 Autodiscover Service" (<http://go.microsoft.com/fwlink/?linkid=85214>).

The Exchange Remote Connectivity is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

