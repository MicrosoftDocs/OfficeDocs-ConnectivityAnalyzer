---
title: Error with System Time
TOCTitle: Error with System Time
ms:assetid: d444776a-2a72-4185-8979-bd786390b38f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ710174(v=EXCHG.80)
ms:contentKeyID: 50384379
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Error with System Time

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2012-11-06_

The Microsoft Exchange Remote Connectivity Analyzer Tool determines whether any issues that affect free/busy queries exist between an Office 365 mailbox and an on-premises mailbox. This status check includes checking the system time of the on-premises Exchange server. Similar to issues that affect Kerberos protocol, if the system time of the on-premises server that is communicating with the Microsoft Federation Gateway is skewed by more than five (5) minutes, the server experiences an Access Denied error when it requests a delegation token.

The Access Denied error causes issues that affect cross-premises free/busy lookups in addition to issues that affect any other cross premises feature. The solution to this issue is to make sure that you are using a reliable time source for the servers within your environment, and to adjust the system time settings to the correct values.

<div class="alert">


> [!NOTE]
> If you are creating a federation trust, you may also receive the following error message for the same reason that was mentioned previously: 1007 AccessDenied: Access Denied.


</div>

This error message is generally a reliable indicator of this issue. However, if you are still unsure whether this is the issue that you are dealing with, you can connect to the Exchange Management Shell on your on-premises Exchange server, and then run the following cmdlet: **Test-FederationTrust ValidMailbox -userIdentity –Verbose**.

<div>

## More Information

For information about how to resolve this issue, see [Synchronize the Time Server for the Domain Controller with an External Source](http://technet.microsoft.com/en-us/library/cc784553\(ws.10\).aspx).

We recommend that you consult the following resources before you decide how to configure Cross premises Exchange:

  - [The Exchange Deployment Assistant](http://technet.microsoft.com/en-us/exdeploy2010/default.aspx)

  - Microsoft Knowledge Base article [How to troubleshoot free/busy issues when you use Exchange Federation in the Microsoft Office 365 for enterprises environment](http://support.microsoft.com/kb/2555008)

The Exchange Remote Connectivity Analyzer is a new tool that currently has limited documentation. In order to improve the documentation for each error that you may receive, we want to ask for more information from the community. Please use the Community Content section in this topic to post additional reasons about why your effort failed at this point. If you want technical help, please contact [support](http://go.microsoft.com/fwlink/?linkid=8158) or create a post at the Remote Connectivity Analyzer forum on TechNet. Although the RCA forum has been retired, the forum threads remain active at [Exchange Previous Versions - Extended Components, Tools, and Utilities](http://social.technet.microsoft.com/forums/en-us/exchangesvr3rdpartyappslegacy).

</div>

</div>

<span> </span>

</div>

</div>

</div>

