---
title: Expected Service Banner was not Received when Connecting
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'Microsoft Remote Connectivity Analyzer message: Expected service banner was not received when connecting'
ms.date: 05/08/2020
---

# Expected Service Banner was not Received when Connecting


_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer attempts to connect to the Exchange SMTP server. Upon a successful connection, an SMTP Banner is returned from the SMTP server. If this banner is never returned due to a timeout or other issue, then the following message is displayed.

"Expected Service Banner was not received when connecting."

## For More Information

If you are using a mail-relay or SMTP filter (available on many firewall products), you should begin your investigation with those products. Consider disabling or bypassing those products for troubleshooting purposes.

  - If you are not using a mail-relay or SMTP filter, then you may want to ensure that the appropriate process is listening on port 25 (SMTP). Use the netstat.exe utility to determine whether the appropriate service is actually listening on the port being tested using Microsoft Knowledge Base article [How To Determine Which Program Uses or Blocks Specific Transmission Control Protocol Ports in Windows Server 2003](https://go.microsoft.com/fwlink/?linkid=3052\&kbid=32335).

  - For Exchange Server 2003, the process name should be inetinfo.exe. For Exchange Server 2007, the process name should be edgetransport.exe.

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
