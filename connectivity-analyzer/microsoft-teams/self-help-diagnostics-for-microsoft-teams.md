---
title: Self-help diagnostics for Microsoft Teams administrators and end users
author: CarlosFarrica
ms.author: cafarric
manager: jweum
audience: ITPro 
ms.topic: article 
ms.service: remote-connect-tool
ms.localizationpriority: medium
description: Description of currently available diagnostics for Microsoft Teams with scenario descriptions
ms.date: 09/08/2023
---

# Self-help diagnostics for Microsoft Teams administrators and end users

## Summary
As Microsoft Teams usage grows, Microsoft has developed Teams-specific diagnostic scenarios that cover top support topics and the most common tasks for which administrators or end users request help. It is important to note that while these diagnostics cannot make changes to your tenant, they do provide insight into known issues and the instructions that allow you to fix the behavior quickly.

> [!NOTE]
> Currently the Microsoft Remote Connectivity Analyzer tool does not support Microsoft 365 Government environments (GCC or GCC High).

## What scenarios are currently covered?
The following diagnostics are currently available with brief scenario descriptions.

| Diagnostic |	Description |
|---|---|
| [Teams sign in](https://testconnectivity.microsoft.com/tests/TeamsSignin/input)	| This test verifies that your account meets the requirements to sign in to Teams. |
| [Teams Presence Based on Calendar Events](https://testconnectivity.microsoft.com/tests/TeamsCalendarPresence/input)	| This test verifies that Teams presence can be updated based on calendar events set in Outlook. |
| [Teams Meeting Recording](https://testconnectivity.microsoft.com/tests/TeamsRecording/input)	| This test verifies that your account meets all requirements to record a meeting in Teams. |
| [Teams Calendar Tab](https://testconnectivity.microsoft.com/tests/TeamsCalendarMissing/input)	| This test verifies that the Teams backend service can connect to an Exchange mailbox. |
| [Teams Exchange Integration](https://testconnectivity.microsoft.com/tests/TeamsExchangeIntegration/input)	| This test validates Teams ability to interact with Exchange. For Exchange Hybrid run the test twice using a Microsoft 365 mailbox and an on-premises mailbox. This is useful for IT administrators who want to troubleshoot Teams and Exchange integration. |
| [Teams Channel Meeting](https://testconnectivity.microsoft.com/tests/TeamsChannelMeeting/input)	| This test verifies that your account meets the requirements to schedule a channel meeting. If your mailbox is hosted on-premises is also verifies if your Exchange on-premises inbound receive connector is properly configured. |
| [Teams PSTN Calling Dial Pad](https://testconnectivity.microsoft.com/tests/TeamsDialpadMissing/input)	| This test verifies that your account meets the requirements to display a dial pad in the Teams desktop client and can make and receive Public Switch Telephone Network (PSTN) calls. |
| [Teams Meeting Delegation](https://testconnectivity.microsoft.com/tests/TeamsMeetingDelegation/input)	| This test verifies that your account meets the requirements to schedule a Teams Meeting on behalf of a delegator. |
| [Teams Voicemail](https://testconnectivity.microsoft.com/tests/TeamsVoicemail/input)	| This test verifies that your account meets the requirements to access your voicemail and that the Teams client can retrieve and display voicemail messages. |

