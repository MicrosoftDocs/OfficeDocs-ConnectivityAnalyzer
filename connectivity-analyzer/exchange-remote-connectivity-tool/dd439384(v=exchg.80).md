---
title: Could Not Find MS-Server-ActiveSync Header in OPTIONS Response
TOCTitle: Could Not Find MS-Server-ActiveSync Header in OPTIONS Response
ms:assetid: b13d5173-7491-4238-a513-6a7f2390aee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439384(v=EXCHG.80)
ms:contentKeyID: 20045831
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Could Not Find MS-Server-ActiveSync Header in OPTIONS Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer Tool sends an HTTP request with the OPTIONS verb to the Microsoft-Server-ActiveSync virtual directory and analyzes the HTTP headers in the response. When the MS-Server-ActiveSync header is missing in the HTTP response, the Exchange Remote Connectivity Analyzer tool generates the following error:

"Could not find MS-Server-ActiveSync header in OPTIONS response."

This issue is typically the result of a firewall or reverse proxy that either does not support the OPTIONS verb or is not configured to send it. Another potential source of this issue is when you install URLScan and configure it to block the OPTIONS verb. In either case, this issue results in mobile device users being unable to successfully connect to Exchange ActiveSync.

<div>

## For More Information

To correct this error, do one of the following:

  - If you are using Internet Security Acceleration (ISA) Server 2000, see Microsoft Knowledge Base article "The ISA Server response to client options requests is limited to a predefined set" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=304340](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=304340)).

  - If you are using a third-party reverse proxy, then contact the vendor to confirm support of, or proper configuration for supporting, the OPTIONS verb.

  - For information about configuring the URLScan tool, see Microsoft Knowledge Base article "How to configure the URLScan Tool" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=326444](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=326444)).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

