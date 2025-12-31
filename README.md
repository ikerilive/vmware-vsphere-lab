# VMware vSphere Hands-On Lab (ESXi & vCenter)

## Overview
This repository documents my hands-on experience building and administering a complete **VMware vSphere lab environment**.  
The goal of this project was to gain real-world skills in **ESXi, vCenter Server Appliance (VCSA), VM lifecycle management, HA, DRS, and troubleshooting**, aligned with enterprise VMware environments.

This is not a theoretical project; every step was implemented, tested, and validated in a working lab.

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

![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/03-vcenter-installation/Screenshot%202025-12-22%20133343.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/03-vcenter-installation/Screenshot%202025-12-22%20133424.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/03-vcenter-installation/Screenshot%202025-12-22%20133642.png)



## 4️⃣ Datacenter & Host Management

### Tasks Performed
- Created Datacenter object
- Added multiple ESXi hosts
- Managed hosts via vCenter
- Assigned licenses
- Verified cluster readiness


![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/04-datacenter-hosts/Screenshot%202025-12-22%20134109.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/04-datacenter-hosts/Screenshot%202025-12-22%20134123.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/04-datacenter-hosts/Screenshot%202025-12-22%20134209.png)
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/04-datacenter-hosts/Screenshot%202025-12-22%20135058.png)



## 5️⃣ vMotion Configuration

### Tasks Performed
- Configured VMkernel adapters for vMotion
- Tested live migration of VMs between hosts
- Verified zero-downtime migration
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/05-vmotion/Screenshot%202025-12-31%20210915.png)

## 6️⃣ High Availability (HA)

### Tasks Performed
- Created shared NFS datastore
- Configured HA cluster
- Simulated host failure
- Verified VM automatic restart

![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/06-ha-07-drs/Screenshot%202025-12-31%20211722.png)
## 7️⃣ Distributed Resource Scheduler (DRS)

### Tasks Performed
- Enabled DRS
- Configured automation level
- Observed workload balancing
- Verified VM migration recommendations
![Lab Architecture](https://github.com/ikerilive/vmware-vsphere-lab/blob/main/06-ha-07-drs/Screenshot%202025-12-31%20212439.png)

## 8️⃣ VM Lifecycle Operations

### Tasks Performed
- VM cloning
- Template creation
- OVF export and import
- Folder organization
- Resource pool management


## 9️⃣ Troubleshooting & CLI

### Tasks Performed
- Used ESXi CLI commands
- Investigated storage issues
- Network troubleshooting
- Reviewed logs for deployment errors



## Key Skills Demonstrated

- Enterprise vSphere architecture
- ESXi installation & administration
- vCenter deployment & management
- HA & DRS configuration
- vMotion & shared storage
- VM lifecycle management
- Real-world troubleshooting

## Outcome

This project demonstrates hands-on experience equivalent to a **junior VMware / Virtualization Administrator role** and reflects real operational workflows used in production environments.
