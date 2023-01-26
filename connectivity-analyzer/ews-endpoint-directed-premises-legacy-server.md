---
title: EWS Endpoint Directed to On-Premises Legacy Server
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'EWS endpoint directed to on-premises legacy server'
ms.date: 05/08/2020
---

# EWS Endpoint Directed to On-Premises Legacy Server

_**Topic Last Modified:** 2012-11-06_

The Microsoft Remote Connectivity Analyzer Tool can be used to determine whether any issues that affect free/busy queries exist between an Office 365 mailbox and an on-premises mailbox. This status check includes verifying that the on-premises Exchange server meets the minimum version requirement. In order for a cross premises free/busy query to work, the version of the server that hosts the Autodiscover and EWS endpoints must be Microsoft Exchange Server 2010 SP1 or a later version.

It is common for organizations to keep their external-facing endpoints (for example, autodiscover.contoso.com and mail.contoso.com) incorrectly pointing to earlier versions of Exchange Server (“legacy servers”) instead of updating the DNS records to point to a server that has Exchange Server 2010 SP1 or a later version installed.

Exchange Server 2010 SP1 or a later version is required in order for free/busy and other hybrid deployment features to work. Legacy servers lack the required logic to handle the complex authentication workflow requirements of a federated request.

The solution to this issue is to make sure that the external DNS records for Autodiscover and EWS are pointed to the Internet-facing server that is running Exchange Server 2010 SP1 or a later version.

<div>

## More information

For more information about how to troubleshoot federated free/busy issues, see Microsoft Knowledge Base article [2555008: How to troubleshoot free/busy issues when you use Exchange Federation in the Microsoft Office 365 for enterprises environment](https://support.microsoft.com/kb/2555008).

We recommend that you consult the following resources before you decide how to configure a cross premises Exchange server:

  - [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

  - Microsoft Knowledge Base article [2555008: How to troubleshoot free/busy issues when you use Exchange Federation in the Microsoft Office 365 for enterprises environment](https://support.microsoft.com/kb/2555008)

<div>

## More resources

Microsoft Remote Connectivity Analyzer currently has limited documentation. In order to improve the documentation for each error that you may receive, we want to ask for more information from the community. Please use the Community Content section in this topic to post additional reasons about why your effort failed at this point. If you want technical help, please contact [support](https://go.microsoft.com/fwlink/?linkid=8158) or create a post at the Remote Connectivity Analyzer forum on TechNet. Although the RCA forum has been retired, the forum threads remain active at [Exchange Previous Versions - Extended Components, Tools, and Utilities](https://social.technet.microsoft.com/forums/exchangesvr3rdpartyappslegacy).

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

