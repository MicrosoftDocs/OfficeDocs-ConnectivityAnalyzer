---
title: No MX Records were Found for the Specified SMTP Domain
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer performs a DNS lookup to locate a list of Mail Exchanger records that match the SMTP domain being tested. If no MX records are returned, the test fails with the following error: "No MX records found in DNS for SMTP domain (Domain Name)"'
---


# No MX Records were Found for the Specified SMTP Domain

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-11-18_

The Microsoft Remote Connectivity Analyzer performs a Domain Name Service (DNS) lookup to locate a list of Mail Exchanger (MX) records that match the SMTP domain being tested. If no MX records are returned in the list, then the test will fail with the following error.  
  
"No MX records found in DNS for SMTP domain (Domain Name)"

Unless the DNS zone for your domain includes MX records, inbound SMTP e-mail may not be able to be properly delivered for that SMTP domain.

The DNS lookup of the MX record(s) for the SMTP domain could fail because the MX record(s) could be missing on the DNS server.

<div>

## For More Information

**To correct this error**

1.  Use the nslookup.exe utility to verify that the Mail Exchanger (MX) record exists on the DNS server.

2.  If the MX resource record does not exist, manually add or modify the resource record. If your external DNS zone is hosted by a third party, you may have to contact that company or use custom tools to make these DNS modifications.

For information about how to troubleshoot DNS, see "Troubleshooting DNS" ([https://go.microsoft.com/fwlink/?LinkId=63003](https://go.microsoft.com/fwlink/?linkid=63003)).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

