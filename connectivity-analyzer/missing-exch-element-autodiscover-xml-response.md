---
title: Missing EXCH Element in Autodiscover XML Response
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

# Missing EXCH Element in Autodiscover XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-02-07_

The Microsoft Remote Connectivity Analyzer Tool queries the HTTP response from the Autodiscover service to determine the attributes that are contained in the XML within that response. The following Microsoft Office Outlook providers and their attributes are commonly found in the XML.

  - **EXCH Provider**  
    The connection settings and Exchange services URLs that are used when Outlook connects by using RPC over TCP

<!-- end list -->

  - **EXPR Provider**  
    The connection settings and Exchange services URLs that are used when Outlook connects by using RPC over HTTP (Outlook Anywhere)

If the EXCH element is missing from the Autodiscover response, the Remote Connectivity Analyzer displays the following error message:

Missing EXCH element in Autodiscover XML Response

<div>

## For More Information

The EXCH element in the Autodiscover XML contains information that is used by the Outlook client to establish RPC over TCP connections to the server that is running Exchange Server. These connections are typically internal to the corporate network. However, the EXCH section is also required when you connect by using RPC over HTTP (Outlook Anywhere).

If the EXCH element is missing, MAPI access may be disabled for the user. To check whether a user is enabled for MAPI access to the mailbox, run the following command in the Exchange Management Shell:

    Get-CASMailbox MailboxName | fl MapiEnabled

If the command returns $false, you must enable MAPI for the mailbox or select an alternative connection method. To enable MAPI for the mailbox, run the following command:

    Set-CASMailbox MailboxName -MapiEnabled:$true

The Remote Connectivity Analyzer is a new tool that has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why your efforts failed at this point. If you require technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420), or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

<div>

## See Also

#### Concepts

[Missing EXPR Element in Autodiscover XML Response](missing-expr-element-autodiscover-xml-response.md)  
[MAPI Connections are Not Allowed](mapi-connections-are-not-allowed.md)  

#### Other Resources

[Set-CasMailbox](https://technet.microsoft.com/library/bb125264.aspx)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

