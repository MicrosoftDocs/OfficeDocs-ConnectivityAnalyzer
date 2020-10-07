---
title: RPC Server Unavailable Error was Thrown by the RPC Runtime
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

# RPC Server Unavailable Error was Thrown by the RPC Runtime

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2010-08-20_

The Microsoft Remote Connectivity Analyzer issues an RPCPing to several Exchange Server endpoints to simulate the connections that are made when a Microsoft Outlook client connects to Microsoft Exchange Server 2007 Outlook Anywhere or to Microsoft Exchange Server 2003 RPC over HTTP. To connect, the client must be able to successfully connect to the HTTP endpoints of the Microsoft Exchange Information Store, the referral service of DSProxy within the Exchange System Attendant service, and to the DSProxy service within the Exchange System Attendant service over ports 6001, 6002, and 6004, respectively. If the test fails, the Microsoft Remote Connectivity Analyzer generates the following error:

"RPC Server Unavailable error (1722) was thrown by the RPC Runtime"

This issue can be caused by any of the following conditions:

  - Failures in DNS name resolution

  - Missing or invalid ValidPorts key in the registry of the Internet-facing Exchange 2007 Client Access server or of the Exchange 2003 server

  - Exchange services not listening on the required endpoints

  - Firewalls blocking the required ports

<div>

## For More Information

To resolve this issue, do the following:

  - Troubleshoot name resolution, and verify that the server acting as the RPC proxy can correctly resolve the internal fully-qualified domain name (FQDN) of the mailbox server or of Exchange 2003.

  - Open Registry Editor on the Client Access server or on the front-end server, and verify that the ValidPorts registry value exists under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc\\Rpcproxy. Also confirm that the key includes the NetBIOS and FQDN for all mailbox servers and for each required port (that is, for ports 6001, 6002, and 6004).

  - To test endpoint connectivity, open a Telnet session on the Client Access server or on the front-end server, and then Telnet to each port on the mailbox servers (that is, on ports 6001, 6002, and 6004). If you cannot successfully Telnet to any of the ports, and if there is a firewall between the servers, check your firewall configuration.

  - If you are receiving this error on port 6004, and if you are using Exchange 2007 on Windows Server 2008, make sure that you have Exchange 2007 SP1 RU4 or later installed. This is because a problem that affects IPv6 can cause DSProxy requests to fail and generate this error. For more information about this specific issue, see Microsoft Knowledge Base article, "[You are prompted for your credentials three times and you receive an error message when you use the Outlook Anywhere feature to connect to an Exchange Server 2007 Service Pack 1–based server that is running Windows Server 2008](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=950138)".

<div class="alert">


> [!NOTE]
> Modification of the ValidPorts does not apply to Microsoft Exchange Server 2010. In Exchange 2010, the registry value is ValidPorts_Exchange. You do not have to manually modify this value. This value is created by automatic configuration in Client Access Server settings.


</div>

</div>

<div>

## Additional Resources

  - For information about how to troubleshoot DNS, see [Troubleshooting DNS](https://go.microsoft.com/fwlink/?linkid=63003).

  - To learn more about Exchange 2007 Outlook Anywhere and the ValidPorts key, see [How does Outlook Anywhere work (and not work)?](https://go.microsoft.com/fwlink/?linkid=148104)

  - To learn more about Exchange 2003 RPC over HTTP and the ValidPorts key, see [RPC over HTTP Interactions on the RPC Proxy Server](https://go.microsoft.com/fwlink/?linkid=161819).

  - To review another option to solve the Outlook Anywhere connectivity issue with Exchange 2007 SP1 on Windows Server 2008, see [Outlook Anywhere Client Connectivity Issue Because of TCP/IPv6](https://go.microsoft.com/fwlink/?linkid=161821).

Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors that you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional information about why you failed at this point. If you require technical assistance, create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

