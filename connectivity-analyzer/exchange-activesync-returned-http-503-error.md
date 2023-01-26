---
title: Exchange ActiveSync Returned an HTTP 503 Error
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'Error: "Exchange ActiveSync returned an HTTP 451 response. (Device Misconfigured)."'
ms.date: 05/08/2020
---

# Exchange ActiveSync Returned an HTTP 503 Error

_**Topic Last Modified:** 2013-03-21_

The Microsoft Remote Connectivity Analyzer includes the **Attempting the FolderSync command on the Exchange ActiveSync session** test. This test determines whether the information store on the Microsoft Exchange 2010 server is mounted.

If the information store is dismounted, you receive the following error message:

"Exchange ActiveSync returned an HTTP 451 response. (Device Misconfigured)."

## More Information

For information about how to start the Information Store service, see [How to Start the Microsoft Exchange Information Store Service (MSExchangeIS)](https://technet.microsoft.com/library/aa998163\(v=exchg.80\)).

For information about how to mount the information store in Exchange 2010 server, see [Mount a Database](https://go.microsoft.com/fwlink/p/?linkid=286791).

