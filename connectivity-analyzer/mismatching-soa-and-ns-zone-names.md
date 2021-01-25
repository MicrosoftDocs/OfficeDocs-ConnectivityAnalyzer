---
title: SOA Record returned for a parent zone while having separate NS record delegation configured for a domain
author: stanalek
ms.author: stanalek
manager: pschiek
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: High
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# SOA Record returned for a parent zone while having separate NS record delegation configured for a domain

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2021-01-25_

A sub-domain is delegated through name server (NS) records at the domain registrar but the  target server actually hosts only the parent domain i.e. no Start of Authority (SOA) record is present for the sub-domain. This results in an SOA record returned which has the zone name of the parent domain (example below). This can cause EDNS resolvers like Windows DNS to fail resolving a MX query for the domain with a "ServerFailure" error.

For any of your domains or sub-domains configured as a separate DNS zone, each DNS zone should have an NS record and an SOA record for that zone, as stated in the RFC  (see [RFC 1034 section 4.2.1](https://tools.ietf.org/html/rfc1034#section-4.2.1"), and [RFC 2308 section 3](https://tools.ietf.org/html/rfc2308#section-3)).

For example, if your parent domain is contoso.com, at your domain registrar (or parent zone server on-premises) you might have configured dedicated delegation for a sub-domain record for mail.contoso.com, like this: 

```
Domain				TTL	Class 	Type	Name Server 

mail.contoso.com	300	IN 		NS		ns1.contoso.com 
mail.contoso.com	300	IN		NS		ns2.contoso.com 
```
 

Yet, the final response for the MX query for mail.contoso.com returns an SOA record for contoso.com instead: 
 
```
SOA Zone name 	TTL Class 	Type 	Primary Name Server 	Email Contact			Serial 		Refresh Retry 	Expire 	Minimum

contoso.com.	60	IN		SOA		ns1.contoso.com. 		hostmaster.ns1.contoso.com 	2020090310 	10800 	3600	604800 	60 
```
 

The different names on NS and SOA records causes EDNS to fail the query with ServerFailure as it violates the RFC references below. 

This is because ns1.contoso.com hosts only the parent domain, contoso.com (i.e. only contoso.com is listed in the zone file).  

One way to address the issue is to remove the dedicated delegation entries for the sub-domain mail.contoso.com from the domain's DNS records at the domain registrar and instead make an entry for the sub-domain A record itself in the parent domain zone (e.g. for *.contoso.com): 
 
```
Domain				TTL	Class	Type	Name Server Host/IP Address

contoso.com			300	IN		NS		ns1.contoso.com. 
ns1.contoso.com		300	IN		A		1.2.3.4 
mail.contoso.com	300	IN		A		111.22.3.4 
```
 
If you have business needs that require you to host the sub-domain on separate servers from where the parent domain is hosted, then those servers should only list the sub-domain, mail.contoso.com in the zone file, and the sub-domain should have its own NS and SOA records (configured at the domain registrar). 

<div>

### References
 
[RFC 1034 section 4.2.1](https://tools.ietf.org/html/rfc1034#section-4.2.1") and [RFC 2181 section 5.4.1](https://tools.ietf.org/html/rfc2181#section-5.4.1) point out that NS resource records (RRs) should point to child zone name servers:

	The RRs that describe cuts around the bottom of the zone are NS RRs that name the servers for the subzones.  Since the cuts are between nodes, these RRs are NOT part of the authoritative data of the zone, and should be exactly the same as the corresponding RRs in the top node of the subzone
  
	"Glue" above includes any record in a zone file that is not properly part of that zone, including nameserver records of delegated sub-zones (NS records)
		 
[RFC 2308 section 3](https://tools.ietf.org/html/rfc2308#section-3) specifies that SOA for the zone should be included into NO DATA response:

	Negative Answers from Authoritative Servers
	 
	   Name servers authoritative for a zone MUST include the SOA record of
	   the zone in the authority section of the response when reporting an
	   NXDOMAIN or indicating that no data of the requested type exists.

</div>

</div>

<span> </span>

</div>

</div>

</div>
