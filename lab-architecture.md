# Cybersecurity Home Lab Architecture

## Lab Objective

Build a controlled cybersecurity home lab for practicing security monitoring, log analysis, threat detection, and incident investigation without affecting the host system.

## Host System

- Device: FAVOUR
- Processor: Intel Core i7-8565U @ 1.80 GHz
- RAM: 16 GB (15.3 GB usable)
- System Type: 64-bit operating system, x64-based processor
- Operating System: Windows 11

  ## Hypervisor

- Virtualization Software: Oracle VM VirtualBox
- Purpose: Create and manage virtual machines for the cybersecurity lab

## Guest Virtual Machine

- Guest Operating System: Windows 11
- RAM Allocation: 4 GB
- CPU Allocation: 2 virtual processors
- Virtual Disk: 60 GB
- Purpose: Security monitoring, log analysis, threat detection, and incident investigation

## Network Configuration

- Network Mode: NAT
- Purpose: Provide internet access to the Windows VM while keeping the virtual machine separated from the physical network.

- ## Security Controls

- Use NAT networking for the initial lab configuration.
- Keep the Windows VM separate from the host system.
- Take a clean baseline snapshot before conducting security experiments.
- Avoid storing passwords, credentials, or other sensitive information in the GitHub repository.
- Use the VM for controlled cybersecurity exercises rather than testing on the host system.

## Resource Limitations

- Host RAM: 16 GB
- RAM allocated to Windows VM: 4 GB
- CPU allocated to Windows VM: 2 virtual processors
- Run one major virtual machine at a time to maintain host performance.
- Avoid running resource-intensive applications on the host while the lab is active.

## Lab Architecture Diagram

```text
                    Internet
                       |
                       |
                +--------------+
                | Host Laptop  |
                | Windows 11   |
                | 16 GB RAM    |
                +------+-------+
                       |
                  VirtualBox
                  (Hypervisor)
                       |
                 NAT Network
                       |
                +------+-------+
                | Windows 11   |
                |     VM       |
                | 4 GB RAM     |
                | 2 vCPUs     |
                +------+-------+
                       |
                    Sysmon
                       |
                 Security Data
                       |
                +------+-------+
                | Splunk/Wazuh |
                |     SIEM     |
                +--------------+
```
