---
title: Missing AuthPackage Element in Autodiscover XML Response
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# Missing AuthPackage Element in Autodiscover XML Response

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-09-01_

The Microsoft Remote Connectivity Analyzer sends an XML Autodiscover request to the remote Exchange 2007 Client Access server and analyzes the Autodiscover XML response. If there is no AuthPackage element present in the XML response received from Autodiscover, then the Microsoft Remote Connectivity Analyzer displays the following error message:

"Missing AuthPackage element in Autodiscover XML Response"

This error typically occurs when the Server attribute is incorrectly set for the EXPR Outlook Provider. If the value of the attribute is set to anything but its default setting of NULL, then end users may report that they are prompted for credentials when connecting using Outlook Anywhere even though the Exchange proxy settings in Outlook 2007 have been configured for NT LAN Manager (NTLM) authentication.

<div>

## For More Information

EXPR is one of the Outlook providers that can be managed by using the cmdlets, Get-OutlookProvider and Set-OutlookProvider, in the Exchange Management Shell. The Server attribute for the OutlookProvider object should remain at its default setting of $null. You can check the value of the Server attribute by running the Get-OutlookProvider cmdlet (Get-OutlookProvider Identity | format-list).

For more information, including instructions for modifying the Server attribute, see [Autodiscover Service Returns Unexpected Values for Outlook Anywhere Proxy Settings](https://go.microsoft.com/fwlink/?linkid=161812).

For more information about modifying the Outlook Providers in general, see, [When, if and how do you modify Outlook Providers?](https://go.microsoft.com/fwlink/?linkid=160947)

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

