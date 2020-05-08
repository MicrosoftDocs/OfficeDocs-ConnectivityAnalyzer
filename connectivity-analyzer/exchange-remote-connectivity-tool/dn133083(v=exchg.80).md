---
title: Message Header Analyzer
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

# Message Header Analyzer

</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Topic Last Modified:** 2013-03-29_

If you’ve ever had to troubleshoot issues that occur in an email system, regardless of which email service you use, you may be familiar with message headers. Message headers contain information about the path that a message took, in addition to other valuable metadata.

Header can answer various questions about a message, such as the following:

  - Why did the message take so long to arrive?

  - Why did the message end up in my Junk/Spam folder?

  - What hops did the message take to arrive at my Inbox?

Header Analyzers, such as the one included in Microsoft Remote Connectivity Analyzer, can help you view and analyze message headers by displaying the information in a user-friendly manner and also by calling out various issues, such as suspected delivery delays that may require your attention.

Message headers are more useful when you read the recipient’s copy of a message. Headers in the sender’s copy are not necessarily useful. If you want to have message headers sent to you, the recipient will have to either extract the headers or forward the original email message as an attachment. (Most mail clients offer this capability as an option, but do not do this by default.)

After you obtain the message headers, paste them into Message Header Analyzer, and then click **Parse**. The Analyzer shows you a breakdown of each hop that the message took, and details about all the non-received messages.

<div class="alert">


> [!NOTE]
> If a message never arrived at its intended destination, you will have to try a different method to obtain this information, such as using the message-tracking features that are offered by Microsoft&nbsp;Exchange Server or Microsoft&nbsp;Exchange Online. These features maintain a log of all messages that are handled by the system. Generally, you will have to work with your Helpdesk or system administrator in this situation.


</div>

<div>

## How to View Message Headers

For directions to view message headers, go to the following sections, as appropriate for the email clients that you use:

  - <span></span>  
    Outlook 2013, Outlook 2010, or Outlook 2007

  - <span></span>  
    Outlook Web App

  - <span></span>  
    Windows Mail App

  - <span></span>  
    Windows Mail (Desktop)

  - <span></span>  
    Thunderbird client (IMAP)

  - <span></span>  
    Mobile devices (Windows Phone, iPhone, iPad, and so on)

  - <span></span>  
    Outlook.com

  - <span></span>  
    Apple Mail

  - <span></span>  
    Gmail.com

<span id="Outlook2013Outlook2010orOutlook2007"></span>

<div>

## Outlook 2013, Outlook 2010, or Outlook 2007

Although these versions of Outlook differ slightly, the process for viewing message headers is basically the same. For any version, follow these steps:

1.  Open the message.

2.  On the **File** tab, click **Properties** in the **Info** area.
    
    Or, click the Dialog Box Launcher in the lower-right corner of the **Tags** group on the Ribbon.

3.  In the **Properties** dialog box, locate the message headers in the **Internet headers** area.

For more information, see [View e-mail message headers](http://office.microsoft.com/en-us/outlook-help/view-e-mail-message-headers-ha001230300.aspx)

</div>

<span id="OutlookWebApp"></span>

<div>

## Outlook Web App

  - **Exchange Server 2007 (OWA)**   Open the message, and then click the “Message Details" icon. In the **Message Details** dialog box, locate the message headers in the **Internet Mail Headers** area.

  - **Exchange Server 2013 OWA**   Download the [Message Headers Analyzer](http://office.microsoft.com/en-us/store/message-header-analyzer-wa104005406.aspx?queryid=69795c55-fbb0-4a0d-8ec3-d779b421a7ea%26css=headers%26ctt=1) app from the Office app store.

</div>

<span id="WindowsMailApp"></span>

<div>

## Windows Mail App

Currently, Windows 8 Mail App does not offer this functionality.

</div>

<span id="WindowsMailDesktop"></span>

<div>

## Windows Mail (Desktop)

1.  In the Inbox, right-click the message, and then click **Properties**.

2.  Click the **Details** tab to view the message headers.

</div>

<span id="ThunderbirdClientIMAP"></span>

<div>

## Thunderbird client (IMAP)

1.  Double-click to open the message.

2.  On the **View** menu, click **Message Source**. Message headers are displayed in a new window in the full message source.

</div>

<span id="MobileDevices"></span>

<div>

## Mobile devices (Windows Phone, iPhone, iPad, and so on)

Some mobile apps have this capability. However, most mobile devices do not have a good method to retrieve message headers. For now, we recommend that you use a computer to log on to your web mail client that offers this functionality.

</div>

<span id="Outlook_com"></span>

<div>

## Outlook.com

In any folder, right-click a message, and then click **View message source**. The message headers and all message sources are displayed in a browser window.

</div>

<span id="AppleMail"></span>

<div>

## Apple Mail

For current versions of Apple Mail, follow these steps:

1.  Click the message.

2.  On the **View** menu, click **Message**.

3.  Click **Long Headers**. Locate the message headers in the window underneath the Inbox.

</div>

<span id="Gmail_com"></span>

<div>

## Gmail.com

1.  Open the message.

2.  At the top of the message, click the down arrow next to **Reply**, and then click **Show Original**. Locate the full headers in the new browser window that opens.

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

