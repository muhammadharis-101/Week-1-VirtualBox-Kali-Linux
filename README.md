# Week-1-VirtualBox-Kali-Linux
Week 1 Cybersecurity Internship - VirtualBox and Kali Linux Lab Setup

# Week 1: VirtualBox and Kali Linux Lab Setup

**Cybersecurity Internship — Practical Lab**

## Project Overview

This project documents the setup and configuration of a virtual cybersecurity lab using Oracle VirtualBox and Kali Linux. The objective was to establish a working Linux environment, configure network connectivity, assign a static IP address, and enable file sharing between the Windows host and Kali Linux virtual machine.

## Tools and Technologies

* Oracle VirtualBox 7.2.22
* Kali Linux 2026.3
* Windows Host Operating System
* Linux Terminal
* NetworkManager
* VirtualBox Guest Additions

## Virtual Machine Configuration

| Component               | Configuration     |
| ----------------------- | ----------------- |
| Virtualization Software | Oracle VirtualBox |
| Guest Operating System  | Kali Linux 2026.3 |
| RAM                     | 2 GB              |
| CPU                     | 2 Processors      |
| Virtual Disk            | 80 GB             |
| Network Mode            | NAT Network       |
| Network Name            | CyberLab          |

## Network Configuration

A NAT Network named `CyberLab` was created in VirtualBox.

The Kali Linux virtual machine was configured with the following static network settings:

| Setting         | Value       |
| --------------- | ----------- |
| IP Address      | 10.0.0.2/24 |
| Default Gateway | 10.0.0.1    |
| DNS Server      | 8.8.8.8     |
| Secondary DNS   | 1.1.1.1     |
| Network         | 10.0.0.0/24 |

## Practical Tasks Completed

1. Installed Oracle VirtualBox.
2. Downloaded and extracted the Kali Linux 2026.3 VirtualBox image.
3. Verified the downloaded image using SHA-256 checksum.
4. Imported and configured the Kali Linux virtual machine.
5. Created a NAT Network named CyberLab.
6. Configured a static IP address in Kali Linux.
7. Tested connectivity with the default gateway.
8. Verified internet connectivity.
9. Tested DNS resolution.
10. Installed the available VirtualBox Guest Additions packages.
11. Configured shared clipboard and drag-and-drop settings.
12. Created a shared folder between Windows and Kali Linux.
13. Successfully tested file transfer between both systems.

## Network Connectivity Testing

The following commands were used to verify the network configuration:

```bash
ip -br addr
ip route
ping -c 4 10.0.0.1
ping -c 4 1.1.1.1
ping -c 4 google.com
```

**Results:**

* Static IP configuration: Successful
* Gateway connectivity: Successful
* Internet connectivity: Successful
* DNS resolution: Successful

## Shared Folder Configuration

A shared folder was configured to exchange files between Windows and Kali Linux.

| Component              | Path                |
| ---------------------- | ------------------- |
| Windows Shared Folder  | C:\downloads        |
| Kali Linux Mount Point | /media/sf_downloads |

Two-way file transfer was successfully tested using the shared folder.

## Troubleshooting

During the setup, two main issues were encountered:

1. IP address conflict between the VirtualBox DHCP server and Kali Linux static IP.
2. VirtualBox drag-and-drop functionality returned a VERR_TIMEOUT error.

The DHCP conflict was resolved by removing the conflicting CyberLab DHCP server. For file transfer, the shared folder feature was configured successfully as an alternative to drag-and-drop.

Detailed troubleshooting information is available in the `Troubleshooting/Issues.md` file.

## Learning Outcomes

Through this practical exercise, I gained hands-on experience with:

* Virtual machine creation and configuration.
* Linux network configuration.
* Static IP addressing and DNS.
* Network connectivity troubleshooting.
* VirtualBox Guest Additions.
* Shared folder configuration and file transfer.

## Project Status

**Completed:** Kali Linux virtual lab setup, static network configuration, connectivity testing, and shared folder integration.

**Pending:** Resolving the VirtualBox drag-and-drop issue.

---

**Author:** Muhammad Haris
**Project:** Cybersecurity Internship — Week 1
