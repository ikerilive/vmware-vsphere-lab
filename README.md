# VMware vSphere Hands-On Lab (ESXi & vCenter)

## Overview
This repository documents my hands-on experience building and administering a complete **VMware vSphere lab environment**.  
The goal of this project was to gain real-world skills in **ESXi, vCenter Server Appliance (VCSA), VM lifecycle management, HA, DRS, and troubleshooting**, aligned with enterprise VMware environments.

This is not a theoretical project — every step was implemented, tested, and validated in a working lab.

---

## Technologies Used
- VMware ESXi 6.5 / 6.7
- VMware vCenter Server Appliance (VCSA)
- VMware vSphere Client (HTML5)
- VMware Workstation Pro
- Windows 11 (Installer & DNS)
- Linux (Ubuntu)
- Windows Server (VM)
- NFS Storage (for HA)
- vMotion, HA, DRS

---

## Lab Architecture

**Host Machine**
- Windows 11
- VMware Workstation Pro

**Virtual Infrastructure**
- ESXi Host 1
- ESXi Host 2
- vCenter Server Appliance
- Shared NFS datastore
- Multiple Linux & Windows VMs

---

## Network Design

| Component | IP Address |
|---------|------------|
| ESXi Host 1 | 192.168.47.125 |
| ESXi Host 2 | 192.168.47.131 |
| vCenter Server | 192.168.47.133 |
| Gateway | 192.168.47.2 |
| DNS Server | 192.168.47.2 |

> Static IP addressing was used to simulate an enterprise environment.

---

## Project Sections

---

## 1️⃣ ESXi Installation & Configuration

### Tasks Performed
- Installed ESXi using VMware-VMvisor installer ISO
- Configured:
  - Management network
  - Static IP
  - DNS
  - Hostname
- Verified datastore creation
- Enabled SSH & ESXi Shell

![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/01-esxi-installation/Screenshot%202025-12-22%20130558.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/01-esxi-installation/Screenshot%202025-12-22%20130812.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/01-esxi-installation/Screenshot%202025-12-22%20130849.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/01-esxi-installation/Screenshot%202025-12-22%20130928.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/01-esxi-installation/Screenshot%202025-12-22%20130940.png)




## 2️⃣ Virtual Machine Creation & Management

### Tasks Performed
- Created Linux and Windows virtual machines
- Installed guest operating systems
- Installed VMware Tools
- Modified VM resources (CPU/RAM)
- Took and reverted snapshots


![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/02-vm-management/Screenshot%202025-12-22%20132415.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/02-vm-management/Screenshot%202025-12-22%20132432.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/02-vm-management/Screenshot%202025-12-22%20132450.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/02-vm-management/Screenshot%202025-12-22%20132534.png)


## 3️⃣ vCenter Server Appliance (VCSA) Deployment

### Tasks Performed
- Deployed VCSA using OVA installer
- Configured:
  - FQDN
  - Static IP
  - DNS
  - NTP
- Verified vCenter services
- Accessed vSphere Client (HTML5)
