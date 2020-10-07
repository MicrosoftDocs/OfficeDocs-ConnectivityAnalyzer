---
title: A Network Error Occurred while Communicating with Remote Host
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

# A Network Error Occurred while Communicating with Remote Host

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-11-18_

The Microsoft Remote Connectivity Analyzer attempts to make a TCP connection to the host provided during the test. If the Microsoft Remote Connectivity Analyzer tool is unable to establish a TCP connection over port 80 and port 443 with the host, then it displays the following error message.

"A network connection error occurred while communicating with the remote host: '0'"

Where "0" is replaced with additional information as to why the connection failed.

ExRCA must be able to establish a TCP session over ports 25, 80, and 443 during various tests performed by the tool.

<div>

## For More Information

Connection failures of this type are commonly caused by the following:

  - The server is down.

  - The specified port is not listening for TCP connections.

  - A firewall, proxy server, or hardware device is blocking the connection to your server.

  - The network is congested.

**To correct this error**

1.  Ensure that the server is up and available to the network by troubleshooting the network connectivity by using Microsoft Knowledge Base article 323388, "How To Diagnose and Test TCP/IP or NetBIOS Network Connections in Windows Server 2003" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=323388](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=323388)).

2.  Use the netstat.exe utility to determine whether the appropriate service is actually listening on the port being tested using Microsoft Knowledge Base article 323352, "How To Determine Which Program Uses or Blocks Specific Transmission Control Protocol Ports in Windows Server 2003" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=323352](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=323352)).

3.  Use the Portqry.exe tool to test the TCP connectivity from different points within and outside your network to determine whether a network device is blocking connectivity to the specified port. For more information, see Microsoft Knowledge Base article "How to Use Portqry.exe to Troubleshoot Microsoft Exchange Server Connectivity Issues" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=310298](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=310298)).

4.  Use Network Monitor to capture network traffic to troubleshoot your issue. For more information, see Microsoft Knowledge Base article "Information about Network Monitor 3.2 in Windows Vista" ([https://go.microsoft.com/fwlink/?LinkId=3052\&kbid=955998](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=955998)).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

