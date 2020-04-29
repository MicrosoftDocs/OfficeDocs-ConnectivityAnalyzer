---
title: Could Not Find Autodiscover Service Location (SRV) Record in DNS
TOCTitle: Could Not Find Autodiscover Service Location (SRV) Record in DNS
ms:assetid: f7432938-9087-4033-9648-224565858a5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439398(v=EXCHG.80)
ms:contentKeyID: 20045845
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Could Not Find Autodiscover Service Location (SRV) Record in DNS

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Exchange Analyzer Tool queries DNS to determine whether there are any Service Location (SRV) records for Autodiscover. This DNS Service Location Record query is in the format "\_autodiscover.\_tcp.\<smtpDomain\>" where \<smtpDomain\> is the right-hand side of the user's primary SMTP address. If the Exchange Remote Connectivity Analyzer is unable to locate any SRV records for Autodiscover in that namespace, then the following error is displayed:

"Failed to find Autodiscover SRV record in DNS."

Microsoft Office Outlook 2007 clients attempt to connect to the Autodiscover service using four methods. As each one fails, the next method is tried in the following order:

1.  Using a Service Connection Point (SCP) object in Active Directory

2.  Using DNS

3.  Using an HTTP redirect

4.  Using an SRV record

<div class="alert">


> [!NOTE]
> This should only be considered an error if you intended to configure your environment so that the location of the Autodiscover virtual directory on the Client Access server would be found using an SRV record.


</div>

<div>

## For More Information

The following resources should be consulted before deciding how to configure Autodiscover:

  - For more information about Outlook 2007 and Autodiscover interoperability, including a description of each method that can be used to locate Autodiscover, see [White Paper: Exchange 2007 Autodiscover Service](http://go.microsoft.com/fwlink/?linkid=85214).

  - For more information about enabling Outlook 2007 to use SRV records to locate Autodiscover, see Microsoft Knowledge Base article, "A new feature is available that enables Outlook 2007 to use DNS Service Location (SRV) records to locate the Exchange Autodiscover service" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=940881](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=940881)).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

