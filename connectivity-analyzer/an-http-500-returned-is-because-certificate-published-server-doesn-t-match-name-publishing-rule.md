---
title: An HTTP 500 was Returned to ISA Because the Certificate on the Published Server Doesn't Match the Name in the Publishing Rule
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

# An HTTP 500 was Returned to ISA Because the Certificate on the Published Server Doesn't Match the Name in the Publishing Rule

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2009-08-18_

The Microsoft Remote Connectivity Analyzer sends an HTTP(s) request to the requested URL. If an HTTP 500 response is received and the page includes the error code -2146893022, then the Microsoft Remote Connectivity Analyzer tool returns the following error.

"An HTTP 500 was returned to ISA because the certificate on the published server doesn't match the name in the publishing rule."

Microsoft Remote Connectivity Analyzer issues an error when you use Microsoft Internet Security and Acceleration (ISA) Server 2006 or ISA Server 2004 to publish a Web site that requires a Secure Sockets Layer (SSL) connection and the SSL client request from ISA Server does not match the common name that is specified in the Web site certificate. The most common symptom occurs when users receive the following error message when they try to connect to the Web site.

"Error Code 500 Internal Server Error.  
The target principal name is incorrect. (-2146893022)."

<div>

## Resolution

Check that the certificate names follow the guidelines below:

  - For the certificate on the ISA Server computer, the name must match the name that the external clients specify to reach the site.

  - For the certificate on the published Web server, the name must match the name that appears on the To tab of the rule.

  - In the case of the certificate on the Web server in a server publishing scenario, the certificate should have the name that users will use to connect to the server.

To troubleshoot, either obtain a new certificate that matches the required name, or modify the required name to match the certificate’s common name. In addition, make sure that the ISA Server can resolve the name to the IP address of the published Web site. If you modify the name on the To tab, one way to ensure that the name can be resolved is to add a Hosts file entry on the ISA Server computer (WINNT\\system32\\drivers\\etc\\hosts) to map the name and IP address of the published site.

</div>

<div>

## For More Information

To learn more about troubleshooting SSL certificates when using ISA Server, see "[Troubleshooting SSL Certificates in ISA Server 2004 Publishing](https://go.microsoft.com/fwlink/?linkid=48904)."

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

