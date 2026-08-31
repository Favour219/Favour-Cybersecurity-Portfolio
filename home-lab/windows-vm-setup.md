# Windows VM Setup

## Objective

Create a secure Windows virtual machine for SOC analyst training and security monitoring.

## Host System

- Host OS: Windows
- Virtualization Software: Oracle VirtualBox

## Guest System

- Operating System: Windows 10
- VM Name: Windows SOC-Lab

## User Accounts

### Administrator Account

- Username: FAVOUR
- Account Type: Administrator

### Standard User Account

- Username: labuser
- Account Type: Standard User

## Security Configuration

### Microsoft Defender

Status: Enabled

Evidence:
- No current threats detected
- Virus & Threat Protection active

### Windows Firewall

Status: Enabled

Evidence:
- Domain network firewall enabled
- Private network firewall enabled
- Public network firewall enabled

Purpose:
Provides host-based network protection and generates useful security events for monitoring and investigations.

### Windows Updates

Status: Pending

## Snapshot

Status: Pending

Snapshot Name:
Clean-Windows-Baseline

## Lessons Learned

Creating separate administrator and standard user accounts helps simulate real-world environments and provides useful log data for future investigations.
