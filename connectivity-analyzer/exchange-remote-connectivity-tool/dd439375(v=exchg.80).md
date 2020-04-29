---
title: Exchange ActiveSync Returned an HTTP 500 Error
TOCTitle: Exchange ActiveSync Returned an HTTP 500 Error
ms:assetid: 620c5ce8-3595-4658-9a7a-ec76c10e4a69
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd439375(v=EXCHG.80)
ms:contentKeyID: 20045822
ms.date: 07/23/2014
mtps_version: v=EXCHG.80
---

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="http://msdn.microsoft.com/en-us/">

<div data-asp="http://msdn2.microsoft.com/asp">

# Exchange ActiveSync Returned an HTTP 500 Error

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2010-06-25_

The Microsoft Exchange Analyzer tool sends Exchange ActiveSync commands to test for Exchange ActiveSync connectivity. If the FolderSync command (the first command in the sequence) returns an HTTP 500 error, then the Exchange Server Remote Connectivity Analyzer tool returns the following error.

"Exchange ActiveSync returned an HTTP 500 response."

<div>

## For More Information

You may experience this error if you have an Exchange 2003 server without a front-end server and are using Secure Sockets Layer (SSL) or forms-based authentication. If this is the case, see Microsoft Knowledge Base article, "Exchange ActiveSync and Outlook Mobile Access errors occur when SSL or forms-based authentication is required for Exchange Server 2003" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=817379](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=817379)).

In Exchange 2003, ActiveSync requires Kerberos authentication to work properly between the front-end and the back-end servers. Some common reasons for Kerberos authentication in IIS not working are:

  - Integrated Windows Authentication may not be enabled on the back-end server's "/Exchange" virtual directory.

  - The affected users may be members of too many groups causing their user tokens to be larger than the maximum allowed size.
    
    <div class="alert">
    

    > [!NOTE]
    > The authentication methods on Exchange Server virtual directories should be managed using the Exchange System Manager and not Internet Information Services (IIS) Manager.

    
    </div>

For more information, see Microsoft Knowledge Base article, "How to troubleshoot server ActiveSync HTTP error codes" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=330463](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=330463)).

In Exchange Server 2010, you may also experience this issue if the Exchange Servers group does not have the appropriate permission to the mailbox object in Active Directory. The most common cause for this is broken Access Control List (ACL) inheritance in Active Directory.

To check whether inheritance is disabled on the user:

1.  Open **Active Directory Users and Computers**.

2.  On the menu at the top of the console, click **View** \> **Advanced Features**.

3.  Locate and right-click the mailbox account in the console, and then click **Properties**.

4.  Click the **Security** tab.

5.  Click **Advanced**.

6.  Make sure that the check box for "Include inheritable permissions from this object's parent" is selected.

If the user is a member of certain protected groups such as Domain Administrators, it is normal for this box to be unchecked. If you are experiencing a problem with members of these protected groups you should check the permissions on the AdminSDHolder object.

<div class="alert">


> [!NOTE]
> We recommend that you do not use accounts that are members of protected groups for e-mail purposes. If you require the rights that are afforded to a protected group, we recommend that you have two Active Directory user accounts. These Active Directory accounts include one user account that is added to a protected group and one user account that is used for e-mail purposes and at all other times.


</div>

For more information, see TechNet Magazine article, "AdminSDHolder, Protected Groups and SDPROP" (<http://technet.microsoft.com/en-us/magazine/2009.09.sdadminholder.aspx>).

The Exchange Remote Connectivity Analyzer is a new tool with limited documentation at this time. In an effort to improve the documentation for each of the errors you might receive, we would like to solicit additional information from the community. Please use the Community Content section below to post additional reasons why you failed at this point. If you need technical assistance, please create a post in the appropriate [Exchange TechNet forum](http://go.microsoft.com/fwlink/?linkid=73420) or contact [support](http://go.microsoft.com/fwlink/?linkid=8158).

</div>

</div>

<span> </span>

</div>

</div>

</div>

