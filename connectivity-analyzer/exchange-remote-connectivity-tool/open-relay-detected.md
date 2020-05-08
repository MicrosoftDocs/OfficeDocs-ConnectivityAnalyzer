---
title: Open Relay Detected
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

# Open Relay Detected

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer tool attempts to send a test message using a recipient address that does not belong to the Exchange organization. If this operation succeeds, then the SMTP Server operates as an open relay and the following message is returned from the test.

"Open relay test message delivered successfully to Admin@TestExchangeConnectivity.com"

A computer that is running Microsoft Exchange 2000 Server, Exchange Server 2003 or Exchange Server 2007 can be configured as a mail relay, which is not recommended.

An Exchange computer that is configured as an open mail relay may be used to send unsolicited commercial e-mail, also known as spam. If other mail servers identify your Exchange computer as an unsolicited commercial e-mail server, then your Exchange computer may be added to block lists.

<div>

## For More Information

To resolve this issue, see the following Exchange Best Practices Analyzer article [SMTP server failed open relay test](http://go.microsoft.com/fwlink/?linkid=161823).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

