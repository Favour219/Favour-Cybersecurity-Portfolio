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
