---
title: You must uninstall all interim updates before you install Exchange Server 2010 Service Pack 2
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
localization_priority: Normal
description: 
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# You must uninstall all interim updates before you install Exchange Server 2010 Service Pack 2

</div>

<div id="mainSection">

<div id="mainBody">

\[This topic is intended to address a specific issue called out by the Exchange Server Analyzer Tool. You should apply it only to systems that have had the Exchange Server Analyzer Tool run against them and are experiencing that specific issue. The Exchange Server Analyzer Tool, available as a free download, remotely collects configuration data from each server in the topology and automatically analyzes the data. The resulting report details important configuration issues, potential problems, and nondefault product settings. By following these recommendations, you can achieve better performance, scalability, reliability, and uptime. For more information about the tool or to download the latest versions, see "Microsoft Exchange Analyzers" at <http://go.microsoft.com/fwlink/?linkid=34707>.\] <span> </span>

_**Topic Last Modified:** 2011-11-02_

The Microsoft Exchange Best Practices Analyzer Tool checks whether a Microsoft Exchange Server 2010 interim update (IU) is installed on the computer that is running Exchange 2010. If an IU is installed, Microsoft Exchange Server 2010 Service Pack 2 (SP2) cannot be installed.

To install Exchange 2010 SP2, you must uninstall the IU. After the IU is uninstalled, install Exchange 2010 SP2.

To uninstall the IU, follow these steps:

1.  In **Control Panel**, double-click **Programs and Features**.

2.  In the **Currently installed programs** list, click **Interim Update for Exchange Server 2010** **(KB**<span></span>*xxxxxx*<span></span>**)**, where xxxxxx is the Knowledge Base article number that is associated with the IU.

3.  Click **Remove**.

4.  At a command prompt, run **sn.exe -Vu \*** to enable strong name verification.

5.  Run **sn.exe –Vl** to verify that strong name verification is enabled.

</div>

<span> </span>

</div>

</div>

</div>

