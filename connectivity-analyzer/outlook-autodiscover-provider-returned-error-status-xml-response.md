---
title: The Outlook Autodiscover Provider Returned an Error Status in the XML Response
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

# The Outlook Autodiscover Provider Returned an Error Status in the XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-02-24_

The Microsoft Remote Connectivity Analyzer sends an Autodiscover XML/HTTP request to the Exchange Autodiscover service using the Outlook provider schema to locate Outlook settings for the specified user. When an error status message is present in the response, the Microsoft Remote Connectivity Analyzer generates the following error:

"The Outlook Autodiscover provider returned an error status in the XML response."

The Autodiscover service is used by Microsoft Office Outlook 2007 and later versions to automatically configure connection settings and locate the URLs for Exchange services including the Availability service, Out of Office Assistant, Web-distributed Offline Address Books, and Unified Messaging. If Outlook is unable to successfully connect to the Autodiscover service, then you will not be able to automatically create your profile settings or connect to the Exchange services.

<div>

## For More Information

The following error messages can be returned from the Exchange Autodiscover service:

  - "Autodiscover cannot process the given e-mail address. Only mailboxes and contacts are allowed."

  - "The e-mail address cannot be found."

  - "Client mailboxes must be on Exchange 2007 Server or later."

To resolve this issue, confirm that the account you are using has an Exchange 2007 mailbox and is stamped with a valid e-mail address.

For more information about the Autodiscover service, see [White Paper: Exchange 2007 Autodiscover Service](https://go.microsoft.com/fwlink/?linkid=157773).

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

