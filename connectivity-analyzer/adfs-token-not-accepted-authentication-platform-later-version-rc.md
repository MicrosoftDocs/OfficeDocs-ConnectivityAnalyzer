---
title: ADFS token not accepted by Authentication Platform (for later version of RCA)
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">

# ADFS token not accepted by Authentication Platform (for later version of RCA)

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. Occasionally, the configuration information that is returned causes the ADFS server to respond with an invalid token because of the existing configuration in the on-premise ADFS environment.

The Remote Connectivity Analyzer displays a warning when the authorization fails to indicate that the token was not accepted by the Authentication Platform in the cloud. To resolve this issue, fix the configuration in the on-premise ADFS configuration that is incorrectly configured. After this issue is resolved, you must update the settings in the Authentication Platform in the cloud. This issue usually affects customers who have federated with previous versions of the Online services.

<div>

## More Information

For more information about how to troubleshoot this issue, see Microsoft Knowledge Base article 2521057, [How to reestablish trust with the Microsoft Online Services ID service after the AD FS 2.0 server stops responding](https://support.microsoft.com/kb/2521057)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

