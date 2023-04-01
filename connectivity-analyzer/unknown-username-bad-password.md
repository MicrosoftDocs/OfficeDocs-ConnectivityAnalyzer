---
title: Unknown Username or bad password
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Remote Connectivity Analyzer displays the following warning message if the user is not authenticated correctly: "The Security Token Service indicated that the authentication failed. Check the username and password and try again."'
ms.date: 05/08/2020
---

# Unknown Username or bad password

_**Topic Last Modified:** 2011-06-06_

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to simulate the token retrieval process from the on-premise ADFS server. To perform the test, you must type the correct username and password so that the tool retrieves the token correctly on behalf of the user.

The Remote Connectivity Analyzer displays the following warning message if the user is not authenticated correctly:

The Security Token Service indicated that the authentication failed. Check the username and password and try again.

This message indicates a logon failure when you try to authenticate at the ADFS endpoint. This error can occur for any of the following reasons:

  - Users enter a bad password

  - Users enter a bad username

  - Users do not have the identity federated domain set as their UPN

You can address these issues in the on-premise Active Directory Users and Computers MMC.

## More Information

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx).

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx).
