---
title: The Service Account Specified Does Not Have Impersonation Rights on Client Access Server
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

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# The Service Account Specified Does Not Have Impersonation Rights on Client Access Server

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-09-01_

The Microsoft Exchange Analyzer Tool sends XML/HTTP requests to the Exchange Web Services service using the Exchange Web Services API. When those requests attempt to use Exchange Impersonation and an error status message is present in the response, the Exchange Remote Connectivity Analyzer generates the following error.

“ErrorImpersonationDenied, this error code indicates that the Service Account specified does not have the ms-Exch-EPI-Impersonation right on the Exchange Client Access server.”

The Exchange Remote Connectivity Analyzer uses the [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) SOAP header of Exchange Web Services to specify an account that is to be impersonated by the Service Account to test whether the Service Account has permissions to issue impersonation requests using [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) (also known as [Server-to-Server Authorization](https://go.microsoft.com/fwlink/?linkid=161951)).

<div>

## For More Information

To resolve this issue, the Service Account must be granted permission to issue an impersonation call through the Client Access server. For more information, see [Configuring Exchange Impersonation (Exchange Web Services)](https://go.microsoft.com/fwlink/?linkid=161954).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

