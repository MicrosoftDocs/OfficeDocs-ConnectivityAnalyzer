---
title: An HTTP 403.4 was Returned Because SSL was Required on the Virtual Directory
TOCTitle: An HTTP 403.4 was Returned Because SSL was Required on the Virtual Directory
ms:assetid: 1ce88d57-a5e6-4797-b3fe-1ba0f2410f11
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439365(v=EXCHG.80)
ms:contentKeyID: 20045812
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# An HTTP 403.4 was Returned Because SSL was Required on the Virtual Directory

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2011-01-21_

The Microsoft Exchange Analyzer tool attempts to connect and authenticate to the Web site or virtual directory using the credentials and protocol supplied by the user. If the connection is attempted using a non-secure protocol, then the test may fail and return the following error.

"An HTTP 403.4 was returned because SSL was required on the virtual directory."

This issue occurs whenever a connection is attempted using a non-secure protocol (HTTP), but the server only allows Secure Sockets Layer (SSL) HTTPS connections. The most common scenario is attempting to connect to the website or virtual directory using HTTP instead of HTTPS.

<div>

## For More Information

To correct this error, do one of the following.

  - Use the HTTPS protocol to visit the Web site. That is, make sure that the URL begins with "https://".

  - In the SSL settings for the Web site, clear the Require SSL check box. To do this, perform the following steps.

For Windows 2003:

1.  Click **Start**, click **Run**, type Inetmgr, and then click **OK**.

2.  In Internet Information Services (IIS) Manager, expand Computer\_Name , expand Web Sites, and then right-click the Web site that you want to remove the SSL feature from.

3.  Click **Properties**.

4.  Click the Security tab.

5.  Under Secure Communications, click the **Edit** button.

6.  Clear the following checkboxes:
    
      - Require Secure Channel when accessing this resource
    
      - Require 128-bit Encryption

7.  Click OK.

For Windows 2008:

1.  Click **Start**, click **Run**, type Inetmgr, and then click **OK**.

2.  In Internet Information Services (IIS) Manager, expand Computer\_Name , expand Sites, and then click the Web site that you want to remove the SSL feature from.

3.  In the Middle Window pane, double click on SSL Settings.

4.  Clear the following checkboxes:
    
      - Require Secure Channel when accessing this resource
    
      - Require 128-bit Encryption

5.  Click **Apply** in the right pane.

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point.  If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

