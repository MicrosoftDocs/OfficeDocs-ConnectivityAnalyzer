---
title: The MobileSync Autodiscover Provider Returned an Error Status in the XML Response
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# The MobileSync Autodiscover Provider Returned an Error Status in the XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-19_

The Microsoft Exchange Analyzer Tool sends an Autodiscover XML/HTTP request to the Exchange Autodiscover service using the MobileSync provider schema to locate mobile device settings for the specified user. When an error status message is present in the response, the Exchange Remote Connectivity Analyzer displays the following error:

"The MobileSync Autodiscover provider returned an error status in the XML response."

<div>

## For More Information

The following error messages can be returned from the Exchange ActiveSync (MobileSync) Autodiscover provider:

  - "Active Directory currently not available"

  - "Cannot find mobile mailbox"

  - "Autodiscover cannot process the given e-mail address. Only mailboxes and contacts can be used for MobileSync."

  - "Cannot find the e-mail address"

There is a known issue in Exchange Server 2007 that causes the error "Active Directory currently not available" when you have Client Access servers in Active Directory sites that are not Internet-facing. Internet-facing Client Access servers are determined by the presence of the ExternalUrl attribute on the ActiveSync virtual directory. If the ExternalUrl is not set, then the CAS Client Access server is not considered "Internet-facing." This issue is fixed in Exchange 2007 SP1 RU4. For more information about this specific issue, see Microsoft Knowledge Base article "The Autodiscover service for ActiveSync in an Exchange 2007 environment does not work for users in sites that do not have the ExternalURL property set" ([The Autodiscover service for ActiveSync in an Exchange 2007 environment does not work for users in sites that do not have the ExternalURL property set](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=952152)).

For more information about Internet-facing and non Internet-facing Client Access servers, see [Understanding Proxying and Redirection](https://go.microsoft.com/fwlink/?linkid=105411).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

