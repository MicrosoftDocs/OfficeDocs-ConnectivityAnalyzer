---
title: ActiveSync ExternalUrl is Not in the Expected Format
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'ActiveSync URL was in an Invalid format. It should be https://host/Microsoft-Server-ActiveSync. The URL was...'
---


# ActiveSync ExternalUrl is Not in the Expected Format

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-09-01_

The Microsoft Remote Connectivity Analyzer sends an HTTP request to the MobileSync Autodiscover provider on the Client Access server to obtain an External URL for ActiveSync devices to use when connecting to Exchange. This URL should be in the format https://{hostname}/Microsoft-Server-ActiveSync (where {hostname} is the external DNS fully-qualified domain name (FQDN)) used by mobile devices to connect to Exchange ActiveSync. When the URL that is returned is not in the expected format, the Microsoft Remote Connectivity Analyzer returns the following error.

"ActiveSync URL was in an Invalid format. It should be https://host/Microsoft-Server-ActiveSync. The URL was \<your URL\>."

<div>

## For More Information

To resolve this issue, verify the ExternalUrl setting on the Microsoft-Server-ActiveSync virtual directory in the Exchange Management Console.

1.  Expand the Server Configuration node.

2.  Select the Client Access node.

3.  Select the appropriate Client Access server.

4.  Select the Exchange ActiveSync tab.

5.  Select the Microsoft-Server-ActiveSync virtual directory.

6.  Click Properties for the virtual directory.

7.  Ensure that the External URL setting is in the format: https://host/Microsoft-Server-ActiveSync.

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

