---
title: Expected Service Banner was not Received when Connecting
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

# Expected Service Banner was not Received when Connecting

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer tool attempts to connect to the Exchange SMTP server. Upon a successful connection, an SMTP Banner is returned from the SMTP server. If this banner is never returned due to a timeout or other issue, then the following message is displayed.

"Expected Service Banner was not received when connecting."

<div>

## For More Information

If you are using a mail-relay or SMTP filter (available on many firewall products), you should begin your investigation with those products. Consider disabling or bypassing those products for troubleshooting purposes.

  - If you are not using a mail-relay or SMTP filter, then you may want to ensure that the appropriate process is listening on port 25 (SMTP). Use the netstat.exe utility to determine whether the appropriate service is actually listening on the port being tested using Microsoft Knowledge Base article "How To Determine Which Program Uses or Blocks Specific Transmission Control Protocol Ports in Windows Server 2003" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=323352](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=323352)).

  - For Exchange Server 2003, the process name should be inetinfo.exe. For Exchange Server 2007, the process name should be edgetransport.exe.

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

