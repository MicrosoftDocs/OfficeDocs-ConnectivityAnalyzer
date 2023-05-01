---
title: Name Space is not Federated
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Remote Connectivity Analyzer displays the following warning when the domain part of the name is not set up for identity federation: "The domain is not a federated domain."'
ms.date: 05/08/2020
---

# Name Space is not Federated


_**Topic Last Modified:** 2011-06-22_

The Microsoft Remote Connectivity Analyzer Tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. If the identity that you provide does not match an identity federated domain name, the lookup fails.

The Remote Connectivity Analyzer displays the following warning when the domain part of the name is not set up for identity federation:

The domain is not a federated domain.

This message indicates a failure of the realm discovery process. This process is the initial check against the domain name to determine whether the Authentication Platform in the cloud has this domain configured for identity federation. The failure of this process can be caused by an incorrectly typed UPN. The failure can also indicate that identity federation is not yet configured.

To verify whether the domain name is set up for identity federation, follow these steps:

1.  Log on to the Microsoft Online Portal as a Tenant Administrator.

2.  Under **Management** in the navigation pane, click **Domains**.

3.  Locate the domain that matches the UPN that was entered for the test.

4.  Verify that the domain type is set to **configured for single sign-on**.

## More Information

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx).

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx).
