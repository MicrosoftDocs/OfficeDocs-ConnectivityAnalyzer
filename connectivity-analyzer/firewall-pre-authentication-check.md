---
title: Firewall Pre-Authentication Check
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: Firewall Pre-Authentication Check in Microsoft Remote Connectivity Analyzer
---

# Firewall Pre-Authentication Check

_**Topic Last Modified:** 2013-03-21_

The Microsoft Remote Connectivity Analyzer (RCA) queries to determine whether any DNS records point to the Autodiscover endpoint. After that lookup occurs, the RCA performs additional queries to discover whether authentication is configured correctly. Frequently, a perimeter device, such as Microsoft Threat Management Gateway (TMG), is configured incorrectly.

Customers often decide to use pre-authentication at the perimeter device. This is a fine solution for such applications as Outlook Anywhere and OWA, but it can cause issues that affect the Office 365 hybrid deployment. We must accommodate pass-through authentication for certain endpoints that use token-based authorization instead of standard basic/integrated authentication options.

The solution is simple: Create a rule that uses the same listener as the other Exchange components do, but also provides explicit paths for the endpoints that require pass-through authentication. Configure the new rule so that it does not perform pre-authentication at the perimeter device. If the rule is implemented correctly, you can continue to use the same external IP address and port (443) on the same listener for both rules.

<div>

## More Information

For information about how to configure TMG for Office 365 hybrid deployments, including how to configure a rule for specific paths that require pass-through authentication, see [How to Configure TMG for Office 365 (Exchange) Hybrid deployments](https://go.microsoft.com/fwlink/p/?linkid=241473).

Before you decide how to configure Autodiscover, we recommend that you obtain and read [Publishing Exchange Server 2010 with Forefront Unified Access Gateway 2010 and Forefront Threat Management Gateway 2010](https://go.microsoft.com/fwlink/p/?linkid=197136).

Microsoft Remote Connectivity Analyzer currently has limited documentation. In order to improve the documentation for each error that you may receive, we want to ask for more information from the community. Please use the Community Content section in this topic to post additional reasons about why your effort failed at this point. If you want technical help, please contact [Microsoft Support](https://go.microsoft.com/fwlink/p/?linkid=8158) or create a post at the RCA forum on TechNet. Although the RCA forum has been retired, the forum threads remain active at [Exchange Previous Versions - Extended Components, Tools, and Utilities](https://go.microsoft.com/fwlink/p/?linkid=288878).

</div>

</div>

<span> </span>

</div>

</div>

</div>

