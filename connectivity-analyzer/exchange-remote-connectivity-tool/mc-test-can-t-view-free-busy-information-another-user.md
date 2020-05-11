---
title: "MCA test: I can't view the free/busy information of another user"
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# MCA test: I can't view the free/busy information of another user

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2013-02-21_

The Microsoft Connectivity Analyzer includes the **I can't view the free/busy information of another user** test. This test verifies that an Office 365 mailbox can access the free/busy information of an on-premises mailbox, and vice versa.

This test includes the following features:

  - A check to verify that the system time of the hybrid server is not offset by more than five minutes. An offset of more than five minutes causes failures when delegation tokens are requested from the Microsoft Federation Gateway.

  - A check to verify that inbound connectivity to the hybrid server does not require firewall pre-authentication. The firewall must allow pass-through authentication. This check is effective when the MCA client is run from outside the corporate network.

  - A check to verify that the hybrid server meets the minimum Exchange Server version requirements.

  - A basic free/busy query against the target Availability service.

  - Links to guidance about the Hybrid Configuration wizard. This wizard is a common source of potential hybrid deployment misconfiguration.

The Microsoft Connectivity Analyzer is a new tool that has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the following Community Content section to post additional reasons about why your testing failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/p/?linkid=73420) or contact [Microsoft Support](http://go.microsoft.com/fwlink/p/?linkid=8158).

</div>

<span> </span>

</div>

</div>

</div>

