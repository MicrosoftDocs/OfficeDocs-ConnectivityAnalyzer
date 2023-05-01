---
title: Invalid XML Response Unable to Retrieve Availability or OOF Settings
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'Invalid XML response, unable to retrieve Availability or OOF Settings.'
ms.date: 05/08/2020
---

# Invalid XML Response Unable to Retrieve Availability or OOF Settings

_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends GetUserOofSettings and GetUserAvailability XML/HTTP requests to the Exchange Web Services service using the Exchange Web Services API to test operations used by Exchange clients and custom applications. When invalid XML is returned in the response, the Microsoft Remote Connectivity Analyzer tool generates the following error:

"Invalid XML response, unable to retrieve Availability or OOF Settings."

The Microsoft Remote Connectivity Analyzer tool uses the [GetUserOofSettings Operation](https://go.microsoft.com/fwlink/?linkid=85951) and [GetUserAvailability Operation](https://go.microsoft.com/fwlink/?linkid=85950) to retrieve a user’s OOF settings and scheduled availability in the calendar respectively. These operations are used by clients such as Microsoft Office Outlook 2007 as well as custom applications.

## For More Information

To correct this error, see [Outlook 2007 crashes or you cannot access OOF settings after you install a package that contains the .NET Framework 3.5 with SP1 and the .NET Framework 2.0 with SP2 on an Exchange 2007 Client Access server](https://go.microsoft.com/fwlink/?linkid=3052\&kbid=958934).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
