---
title: Exchange ActiveSync Returned an HTTP 500 Error
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'The Microsoft Remote Connectivity Analyzer tool returns the following error: "Exchange ActiveSync returned an HTTP 500 response."'
ms.date: 05/08/2020
---

# Exchange ActiveSync Returned an HTTP 500 Error

_**Topic Last Modified:** 2010-06-25_

The Microsoft Remote Connectivity Analyzer sends Exchange ActiveSync commands to test for Exchange ActiveSync connectivity. If the FolderSync command (the first command in the sequence) returns an HTTP 500 error, then the Microsoft Remote Connectivity Analyzer tool returns the following error.

"Exchange ActiveSync returned an HTTP 500 response."

## For More Information

You may experience this error if you have an Exchange 2003 server without a front-end server and are using Secure Sockets Layer (SSL) or forms-based authentication. If this is the case, see Microsoft Knowledge Base article, [Exchange ActiveSync and Outlook Mobile Access errors occur when SSL or forms-based authentication is required for Exchange Server 2003](https://go.microsoft.com/fwlink/?linkid=3052\&kbid=817379).

In Exchange 2003, ActiveSync requires Kerberos authentication to work properly between the front-end and the back-end servers. Some common reasons for Kerberos authentication in IIS not working are:

  - Integrated Windows Authentication may not be enabled on the back-end server's "/Exchange" virtual directory.

  - The affected users may be members of too many groups causing their user tokens to be larger than the maximum allowed size.    

    > [!NOTE]
    > The authentication methods on Exchange Server virtual directories should be managed using the Exchange System Manager and not Internet Information Services (IIS) Manager.

For more information, see Microsoft Knowledge Base article, [How to troubleshoot server ActiveSync HTTP error codes](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=330463).

In Exchange Server 2010, you may also experience this issue if the Exchange Servers group does not have the appropriate permission to the mailbox object in Active Directory. The most common cause for this is broken Access Control List (ACL) inheritance in Active Directory.

To check whether inheritance is disabled on the user:

1.  Open **Active Directory Users and Computers**.

2.  On the menu at the top of the console, click **View** \> **Advanced Features**.

3.  Locate and right-click the mailbox account in the console, and then click **Properties**.

4.  Click the **Security** tab.

5.  Click **Advanced**.

6.  Make sure that the check box for "Include inheritable permissions from this object's parent" is selected.

If the user is a member of certain protected groups such as Domain Administrators, it is normal for this box to be unchecked. If you are experiencing a problem with members of these protected groups you should check the permissions on the AdminSDHolder object.

> [!NOTE]
> We recommend that you do not use accounts that are members of protected groups for e-mail purposes. If you require the rights that are afforded to a protected group, we recommend that you have two Active Directory user accounts. These Active Directory accounts include one user account that is added to a protected group and one user account that is used for e-mail purposes and at all other times.

For more information, see TechNet Magazine article, [AdminSDHolder, Protected Groups and SDPROP](https://technet.microsoft.com/magazine/2009.09.sdadminholder.aspx).

The Microsoft Remote Connectivity Analyzer has limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](https://go.microsoft.com/fwlink/?linkid=73420) or contact [support](https://go.microsoft.com/fwlink/?linkid=8158).
