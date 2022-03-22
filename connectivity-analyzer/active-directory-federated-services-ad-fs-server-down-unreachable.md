---
title: Active Directory Federated Services (AD FS) server is down or unreachable
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud by using Identity Federation to simulate the authentication to the Office 365 environment. Occasionally, the ADFS server is not reachable, and you receive an error message.'
---



# Active Directory Federated Services (AD FS) server is down or unreachable



_**Topic Last Modified:** 2011-06-06_

<div id="sectionSection0" class="section">

The Microsoft Remote Connectivity Analyzer tool queries the Authentication Platform in the cloud by using Identity Federation to simulate the authentication to the Office 365 environment. Occasionally, the ADFS server is not reachable at all. For instance, the ADFS server is not reachable if the ADFS services crash or fail to start. If this issue occurs, you may receive a message that resembles the following message:


<table>
<colgroup>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Retrieving ADFS metadata information from Metadata Exchange Url https://sts.Contoso.com/adfs/services/trust/mex</p></td>
</tr>
<tr class="even">
<td><p>Failed to retreive ADFS metadata.</p></td>
</tr>
<tr class="odd">
<td><p>Additional Details</p></td>
</tr>
<tr class="even">
<td><p>A Web exception occurred because an HTTP 503 - ServiceUnavailable response was received from Unknown.</p></td>
</tr>
</tbody>
</table>

If you see this error returned, make sure that you examine the ADFS services on the ADFS server and on the ADFS proxy. A failure of the services to start on either server can cause the same error message to be generated. In this case, you must investigate the cause of the service failure by examining the event logs. If the services cannot be started, and there is no indication in the logs about the cause of the failure, you might have to make a support call.

<div>

## More Information

For more information planning for identity federation, see [Prepare for single sign-on](https://onlinehelp.microsoft.com/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](https://technet.microsoft.com/exdeploy2010/default.aspx)

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

