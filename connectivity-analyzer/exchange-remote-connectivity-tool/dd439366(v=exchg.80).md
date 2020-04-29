---
title: Name Could Not be Matched to a Name in the Address List
TOCTitle: Name Could Not be Matched to a Name in the Address List
ms:assetid: 2268f80c-4f96-4612-85ee-99b5a0322f5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439366(v=EXCHG.80)
ms:contentKeyID: 20045813
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Name Could Not be Matched to a Name in the Address List

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer tool uses the user information provided and sends an NSPI ResolveNames (Check Name) request to the Exchange Server (using RPC over HTTP) to attempt to resolve the user account in the Address Book. If no matching entries are found, then the Exchange Remote Connectivity Analyzer tool displays the following error message.

"The name could not be matched to a name in the address list."

This issue typically occurs when the user account is not associated with a mailbox or when it has been manually configured to be hidden from the Global Address List. Lack of Active Directory permissions to certain objects or issues with the Exchange Recipient Update Service are also common causes. In addition to the error above, end users may be unable to successfully perform a check name, create a MAPI profile, or connect to an Exchange server.

<div>

## For More Information

To resolve this issue, see Microsoft Knowledge Base article, "Troubleshooting Check Name errors" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=297801](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=297801)).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

