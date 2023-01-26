---
title: The ActiveSync OPTIONS command returned an HTTP 401 Error
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'When the Microsoft Best Practices Analyzer tests ActiveSync connectivity, the ActiveSync test returns the following error message: Errors were encountered while testing the Exchange ActiveSync session.'
ms.date: 05/08/2020
---

# The ActiveSync OPTIONS command returned an HTTP 401 Error

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2013-02-05_

Microsoft Exchange ActiveSync enables the synchronization of mailbox information with mobile devices. To do this, Exchange uses the Microsoft-Server-ActiveSync virtual directory in Internet Information Services (IIS).

When the Microsoft Best Practices Analyzer tests ActiveSync connectivity, the ActiveSync test returns the following error message:

   *An ActiveSync session is being attempted with the server.
   Errors were encountered while testing the Exchange ActiveSync session.
   Test Steps
   Attempting to send the OPTIONS command to the server.
   Testing of the OPTIONS command failed. For more information, see Additional Details.
   Additional Details
   An HTTP 401 Unauthorized response was received from the remote IIS server. This is usually the result of an incorrect username or password. If you are attempting to log onto an Office 365 service, ensure you are using your full User Principal Name (UPN).*

This error typically occurs in an Exchange 2010 or Exchange 2007 environment where the target mailbox resides on an Exchange 2003 server and Basic Authentication is configured on the **Microsoft-Server-ActiveSync** virtual directory.

When Exchange 2010 or Exchange 2007 coexist with Exchange 2003, Integrated Windows authentication must be enabled on the **Microsoft-Server-ActiveSync** virtual directory that is hosted on the Exchange 2003 mailbox server. This allows the Exchange 2010 or Exchange 2007 Client Access server and the Exchange 2003 back-end server to communicate by using Kerberos authentication.

The most common cause for this error is an incorrect username or password.  If you are using Office 365, make sure that you log in by using your full User Principal Name (UPN). For example, log in by using the following: user@domain.com.  If the login information is correct, we recommend that you use the following procedure to help resolve this issue.

<div class="alert">


> [!IMPORTANT]
> You must use Exchange System Manager to adjust the authentication settings of the Exchange ActiveSync virtual directory. Do not use IIS Manager to change the authentication setting on the ActiveSync virtual directory. This is because the Exchange System Attendant overwrites the settings that are stored in Active Directory.


</div>

**To modify permissions on the Microsoft-Server-ActiveSync virtual directory in Exchange 2003 Server Manager**

1.  Install the following hotfix on the Exchange 2003 server:  
      
    [Event ID 1036 is logged on an Exchange 2007 server that is running the CAS role when mobile devices connect to the Exchange 2007 server to access mailboxes on an Exchange 2003 back-end server](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=937031)

2.  Start Exchange System Manager on the Exchange 2003 Mailbox server.

3.  Expand **Administrative Groups**, expand **Administrative\_Group\_Name**, and then expand **Servers**.

4.  Expand ServerName, expand **Protocols**, and then expand **HTTP**.

5.  Expand **Exchange Virtual Server**, right-click **Microsoft-Server-ActiveSync**, and then click **Properties**.

6.  Click the **Access** tab, and then click **Authentication**.

7.  Click to select the **Integrated Windows Authentication** check box.

8.  Click **OK** two times.

9.  To verify that this data successfully replicated to the metabase on the Exchange server, follow these steps:
    
    1.  Open the Internet Information Services (IIS) Manager under **Administrative Tools**.
    
    2.  Expand the **ServerName**, expand **Web Sites**, and then expand **Default Web Site**.
    
    3.  Right-click **Microsoft-Server-ActiveSync**, and then click **Properties**.
    
    4.  Click the **Directory Security** tab, and then select the **Edit** button under **Authentication and access control**.
    
    5.  Verify that the **Integrated Windows Authentication** check box is selected.
        
        <div class="alert">
        

        > [!NOTE]
        > If this check box is selected, you have successfully replicated the change that was made in the Exchange System Manager to the metabase on the Exchange server.

        
        </div>
    
    6.  Click **Cancel** two times, and then exit Internet Information Services (IIS) Manager.

For more information, see step 7 under “Installing Exchange 2010” in the following TechNet topic: [Upgrade from Exchange 2003 Client Access](https://go.microsoft.com/fwlink/p/?linkid=280550)

</div>

<span> </span>

</div>

</div>

</div>

