---
title: The Service Account Specified Does Not Have Impersonation Rights on Client Access Server
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer generates the following error: "ErrorImpersonationDenied, this error code indicates that the Service Account specified does not have the ms-Exch-EPI-Impersonation right on the Exchange Client Access server."'
ms.date: 05/08/2020
---

# The Service Account Specified Does Not Have Impersonation Rights on Client Access Server


_**Topic Last Modified:** 2009-09-01_

The Microsoft Remote Connectivity Analyzer sends XML/HTTP requests to the Exchange Web Services service using the Exchange Web Services API. When those requests attempt to use Exchange Impersonation and an error status message is present in the response, the Microsoft Remote Connectivity Analyzer generates the following error.

“ErrorImpersonationDenied, this error code indicates that the Service Account specified does not have the ms-Exch-EPI-Impersonation right on the Exchange Client Access server.”

The Microsoft Remote Connectivity Analyzer uses the [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) SOAP header of Exchange Web Services to specify an account that is to be impersonated by the Service Account to test whether the Service Account has permissions to issue impersonation requests using [ExchangeImpersonation](https://go.microsoft.com/fwlink/?linkid=161948) (also known as [Server-to-Server Authorization](https://go.microsoft.com/fwlink/?linkid=161951)).

## For More Information

To resolve this issue, the Service Account must be granted permission to issue an impersonation call through the Client Access server. For more information, see [Configuring Exchange Impersonation (Exchange Web Services)](https://go.microsoft.com/fwlink/?linkid=161954).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
