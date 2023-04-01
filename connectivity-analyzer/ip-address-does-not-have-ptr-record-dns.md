---
title: IP Address does not have a PTR record in DNS
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'IP Address X.X.X.X does not have a PTR record in DNS'
ms.date: 05/08/2020
---

# IP Address does not have a PTR record in DNS


_**Topic Last Modified:** 2011-01-25_

The Microsoft Remote Connectivity Analyzer tries to perform a Reverse DNS (PTR) lookup on the outbound IP address that is used to send e-mail to the Internet. If a DNS entry for this IP address cannot be found, the following error message is generated:

IP Address X.X.X.X does not have a PTR record in DNS

## For More Information

Reverse zones are in the following format: reversed dotted-notation-ip.in-addr.arpa.

For example, if you specify A.B.C.D for the outbound IP Address, the query would be formed as D.C.B.A.in-addr.arpa. The query would not find an entry in the reverse zone in DNS.

Typically, reverse zones are maintained by your ISP.

## What this error means to you as an admin

Some e-mail servers check for a reverse record as a basic anti-spam check procedure. Therefore, it is a good practice to have a reverse record that matches your A record. These e-mail servers may reject messages from your domain, or they may flag messages as spam if they cannot detect a valid PTR record for your sending host.

For more information about reverse lookup DNS, see the following articles on the IETF Tools Web site:

<https://tools.ietf.org/html/rfc1912>

<https://tools.ietf.org/html/rfc2317>

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors that you might receive, we would like to solicit additional information from the community. Please use the Community Content section at the bottom of this page to post additional reasons why your lookup failed at this point. If you require technical assistance, create a post in the appropriate [Microsoft Exchange Server TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420), or contact [Microsoft Product Support Services](https://go.microsoft.com/fwlink/?linkid=8158).
