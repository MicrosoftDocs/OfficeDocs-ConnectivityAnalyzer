---
title: The Host Name Could Not be Resolved in DNS
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

# The Host Name Could Not be Resolved in DNS

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-11-09_

The Microsoft Analyzer Tool performs a Domain Name System (DNS) lookup to retrieve the Host (A) record of the host name provided. If the DNS lookup operation does not return an IP address, then the Microsoft Remote Connectivity Analyzer displays the following error message:

"The host name could not be resolved in DNS."

<div>

## For More Information

To correct this error, do the following.

  - Use nslookup to verify that the Host (A) record exists on the DNS server. For more information, see [To verify A resource records exist in DNS](https://go.microsoft.com/fwlink/?linkid=63001).

  - If the Host (A) resource record does not exist or is incorrect, then manually add or modify the host record. If your external DNS zone is hosted by a third party, you may have to contact that company or use custom tools to make these DNS modifications.

For information about how to troubleshoot DNS, see [Troubleshooting DNS](https://go.microsoft.com/fwlink/?linkid=63003).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

Sometimes, you may have to verify the URL that is used for the AD FS endpoint for Office 365 identity federation. For a procedure to determine the value to which the endpoint is currently set, see the “More Information” section of [Internet Explorer cannot display the Office 365 portal webpage when a federated user tries to sign in](https://support.microsoft.com/kb/2419389).

</div>

</div>

<span> </span>

</div>

</div>

</div>

