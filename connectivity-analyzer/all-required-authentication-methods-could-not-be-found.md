---
title: All Required Authentication Methods Could Not be Found
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

# All Required Authentication Methods Could Not be Found

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-11-18_

The Microsoft Exchange Analyzer tool sends an HTTP request to test the authentication methods of the specified service. If a 401 Unauthorized Response is received, then the Exchange Remote Connectivity Analyzer tool expects certain WWW-Authenticate headers in the response. Certain services such as Exchange ActiveSync and Outlook Anywhere (RPC over HTTP) do not negotiate an authentication method with the remote server. These clients have a pre-defined authentication method that is sent with each request. If this authentication method is not enabled on the remote server, then the Exchange Remote Connectivity Analyzer generates the following error:

"All Required Authentication Methods could not be found."

If the pre-defined authentication method isn't enabled on the remote server, then users may experience the following issues:

  - Mobile device users connecting using Exchange ActiveSync will be unable to successfully connect.

  - Microsoft Office Outlook users may be unable to connect using Outlook Anywhere.

<div>

## For More Information

**To correct this error**

1.  Confirm that Basic authentication is enabled on the Exchange ActiveSync virtual directory in the Exchange Management Console and in IIS on the Microsoft-Server-ActiveSync virtual directory

2.  For Outlook Anywhere users, verify the following server and client settings:
    
    1.  Confirm that Basic and/or Integrated Windows Authentication is enabled on the /Rpc virtual directory in IIS. Please note that these authentication methods should be managed through the Set-OutlookAnywhere cmdlet and not directly in IIS.

3.  Confirm that Basic or NT LAN Manager (NTLM) authentication is selected under Exchange Proxy Settings in Microsoft Outlook. This setting should match the authentication method you have enabled in IIS. If this setting is being obtained via Autodiscover, then ensure that your ClientAuthenticationMethod or DefaultAuthenticationMethod is specified properly on your Outlook Anywhere Configuration.

For more information, review the following documentation and confirm that the virtual directories on your Exchange server have the proper authentication methods enabled for each application or service:

  - To see a list of the default authentication methods for Exchange Server 2007 applications and services, see the following Microsoft blog post [Default settings for Exchange-related virtual directories in Exchange Server 2007](https://go.microsoft.com/fwlink/?linkid=161402).

  - For information about the supported authentication methods available for managing Exchange applications hosted on an Exchange 2007 Client Access server, see [Managing Client Access Security](https://go.microsoft.com/fwlink/?linkid=100585).

  - For details about configuring authentication specific to Exchange 2007 Outlook Anywhere, see the following documentation on TechNet: [How to Configure Authentication for Outlook Anywhere](https://go.microsoft.com/fwlink/?linkid=161403).

  - For information about configuring authentication for Web applications on Exchange Server 2003 and Exchange 2000 Server, see [Front-End and Back-End Server Topology Guide for Microsoft Exchange Server 2003 and Exchange 2000 Server](https://go.microsoft.com/fwlink/?linkid=161404).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

