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
---

# Microsoft Remote Connectivity Analyzer

This content is intended to address specific issues called out by the Microsoft Remote Connectivity Analyzer tool. You should apply these resolutions only to systems that have had the Microsoft Remote Connectivity Analyzer tool run against them and are experiencing that specific issue.

The Microsoft Remote Connectivity Analyzer tool is available at [https://go.microsoft.com/fwlink/?LinkId=154308](https://go.microsoft.com/fwlink/?linkid=154308). The tool is a web-based, and is designed to help IT Administrators troubleshoot connectivity issues that affect their Microsoft 365, Teams, and Exchange Server deployments. The tool simulates several client logon and mail flow scenarios. When a test fails, many of the errors have troubleshooting tips to assist the IT Administrator to correct the problem.

The Microsoft Remote Connectivity Analyzer tool uses a specific set of IP addresses to perform these communications, those IP addresses and all of the URL and IP address information for Office 365 can be found in this documentation: [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/?linkid=532912). The Microsoft Remote Connectivity Analyzer tool ranges are part of the Microsoft 365 Common and Office Online section, specifically ID 46 in the documentation. While not called out specifically in that section, you should also expect any relevant SMTP, POP & IMAP ports to be used by these IP address ranges as needed. 

The articles in this section correspond to specific error conditions that are identified when running the Microsoft Remote Connectivity Analyzer tool. Each article describes the error condition and provides links to help IT Administrators resolve the issue.
