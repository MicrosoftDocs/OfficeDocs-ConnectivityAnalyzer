---
title: Missing EXPR Element in Autodiscover XML Response
TOCTitle: Missing EXPR Element in Autodiscover XML Response
ms:assetid: cdd6809e-b5dc-49e5-b977-750ccec1e1eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439390(v=EXCHG.80)
ms:contentKeyID: 20045837
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Missing EXPR Element in Autodiscover XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-02-10_

The Microsoft Exchange Analyzer Tool queries the HTTP response from the Autodiscover service to determine the attributes contained in the XML within that response. Two Outlook Providers and their attributes are commonly found in the XML:

  - **EXCH Provider**  
    The connection settings and Exchange services URLs used when Outlook connects using RPC.

<!-- end list -->

  - **EXPR Provider**  
    The connection settings and Exchange services URLs used when Outlook connects using HTTP (Outlook Anywhere).

If the EXPR element is missing from the Autodiscover response, then the Exchange Remote Connectivity Analyzer tool displays the following error message:

"Missing EXPR element in Autodiscover XML Response."

This typically means that Outlook Anywhere is either not enabled or configured correctly.

<div>

## For More Information

  - For more information about deploying Outlook Anywhere, see [Deploying Outlook Anywhere](http://go.microsoft.com/fwlink/?linkid=80831).

  - For more information about the Outlook Providers, see [The Autodiscover Service and Outlook Providers - how does this stuff work?](http://go.microsoft.com/fwlink/?linkid=161811)

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

