---
title: Reset MFA
description: Remove all App- and Mobilephone auth methods for a user
---

## Description
Removes authenticator app and phone-based authentication methods for a user. This forces the user to re-enroll MFA methods after the reset. Optionally a notification email can be sent to the user informing them that their MFA methods have been reset through this runbook.

## Location
User → Security → Reset MFA

## Permissions
### Application permissions
- **Type**: Microsoft Graph
  - UserAuthenticationMethod.ReadWrite.All
  - Mail.Send


## Parameters
### UserName

User principal name of the target user.

| Property | Value |
| --- | --- |
| Required | true |
| Default Value |  |
| Type | String |

### NotifyUser

When enabled, sends a notification email to the target user informing them that their MFA methods were reset by an administrator. Default is disabled.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value | False |
| Type | Boolean |

### EmailFrom

Sender email address for the optional notification mail. Sourced from the RealmJoin tenant setting RJReport.EmailSender.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value |  |
| Type | String |

### ServiceDeskDisplayName

Service Desk display name for user contact information (optional). Sourced from the RealmJoin tenant setting RJReport.ServiceDesk_DisplayName.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value |  |
| Type | String |

### ServiceDeskEmail

Service Desk email address for user contact information (optional). Sourced from the RealmJoin tenant setting RJReport.ServiceDesk_EMail.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value |  |
| Type | String |

### ServiceDeskPhone

Service Desk phone number for user contact information (optional). Sourced from the RealmJoin tenant setting RJReport.ServiceDesk_Phone.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value |  |
| Type | String |

### LanguageOverride

Overrides the language used for the notification email. Accepted values are 'DE' (German) or 'EN' (English). If left empty, the language is determined automatically based on the target user's usage location.

| Property | Value |
| --- | --- |
| Required | false |
| Default Value |  |
| Type | String |



[Back to Runbook Reference overview](../../README.md)

