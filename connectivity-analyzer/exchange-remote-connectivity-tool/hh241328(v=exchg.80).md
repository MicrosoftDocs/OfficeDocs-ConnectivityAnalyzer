---
title: Name Space is not Federated
TOCTitle: Name Space is not Federated
ms:assetid: 08199ae2-2469-4f5f-aba5-aa4744ac7ebf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh241328(v=EXCHG.80)
ms:contentKeyID: 36021327
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Name Space is not Federated

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-06-22_

The Microsoft Remote Connectivity Analyzer Tool queries the Authentication Platform in the cloud to perform a realm discovery. When that process is finished, the Authentication Platform passes to the requesting client the ADFS endpoint URL that the client requires for authentication. If the identity that you provide does not match an identity federated domain name, the lookup fails.

The Remote Connectivity Analyzer displays the following warning when the domain part of the name is not set up for identity federation:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The domain is not a federated domain.</p></td>
</tr>
</tbody>
</table>

This message indicates a failure of the realm discovery process. This process is the initial check against the domain name to determine whether the Authentication Platform in the cloud has this domain configured for identity federation. The failure of this process can be caused by an incorrectly typed UPN. The failure can also indicate that identity federation is not yet configured.

To verify whether the domain name is set up for identity federation, follow these steps:

1.  Log on to the Microsoft Online Portal as a Tenant Administrator.

2.  Under **Management** in the navigation pane, click **Domains**.

3.  Locate the domain that matches the UPN that was entered for the test.

4.  Verify that the domain type is set to **configured for single sign-on**.

<div>

## More Information

For more information planning for identity federation, see [Prepare for single sign-on](http://onlinehelp.microsoft.com/en-us/office365-enterprises/ff652540.aspx)

For help to upgrade your current Exchange 2010 environment, see [Exchange Server Deployment Assistant](http://technet.microsoft.com/en-us/exdeploy2010/default.aspx)

</div>

</div>

<span> </span>

</div>

</div>

</div>

