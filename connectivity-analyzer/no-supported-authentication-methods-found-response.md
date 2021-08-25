---
title: No Supported Authentication Methods Found in Response
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

# No Supported Authentication Methods Found in Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-05-21_

The Microsoft Remote Connectivity Analyzer sends an HTTP request to test the authentication methods of a specified service. If a 401 unauthorized response is received, the Analyzer expects certain WWW-Authenticate headers in the response. These headers indicate the supported authentication methods for the service. If no WWW-Authenticate headers are received, the Analyzer generates the following error:

"No supported Authentication Methods found in Response"

This issue will prevent users from being able to successfully connect to the specified service.

<div>

## For More Information

To resolve this issue, do the following:

1.  Confirm that the proper authentication methods are selected for the virtual directories in IIS.
    
      - To see a list of the default authentication methods for Exchange Server 2007 applications and services, see the Exchange Team Blog article [Default settings for Exchange-related virtual directories in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=161402).
    
      - For information about the supported authentication methods available for managing Exchange applications hosted on an Exchange 2007 Client Access server, see [Managing Client Access Security](https://go.microsoft.com/fwlink/?linkid=100585).
    
      - For more information about how to configure authentication specific to Exchange 2007 Outlook Anywhere, see [Configure Authentication for Outlook Anywhere](https://go.microsoft.com/fwlink/?linkid=161403).
    
      - For information about configuring authentication for Web applications in Exchange Server 2003 and in Exchange 2000 Server, see [Front-End and Back-End Server Topology Guide for Microsoft Exchange Server 2003 and Exchange 2000 Server](https://go.microsoft.com/fwlink/?linkid=161404).

2.  If the entry point to your Exchange server is ISA Server 2006, check the publishing rule to determine whether the rule is configured to disallow all authentication. Go to the delegation tab and view the list beneath "Method used by ISA Server to authenticate to the published Web server." The "No delegation and Client may not authenticate directly" option disables any authentication on the rule. Because all Exchange Services require some type of authentication, select on the menu a different delegation method that suits your environment.

For more information about how to publish Exchange 2007 Services through Microsoft ISA Server 2006, see [Publishing Exchange Server 2007 with ISA Server 2006](https://technet.microsoft.com/library/bb794751.aspx).

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

