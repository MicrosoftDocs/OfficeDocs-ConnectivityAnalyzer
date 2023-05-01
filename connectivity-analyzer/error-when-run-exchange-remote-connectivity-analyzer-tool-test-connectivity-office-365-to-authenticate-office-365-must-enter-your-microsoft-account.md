---
title: 'Error when you run the Microsoft Remote Connectivity Analyzer tool to test connectivity to Office 365: "To authenticate to Office 365, you must enter your Microsoft account"'
author: bradhugh
ms.author: bradhugh
manager: tpolitis
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: 'Error when you run the Microsoft Remote Connectivity Analyzer tool to test connectivity to Office 365: "To authenticate to Office 365, you must enter your Microsoft account"' 
ms.date: 05/08/2020
---

# Error when you run the Microsoft Remote Connectivity Analyzer tool to test connectivity to Office 365: \"To authenticate to Office 365, you must enter your Microsoft account\"


_**Topic Last Modified:** 2012-11-06_

If an issue occurs when you try to run the Microsoft Remote Connectivity Analyzer tool to test connectivity to Microsoft Office 365, you may receive the following error message: To authenticate to Office 365, you must enter your Microsoft account. This is your User Principal Name and in many cases will be something like user@contoso.com.

The following sections can help you to resolve this issue.

## Information for end-users

Office 365 customers who experience issues when they run the Microsoft Remote Connectivity Analyzer tool can use the information in the following table to help resolve the issue.


|Possible cause| Resolution |
|---------------|----------------------|
|You are using an incorrect user name.| Enter your Office 365 user ID. Your Office 365 user ID is your user principal name (UPN). For example, enter **jane@contoso.com**. <br> <br> If you don't know your Office 365 user ID, contact your administrator for help. |
| Your password has expired. | Contact your administrator to reset your password. For more information, see Microsoft Knowledge Base article 2606983: [An Office 365 user or an Office 365 administrator forgot his or her password](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2606983). |
| Your Office 365 user account isn't activated. | To get started with Office 365, you have to activate your account. To do this, sign in to the [Office 365 portal](https://portal.microsoftonline.com) for the first time by using your temporary password, and then create a new password to use when you sign in. <br><br> For more information, go to one of the following Office 365 websites:<br><br>- If you have Office 365 for enterprises: [Change your password](https://onlinehelp.microsoft.com/office365-enterprises/ff637578.aspx) <br>- If you have Office 365 for professionals and small businesses: [Change your password](https://onlinehelp.microsoft.com/office365-enterprises/ff637578.aspx)
Your Microsoft Logon account is blocked. | Wait 15 minutes, and then try to log on again. If the problem recurs, your administrator may have to reset your password to unblock your account. For more information, see Microsoft Knowledge Base article 2412085: [You cannot sign in to Microsoft Online Services](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085). |

## Information for administrators

Office 365 customers who experience issues when they run the Microsoft Remote Connectivity Analyzer tool can use the information in the following table to help resolve the issue.


|Possible cause| Resolution |
|---------------|----------------------|
|You are using an incorrect user name.| Enter your Office 365 user ID. Your Office 365 user ID is your user principal name (UPN). For example, enter **jane@contoso.com**. <br> <br> For more information about how to resolve this issue, see [What is my user ID and why do I need it?](https://onlinehelp.microsoft.com/office365-smallbusinesses/gg549202.aspx). |
| Your password has expired. | For information about how to resolve this issue, see Microsoft Knowledge Base article 2412085: [You cannot sign in to Microsoft Online Services](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085).<br><br>Also, see the following articles:<br><br>[Reset a user's password](https://onlinehelp.microsoft.com/office365-smallbusinesses/ff637553.aspx)<br>[Reset your administrator password](https://onlinehelp.microsoft.com/office365-smallbusinesses/gg192871.aspx) |
| Your Office 365 user account isn't activated. | For information about how to resolve this issue, see Microsoft Knowledge Base article 2412085: [You cannot sign in to Microsoft Online Services](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085).
Your Microsoft Logon account is blocked. | Wait 15 minutes, and then try to log on again. If the problem recurs, reset your password to unblock your account. For more information, see Microsoft Knowledge Base article 2412085: [You cannot sign in to Microsoft Online Services](https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085). |

## More information

For more information, go to the following Office 365 websites:

  - [Sign-in and passwords](https://onlinehelp.microsoft.com/office365-smallbusinesses/ff637538.aspx)

  - [User accounts and permissions](https://onlinehelp.microsoft.com/office365-smallbusinesses/ff637545.aspx)
