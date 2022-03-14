---
title: Could Not Negotiate an Appropriate Airsync Version with Server
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'If the MS-ASProtocolVersions header does not contain 2.5 or 12.0, the Microsoft Remote Connectivity Analyzer tool generates the following error: "Could not negotiate an appropriate Airsync version with server."'
---


# Could Not Negotiate an Appropriate Airsync Version with Server


_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an HTTP request using the OPTIONS verb to the Microsoft-Server-ActiveSync virtual directory on the server and analyzes the HTTP headers in the HTTP response. If the MS-ASProtocolVersions header does not contain 2.5 or 12.0, then the Microsoft Remote Connectivity Analyzer tool generates the following error:

"Could not negotiate an appropriate Airsync version with server."

<div>

## For More Information

The Microsoft Remote Connectivity Analyzer currently supports Exchange ActiveSync protocol versions 2.5 and 12.0. If you are using Exchange Server 2003 SP1 or earlier, then this error does not necessarily indicate a problem. Rather, it simply indicates that the tool is not able to properly test your server. Upgrade to Exchange Sever 2003 Service Pack 2 to get the ActiveSync v2.5 functionality.

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

