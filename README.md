# ☁️ Hybrid Active Directory & Azure Enterprise Lab

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Category](https://img.shields.io/badge/Category-Hybrid%20Infrastructure-blue)
![Azure](https://img.shields.io/badge/Azure-Cloud-blue)
![Active Directory](https://img.shields.io/badge/Active%20Directory-Enterprise-darkblue)
![Infrastructure](https://img.shields.io/badge/Infrastructure-IT-lightgrey)
![PowerShell](https://img.shields.io/badge/PowerShell-Automation-blueviolet)

---

## 🏢 Project Overview

This project simulates a **Hybrid Enterprise Infrastructure** combining an on-premise **Windows Server Active Directory environment** with **Microsoft Azure cloud services**.

The objective is to design and implement a structured, secure, and scalable infrastructure environment similar to those used in modern organizations.

This lab focuses on **identity management, infrastructure deployment, cloud integration, automation, and troubleshooting**.

---

## 🎯 Project Goals

- Extend an existing **Active Directory enterprise lab** into the cloud
- Deploy and manage **Azure Virtual Machines**
- Build a secure **Azure network architecture**
- Implement centralized storage using **Windows File Server**
- Prepare the environment for **Hybrid Identity integration**
- Automate administrative tasks using **PowerShell**
- Document real-world troubleshooting scenarios

---

# 🏗️ Lab Environment

## On-Premise Infrastructure

- Hypervisor: VMware Workstation
- Server OS: Windows Server 2022 (Domain Controller)
- Client OS: Windows 11 (Domain Joined)
- Network: Internal LAN
- Domain: `corp.local`

---

## ☁️ Azure Cloud Infrastructure

- Platform: Microsoft Azure
- Resource Group: `RG-AD-LAB`
- Virtual Network: `AZ-DC01-vnet`
- Subnet: `Subnet-Servers`
- Network Security Group: `NSG-Servers`

### Azure Virtual Machines

| Server | Role             |
|--------|------------------|
AZ-DC01  | Domain Controller
AZ-FILE01| File Server

Region: **West Europe**

---

# ☁️ Azure Infrastructure Architecture

```

Microsoft Azure
│
└── Resource Group (RG-AD-LAB)
    │
    └── AZ-DC01-vnet
        │
        └── Subnet-Servers
        │
        ├── AZ-DC01
        │      
        └── Domain Controller
            │
            └── AZ-FILE01
                └── File Server

```

This infrastructure simulates a **basic enterprise cloud environment with centralized identity and storage services**.

---

# 🧩 Hybrid Infrastructure Vision

Modern enterprise environments rarely rely only on on-premise infrastructure.

The long-term objective of this lab is to implement a **Hybrid Identity architecture** combining on-premise and cloud identity services.

```

On-Prem Active Directory
│
│ Directory Synchronization
▼
Microsoft Entra ID (Azure AD)
│
▼
Azure Cloud Resources

```

This architecture reflects how most companies manage identity across on-premise and cloud environments.

---

# 🗂️ Repository Structure

```

hybrid-active-directory-azure-lab
│
├── azure-fundamentals
│     ├── deploy-first-vm.md
│     ├── create-virtual-network.md
│     ├── network-security-group.md
│     ├── deploy-file-server-vm.md
│     └── file-server-setup.md
│
└── screenshots

```

Each section documents a different part of the Azure infrastructure deployment.

---

# ⚙️ Automation

PowerShell scripts will be used to automate several administrative tasks including:

- User creation
- Bulk account provisioning
- Infrastructure management
- Administrative automation

Scripts will be organized in the `/scripts` directory.

---

# 🧪 Troubleshooting Scenarios

This repository documents real-world issues encountered during the lab such as:

- Azure VM connectivity issues
- DNS resolution problems
- Network security misconfigurations
- File share access issues
- Authentication troubleshooting

Each scenario includes diagnostic steps and solutions.

---

# 🧠 Skills Demonstrated

- Windows Server administration
- Active Directory infrastructure
- Azure Virtual Machine deployment
- Azure Virtual Network configuration
- Network Security Groups (NSG)
- File Server configuration
- SMB share management
- Infrastructure documentation
- Cloud infrastructure basics
- Hybrid identity concepts

---

# 🎯 Target Role

This project demonstrates practical skills aligned with roles such as:

- Junior System Administrator
- IT Infrastructure Engineer
- Cloud Support Engineer
- Internal IT Support
- Data Center Technician

The focus is on **enterprise-style infrastructure implementation and documentation**.

---

# 📌 Project Status

🔧 In Progress – The lab continues evolving with additional Azure services, hybrid identity configuration, and automation improvements.

---

# 📘 Purpose of This Repository

This repository serves as:

- A **hands-on enterprise infrastructure simulation**
- A **technical documentation portfolio**
- A demonstration of **real-world Windows and Azure administration practices**
- A structured learning progression toward **professional infrastructure roles**