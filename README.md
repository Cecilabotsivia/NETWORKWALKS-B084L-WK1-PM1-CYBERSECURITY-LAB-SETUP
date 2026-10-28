# NETWORKWALKS-B084L-WK1-PM1-CYBERSECURITY-LAB-SETUP
Cybersecurity Lab Setup
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20Version 7.2.22 r175245 (Qt6.8.0 on windows)-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Cecil%20Abotsivia%20Yao-C00000?style=flat-square" />
</p>

# WK1-PM1: VirtualBox and Kali Linux Lab Setup

![Platform](https://img.shields.io/badge/Platform-Windows%2011-blue)
![Virtualization](https://img.shields.io/badge/Virtualization-VirtualBox-orange)
![Operating System](https://img.shields.io/badge/VM-Kali%20Linux-557C94)

## 1. Project Overview

This project documents the setup and configuration of a Kali Linux virtual machine using Oracle VirtualBox as part of the Week 1 project module.

The lab provides a virtual environment for learning cybersecurity concepts and performing authorized lab exercises.

## 2. Objectives

- Set up Kali Linux in Oracle VirtualBox.
- Configure a VirtualBox NAT Network.
- Assign a static IPv4 address to Kali Linux.
- Verify internet connectivity.
- Configure Shared Clipboard and Drag'n'Drop.
- Configure and test a shared folder between Windows and Kali Linux.
- Create a virtual machine snapshot.

## 3. Lab Environment

| Component | Configuration |
|---|---|
| Host operating system | Windows 11 Pro |
| Virtualization software | Oracle VirtualBox |
| Virtual machine | Kali Linux 2026.3 |
| Allocated RAM | 2048 MB (2 GB) |
| Allocated CPUs | 2 |
| NAT Network name | `NatNetwork` |
| Network subnet | `10.0.0.0/24` |

## 4. Network Configuration

The Kali Linux network interface was configured with the following IPv4 settings.

| Setting | Value |
|---|---|
| Network interface | `eth0` |
| IPv4 address | `10.0.0.2/24` |
| Default gateway | `10.0.0.1` |
| DNS servers | `10.0.0.1`, `8.8.8.8` |
| Network mode | NAT Network |

### Internet Connectivity Test

The following command was used to test internet connectivity from Kali Linux:

```bash
ping -c 4 google.com
```

**Observed result:** Four replies were received with 0% packet loss.

## 5. Shared Folder Configuration

A shared folder was configured to allow file exchange between the Windows host and Kali Linux virtual machine.

The test file `kali-test.txt` was created from Kali Linux in the shared-folder mount. The file was then checked on the Windows host.

## 6. VirtualBox Integration

The following integration settings were configured:

- Shared Clipboard: Bidirectional
- Drag'n'Drop: Bidirectional

These settings allow clipboard sharing and drag-and-drop between the host and guest systems.

## 7. Screenshots and Evidence

The following evidence documents the setup and testing process.

| Evidence | Screenshot |
|---|---|
| Importing Kali into VirtualBox | `02-Import-kali-virtualbox.png` |
| NAT Network configuration | `01-NAT-Network.png` |
| Kali Linux system details | `3-kali-linux.png` |
| Shared folder test | `04-Shared-Folder-Test.png` |
| Virtual machine snapshot | `05-Snapshot.png` |
| Clipboard and Drag'n'Drop settings | `06-Clipboard-DragDrop.png` |
| Kali command (2026 version) | `07-Kali-command-2026version.png` |
| Oracle VirtualBox setup | `Oracle-setup.png` |

## 8. Challenges and Resolution

During the initial setup, hardware virtualization was unavailable to VirtualBox. Intel virtualization support was enabled in the computer's BIOS settings, after which the Kali Linux virtual machine was able to boot.

The Kali Linux network interface was subsequently configured with a static IPv4 address and internet connectivity was verified.

## 9. Conclusion

The Kali Linux virtual machine was configured in Oracle VirtualBox with a static IP address on the specified NAT Network. Internet connectivity was tested successfully, and the shared-folder and VirtualBox integration features were checked.

This repository records the configuration and evidence for the Week 1 lab setup.

## 10. Project Scope

This README documents the lab setup and verification activities. Any additional virtual machines or inter-machine connectivity tests described as optional future tasks in the project brief are outside the scope of this report unless separately completed and documented.
