---
title: A Network Error Occurred while Communicating with Remote Host
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 
---

# A Network Error Occurred while Communicating with Remote Host

The Microsoft Remote Connectivity Analyzer attempts to make a TCP connection to the host provided during the test. If the Microsoft Remote Connectivity Analyzer tool is unable to establish a TCP connection over port 80 and port 443 with the host, then it displays the following error message.

"A network connection error occurred while communicating with the remote host: '0'"

Where "0" is replaced with additional information as to why the connection failed.

The Remote Connectivity Analyzer must be able to establish a TCP session over ports 25, 80, and 443 during various tests performed by the tool.

## For More Information

Connection failures of this type are commonly caused by the following:

- The server is down.

- The specified port is not listening for TCP connections.

- A firewall, proxy server, or hardware device is blocking the connection to your server.

- The network is congested.

### To correct this error

1. Ensure that the server is up and available to the network.

2. Use the netstat.exe utility to determine whether the appropriate service is actually listening on the port being tested. For syntax, see [Windows Commands: netstat](/windows-server/administration/windows-commands/netstat).

3. Use the Portqry tool to test the TCP connectivity from different points within and outside your network to determine whether a network device is blocking connectivity to the specified port. For more information, see Microsoft Knowledge Base article "Verify network ports are not blocked" ([https://support.microsoft.com/topic/f48c0637-95f0-50d7-9d2e-cdeead712052](https://support.microsoft.com/topic/f48c0637-95f0-50d7-9d2e-cdeead712052)).

4. Collect network traces (packet captures) to troubleshoot your issue. You can use packet capture software or packet capture features available on your network devices to collect network traces.

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
