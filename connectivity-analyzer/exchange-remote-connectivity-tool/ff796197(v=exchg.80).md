---
title: IP Address does not have a PTR record in DNS
TOCTitle: IP Address does not have a PTR record in DNS
ms:assetid: 14280637-0bb4-42dd-8ecc-0f6802a4d16d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Ff796197(v=EXCHG.80)
ms:contentKeyID: 31707090
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# IP Address does not have a PTR record in DNS

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-01-25_

The Microsoft Exchange Best Practices Analyzer Tool tries to perform a Reverse DNS (PTR) lookup on the outbound IP address that is used to send e-mail to the Internet. If a DNS entry for this IP address cannot be found, the following error message is generated:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>IP Address X.X.X.X does not have a PTR record in DNS</p></td>
</tr>
</tbody>
</table>

<div>

## For More Information

Reverse zones are in the following format: reversed dotted-notation-ip.in-addr.arpa.

For example, if you specify A.B.C.D for the outbound IP Address, the query would be formed as D.C.B.A.in-addr.arpa. The query would not find an entry in the reverse zone in DNS.

Typically, reverse zones are maintained by your ISP.

<div>

## What this error means to you as an admin

Some e-mail servers check for a reverse record as a basic anti-spam check procedure. Therefore, it is a good practice to have a reverse record that matches your A record. These e-mail servers may reject messages from your domain, or they may flag messages as spam if they cannot detect a valid PTR record for your sending host.

For more information about reverse lookup DNS, see the following articles on the IETF Tools Web site:

<http://tools.ietf.org/html/rfc1912>

<http://tools.ietf.org/html/rfc2317>

The Exchange Remote Connectivity Analyzer is a new tool that has limited documentation at this time. In an effort to improve the documentation for each of the errors that you might receive, we would like to solicit additional information from the community. Please use the Community Content section at the bottom of this page to post additional reasons why your lookup failed at this point. If you require technical assistance, create a post in the appropriate [Microsoft Exchange Server TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420), or contact [Microsoft Product Support Services](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

