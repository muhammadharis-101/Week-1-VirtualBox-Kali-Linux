# Week 1: Troubleshooting and Problem Resolution

This document describes the technical issues encountered during the VirtualBox and Kali Linux lab setup and the steps taken to troubleshoot them.

## Issue 1: IP Address Conflict

**Problem:**

Kali Linux failed to activate its network connection after configuring the static IP address `10.0.0.2`.

**Cause:**

The VirtualBox CyberLab DHCP server was already using the same IP address, resulting in an IP address conflict.

**Troubleshooting:**

* Checked the Kali Linux network connection.
* Reviewed NetworkManager logs.
* Identified that the IP address was already in use.
* Inspected the VirtualBox DHCP server configuration.

**Solution:**

Removed the conflicting DHCP server configuration from the CyberLab NAT Network.

**Result:**

Kali Linux successfully activated its network connection using the static IP address `10.0.0.2/24`.

## Issue 2: VirtualBox Drag-and-Drop Failure

**Problem:**

Drag-and-drop functionality between the Windows host and Kali Linux guest was unsuccessful.

**Error Message:**

`VERR_TIMEOUT`

**Troubleshooting:**

* Checked VirtualBox shared clipboard and drag-and-drop settings.
* Configured both features as Bidirectional.
* Installed the available VirtualBox Guest Additions packages.
* Checked VBoxClient processes.

**Alternative Solution:**

Configured a VirtualBox shared folder between Windows and Kali Linux.

**Result:**

File transfer between Windows and Kali Linux worked successfully through the shared folder.

**Status:** Drag-and-drop functionality remains unresolved. Shared folder integration is working.

## Conclusion

The troubleshooting process helped identify and resolve a network configuration conflict and establish an alternative file-sharing method. These experiences improved practical understanding of Linux networking, virtualization, and technical problem-solving.
