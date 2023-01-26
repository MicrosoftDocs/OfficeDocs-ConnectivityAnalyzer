---
title: Could Not Find MS-Server-ActiveSync Header in OPTIONS Response
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'When the MS-Server-ActiveSync header is missing in the HTTP response, the Microsoft Remote Connectivity Analyzer tool generates the following error: "Could not find MS-Server-ActiveSync header in OPTIONS response."'
ms.date: 05/08/2020
---

# Could Not Find MS-Server-ActiveSync Header in OPTIONS Response


_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an HTTP request with the OPTIONS verb to the Microsoft-Server-ActiveSync virtual directory and analyzes the HTTP headers in the response. When the MS-Server-ActiveSync header is missing in the HTTP response, the Microsoft Remote Connectivity Analyzer tool generates the following error:

"Could not find MS-Server-ActiveSync header in OPTIONS response."

This issue is typically the result of a firewall or reverse proxy that either does not support the OPTIONS verb or is not configured to send it. Another potential source of this issue is when you install URLScan and configure it to block the OPTIONS verb. In either case, this issue results in mobile device users being unable to successfully connect to Exchange ActiveSync.

<div>

## For More Information

To correct this error, do one of the following:

  - If you are using Internet Security Acceleration (ISA) Server 2000, see Microsoft Knowledge Base article "The ISA Server response to client options requests is limited to a predefined set" ([https://go.microsoft.com/fwlink/?linkid=3052\&kbid=304340](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=304340)).

  - If you are using a third-party reverse proxy, then contact the vendor to confirm support of, or proper configuration for supporting, the OPTIONS verb.

  - For information about configuring the URLScan tool, see Microsoft Knowledge Base article "How to configure the URLScan Tool" ([https://go.microsoft.com/fwlink/?linkid=3052\&kbid=326444](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=326444)).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

