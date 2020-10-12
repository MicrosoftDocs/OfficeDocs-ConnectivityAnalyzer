---
title: RPC Encryption Required
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

# RPC Encryption Required

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-05-19_

The Microsoft Remote Connectivity Analyzer queries the server that runs Exchange Server and tries to log on by using RPC over HTTP. If RPC encryption is required on the Exchange server, the following warning may be returned by the Analyzer tool:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Store logon returned ecNotEncrypted 2416. The Server requires RPC Encryption.</p></td>
</tr>
</tbody>
</table>

By default, Microsoft Office Outlook 2007 is configured by having the **Encrypt data between Microsoft Office Outlook and Microsoft Exchange** option enabled. However, the default Microsoft Outlook 2003 configuration does not have this option enabled. If you use the **Set-MailboxServer** cmdlet on an Exchange server to force encrypted connections on users' mailboxes, and the **Encrypt data between Microsoft Office Outlook and Microsoft Exchange** setting is turned off in Outlook, users receive the following error message when they try to connect to their Exchange mailboxes:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Your Exchange Server administrator has blocked the version of Outlook that you are using. Contact your administrator for assistance.</p></td>
</tr>
</tbody>
</table>

Outlook 2003 users who are connecting to Exchange may receive one of the following error messages:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Cannot start Microsoft Office Outlook. Unable to open the Outlook window. The set of folders could not be opened.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Unable to open your default e-mail folders. The Microsoft Exchange Server computer is not available. Either there are network problems or the Microsoft Exchange Server computer is down for maintenance.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The connection to the Microsoft Exchange Server is unavailable. Outlook must be online or connected to complete this action.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Unable to open your default e-mail folders. The information store could not be opened.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Outlook could not log on. Check to make sure you are connected to the network and are using the proper server and mailbox name. The connection to the Microsoft Exchange Server is unavailable. Outlook must be online or connected to complete this action.</p></td>
</tr>
</tbody>
</table>

When Outlook 2003 is configured to use Cached Exchange Mode, Outlook does not display an error message. Instead, Outlook starts in the Disconnected state.

<div>

## For More Information

To resolve this problem, do one or more of the following:

  - Determine whether RPC encryption is required by a Microsoft Exchange 2007 mailbox server. To do this, run the following command at the Exchange Management Shell:
    
        Get-MailboxServer <ServerName>
    
    If MAPIEncryptionRequired is true, Outlook clients that connect to Exchange must have the **Encrypt data between Microsoft Office Outlook and Microsoft Exchange** option enabled.

  - Determine whether RPC encryption is required by a Microsoft Exchange 2010 client access server. To do this, run the following command at the Exchange Management Shell:
    
        Get-RpcClientAccess | fl Server,EncryptionRequired
    
    If EncryptionRequired is true, Outlook clients that connect to Exchange must have the **Encrypt data between Microsoft Office Outlook and Microsoft Exchange** option enabled.

  - Verify that each Outlook profile has the **Encrypt data between Microsoft Office Outlook and Microsoft Exchange** option enabled. To do this, follow these steps:
    
    1.  Start the **Mail** item in Control Panel. Then, click **E-mail Accounts**.
    
    2.  Select the Exchange account, and then click **Change**.
    
    3.  Click **More Settings**, and then click the **Security** tab.
    
    4.  Click to select the **Encrypt data between Microsoft Outlook and Microsoft Exchange** check box, and then click **OK** .
    
    5.  Click **Next**, and then click **Finish**.

  - Alternatively, you may want to remove the Exchange requirement for encrypted RPC communications. To do this, follow these steps.
    
    <div class="alert">
    

    > [!NOTE]
    > <STRONG>Note</STRONG> By default, the requirement for RPC encryption is turned off in Exchange Server 2010 Service Pack 1 (SP1).

    
    </div>
    
      - For an Exchange 2007 mailbox server, run the following command at the Exchange Management Shell:
        
            Set-MailboxServer <ServerName> -MapiEncryptionRequired:$false
    
      - For an Exchange 2010 client access server, run the following command at the Exchange Management Shell:
        
            Set-RpcClientAccess -Server <ServerName> -EncryptionRequired $False

For more information about other issues that may cause the errors mentioned in this topic, see Microsoft Knowledge Base article 924625, [When you use Outlook with an Exchange 2007 mailbox, you cannot connect to Exchange 2007, and you receive an error message](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=924625).

For more information about Outlook 2003 connectivity with Exchange Server 2010, including additional remediation methods, see the Microsoft Knowledge Base article, [Outlook connection issues with Exchange 2010 mailboxes because of the RPC encryption requirement](https://support.microsoft.com/kb/2006508).

For information about the Set-MailboxServer cmdlet and MAPIEncryptionRequired attribute, see [Set-MailboxServer](https://go.microsoft.com/fwlink/?linkid=161822).

For more information about deploying Exchange 2010 with Outlook 2003 clients, see [Concern: Is Having Outlook 2003 Clients Going to Prevent Me from Deploying Exchange 2010?](https://social.technet.microsoft.com/wiki/contents/articles/concern-is-having-outlook-2003-clients-going-to-prevent-me-from-deploying-exchange-2010.aspx).

</div>

</div>

<span> </span>

</div>

</div>

</div>

