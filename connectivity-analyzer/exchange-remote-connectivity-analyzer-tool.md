---
title: Microsoft Remote Connectivity Analyzer Tool
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: Description and IP address ranges of the Microsoft Remote Connectivity Analyzer (RCA) tool
ms.date: 05/08/2020
---

# Microsoft Remote Connectivity Analyzer

This content is intended to address specific issues called out by the Microsoft Remote Connectivity Analyzer tool. You should apply these resolutions only to systems that have had the Microsoft Remote Connectivity Analyzer tool run against them and are experiencing that specific issue.

The Microsoft Remote Connectivity Analyzer tool is available at [Microsoft Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?linkid=154308). The tool is web-based, and is designed to help IT Administrators troubleshoot connectivity issues that affect their Microsoft 365, Teams, and Exchange Server deployments. The tool simulates several client logon and mail flow scenarios. When a test fails, many of the errors have troubleshooting tips to assist the IT Administrator to correct the problem.

The Microsoft Remote Connectivity Analyzer tool uses a specific set of IP addresses to perform these communications, those IP addresses and all of the URL and IP address information for Office 365 can be found in this documentation: [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/?linkid=532912). The Microsoft Remote Connectivity Analyzer tool ranges are part of the Microsoft 365 Common and Office Online section, specifically ID 46 in the documentation. While not mentioned explicitly, if you are testing SMTP, POP or IMAP you will also need to allow access to those relevant ports from the same IP address ranges. 

> [!NOTE]
> At this time the Microsoft Remote Connectivity Analyzer tool doesn't support Microsoft 365 Government environments (GCC or GCC High).

# More information
Remote Connectivity Analyzer is a free connectivity test platform for cloud-based service. It tests the availability of the required federation service endpoint for expected behavior by acting on those services from the Internet.

# How to run Remote Connectivity Analyzer Diagnostics
1 - Open a web browser, and then browse to [Microsoft Remote Connectivity Analyzer](https://testconnectivity.microsoft.com/)
2 - Go through the technologies available and select one of the proposed scenarios
3 – Depending on the test you would like to do, you need to type your user ID, sign in and then verify the password, type the verification code, and then click Perform Test.

# What technologies are currently covered?
[Office 365](https://testconnectivity.microsoft.com/tests/o365)
[Exchange Server](https://testconnectivity.microsoft.com/tests/exchange)
[Microsoft Teams](https://testconnectivity.microsoft.com/tests/teams)
[Skype for Business Server](https://testconnectivity.microsoft.com/tests/skype)


The articles in this section correspond to specific error conditions that are identified when running the Microsoft Remote Connectivity Analyzer tool. Each article describes the error condition and provides links to help IT Administrators resolve the issue.
