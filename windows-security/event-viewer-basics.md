# Windows Event Viewer Fundamentals

## Objective

Learn how Windows records security, system, and application events using Event Viewer.

## Environment

- Operating System: Windows 10
- Virtual Machine: Windows SOC-Lab
- Tool: Event Viewer

## Logs Explored

### Security Log

Purpose:
Records authentication events, account activity, privilege usage, and other security-related actions.

Reason for Analysis:
Security logs provide evidence during security investigations and threat hunting activities.

## Event Investigation

### Event ID 4624 - Successful Logon

Purpose:
Records successful authentication events.

Initial Findings:
- Log Name: Security
- Event ID: 4624
- Task Category: Logon
- Computer Name: DESKTOP-GE2MMDT

Why It Matters:
Successful authentication events help analysts determine who accessed a system and when access occurred.

## Event Investigation 1

### Event ID 4624 - Successful Logon

#### Details

- Event ID: 4624
- Log Name: Security
- Task Category: Logon
- Computer Name: DESKTOP-GE2MMDT
- Account Name: SYSTEM
- Account Domain: NT AUTHORITY
- Logon Type: 5
- Process Name: C:\Windows\System32\services.exe

#### Analysis

This event represents a successful service logon performed by the built-in SYSTEM account.

The process responsible for the logon was services.exe, which is used by Windows to manage system services.

The activity appears legitimate because SYSTEM is a trusted Windows account and service logons are common during normal operating system operations.

## Observation

When logged in as the standard user account (labuser), Event Viewer was unable to access the Windows Security log.

Error:
"Access is denied (5)"

Analysis:
Access to Security logs requires elevated privileges. Standard user accounts have restricted access to sensitive security information.

Security Relevance:
Limiting Security log access helps protect audit information from unauthorized users.

#### Conclusion

No suspicious activity was identified. The event appears to be normal Windows service activity.
