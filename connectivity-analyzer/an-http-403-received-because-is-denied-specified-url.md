---
title: An HTTP 403 was Received Because ISA Denied the Specified URL
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'Error: The server denied the specified Uniform Resource Locator (URL)'
ms.date: 05/08/2020
---

# An HTTP 403 was Received Because ISA Denied the Specified URL


_**Topic Last Modified:** 2009-11-17_

The Microsoft Remote Connectivity Analyzer sends an HTTP request and validates the response it receives to verify connectivity. If the entry point to the Exchange Server is an ISA server, and the publishing rules on the ISA server are not configured correctly, then ISA may send an HTTP 403 Forbidden response. If ISA sends an HTTP 403 response, then the Microsoft Remote Exchange Connectivity tool displays the following message:

"The server denied the specified Uniform Resource Locator (URL)."

End users will not be able to successfully connect to Exchange applications and services.

<div>

## For More Information

There can be multiple reasons for this error with the most likely being a misconfigured ISA server.

<div class="alert">


> [!NOTE]
> If using ISA 2000, we recommend upgrading to ISA 2006. If upgrading is not an option, then on the OWA web publishing rule you must remove all Path entries and replace it with only "/*".


</div>

**To correct this error**

1.  Follow the steps in Microsoft Knowledge Base article, "How to publish a Microsoft Exchange server for Outlook Web Access in ISA Server 2006, in ISA Server 2004, or in Microsoft Forefront Threat Management Gateway, Medium Business Edition" ([https://go.microsoft.com/fwlink/?LinkID=3052\&kbid=837354](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=837354)).

2.  If you have applied the steps from the preceding article and are still receiving the error, see Microsoft Knowledge Base article "A user cannot access a Web site that is published in ISA Server 2006 by using Kerberos constrained delegation if the user is not in the same domain as the ISA Server computer" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=942637](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=942637)) and "Error message when a user visits Web site that is published by using Microsoft ISA Server together with client certificate authentication: Error Code: 403 Forbidden" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=947124](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=947124)).

If the entry point to your Exchange Server is ISA Server 2006, then check the publishing rule to determine whether the rule is configured to disallow all authentications. Go to the Delegation tab and view the drop-down list beneath "Method used by ISA Server to authenticate to the published Web server". The option "No delegation and Client may not authenticate directly" disables any authentication on the rule. Since all Exchange services require some type of authentication, choose a different delegation method from the drop-down menu that suits your environment.

<div class="alert">


> [!NOTE]
> This issue can also be related to a problem with the destination set. Verify that the destination set points to the external IP address.


</div>

Example:

Destination Set Name: OWA

Description: Outlook Web Access

SingleIP: \<internal IP of Exchange server\> (change to external IP on ISA)

Path: /exchange\*

SingleIP: \<internal IP of Exchange server\> (change to external IP on ISA)

Path: /exchweb\*

SingleIP: \<internal IP of Exchange server\> (change to external IP on ISA)

Path: /public\*

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

