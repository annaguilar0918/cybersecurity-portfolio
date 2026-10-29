# Project 02 — Cybersecurity Home Lab Foundation

**Project Status:** Phase 1 — Infrastructure Assessment

**Focus Areas:** IT Support, Hardware Assessment, Networking, Linux, Windows Administration, and Virtualization Planning

## 1. Project Overview

This project establishes the foundation of a personal cybersecurity home lab designed to develop practical skills in IT support, systems administration, networking, and security operations.

Before deploying virtual servers and security tools, I performed an initial assessment of the existing network infrastructure and available computing resources.

The objective was to understand the capabilities and limitations of the environment, identify opportunities for reuse, and plan future lab deployments without unnecessary hardware purchases.

## 2. Objectives

- Identify existing network infrastructure and connected lab computers.
- Inventory hardware and operating system specifications.
- Assess virtualization readiness and available storage.
- Document network interfaces and connectivity.
- Establish a repeatable approach to technical documentation.
- Identify potential constraints before deploying lab services.

## 3. Lab Environment

The environment consists of four computers running Windows 11 and Ubuntu Linux.

| Device | Processor | Memory | Operating System |
|---|---|---|---|
| Primary workstation | Intel Core Ultra 9 285 | 32 GB | Windows 11 Pro |
| Linux lab laptop | Intel Core i7-7700HQ | Approximately 14 GiB usable | Ubuntu Linux |
| Secondary Windows laptop | Intel Core i5-1135G7 | 8 GB | Windows 11 Pro |
| Additional Windows laptop | Intel Core i5-10210U | 16 GB | Windows 11 |

The primary workstation uses NVMe storage and supports hardware virtualization. The Linux laptop has both SSD and HDD storage, allowing different workload and storage configurations to be evaluated.

## 4. Network Assessment

The initial network inventory identified:

- An existing router providing local network connectivity.
- Four lab computers connected through Wi-Fi.
- Available wired Ethernet interfaces on selected devices.
- Virtual network interfaces associated with virtualization and VPN software.
- A need to evaluate wired connectivity and future network segmentation.

Private addressing, device identifiers, and router administration details are intentionally excluded from this public documentation.

## 5. Tools and Commands

### Windows — Hardware and Network Inventory

```powershell
Get-ComputerInfo
Get-NetAdapter
Get-PhysicalDisk
Get-Volume
```

These commands help identify system information, network interfaces, physical storage devices, and disk volumes.

### Linux — Hardware and Network Inventory

```bash
lscpu
free -h
lsblk
df -hT
nmcli device status
sudo lshw -class network -short
```

These commands provide information about CPU capabilities, memory, storage, mounted filesystems, network connections, and network hardware.

## 6. Validation and Findings

The initial inventory confirmed:

- Four available computers for lab activities.
- Hardware virtualization capabilities suitable for further evaluation.
- Available SSD storage for virtual machines and lab files.
- Existing wireless connectivity across the lab computers.
- A mix of Windows and Linux systems for cross-platform administration practice.

The assessment also identified storage cleanup, remote access configuration, and additional network connectivity testing as future maintenance activities.

## 7. Troubleshooting and Observations

During the inventory, I distinguished physical network interfaces from virtual adapters created by VPN and virtualization software.

I also examined the difference between installed memory and memory available to the operating system, and between physical disk capacity and available filesystem space.

These checks helped prevent incorrect assumptions about system capabilities and resource availability.

## 8. Lessons Learned

This project reinforced the importance of completing a hardware and network inventory before designing an IT environment.

Key lessons included:

- Confirm system specifications using operating system tools rather than assumptions.
- Evaluate available resources before assigning virtual machine workloads.
- Distinguish network link status from actual connectivity and performance.
- Protect sensitive configuration details when publishing technical documentation.
- Record findings and verification results so future troubleshooting can be performed systematically.

## 9. Next Steps

- Complete the remaining infrastructure inventory.
- Create a sanitized network topology diagram.
- Develop a virtualization deployment plan.
- Establish baseline system and network configurations.
- Begin documenting practical administration and troubleshooting scenarios.

---

**Documentation Note:** This project reflects completed inventory work. Planned deployments and security implementations will be documented separately after configuration and testing.
