---
title: The Service Account Specified Does Not Have Impersonation Rights on the Act As Account Specified
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

# The Service Account Specified Does Not Have Impersonation Rights on the Act As Account Specified

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-19_

The Microsoft Exchange Analyzer Tool sends XML/HTTP requests to the Exchange Web Services service using the Exchange Web Services API. When those requests attempt to use Exchange Impersonation and an error status message is present in the response, the Exchange Remote Connectivity Analyzer generates the following error.

"ErrorImpersonateUserDenied, this error code indicates that the Service Account specified does not have the ms-Exch-EPI-May-Impersonate right on the Act As Account it is trying to impersonate"

The Exchange Remote Connectivity Analyzer uses the [ExchangeImpersonation](http://go.microsoft.com/fwlink/?linkid=161948) SOAP header of Exchange Web Services to specify an account that is to be impersonated by the Service Account to test whether the Service Account has permissions to impersonate the specified impersonated user using [Exchange Impersonation](http://go.microsoft.com/fwlink/?linkid=161948) (also known as [Server-to-Server Authorization](http://go.microsoft.com/fwlink/?linkid=161951)). The "Act As Account" is the account used by Exchange to authorize the execution of Exchange Web Services commands – it is the account being impersonated.

<div>

## For More Information

To resolve this issue, the Service Account must be granted permission to impersonate the specified user. For more information, see [Configuring Exchange Impersonation (Exchange Web Services)](http://go.microsoft.com/fwlink/?linkid=161954).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

