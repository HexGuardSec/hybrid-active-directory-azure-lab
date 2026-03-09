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
- Understand **Azure infrastructure fundamentals**
- Implement **secure identity management**
- Prepare the environment for **Hybrid Identity integration**
- Automate administrative tasks using **PowerShell**
- Document real-world troubleshooting scenarios

---

## 🏗️ Lab Environment

### On-Premise Infrastructure

- Hypervisor: VMware Workstation
- Server OS: Windows Server 2022 (Domain Controller)
- Client OS: Windows 11 (Domain Joined)
- Network: Internal LAN
- Domain: `corp.local`

### Azure Cloud Infrastructure

- Platform: Microsoft Azure
- Resource Group: `RG-AD-LAB`
- Virtual Machine: `AZ-DC01`
- Operating System: Windows Server 2022
- Region: West Europe
- Remote Management: RDP

---

## ☁️ Azure Infrastructure Architecture

```

Microsoft Azure
│
└── Resource Group (RG-AD-LAB)
│
└── Virtual Machine (AZ-DC01)
│
├── Virtual Network
├── Subnet
├── Public IP
└── Network Security Group

```

This infrastructure provides a basic cloud compute environment used to simulate enterprise workloads.

---

## 🧩 Hybrid Infrastructure Vision

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

## 🗂️ Repository Structure

```

hybrid-active-directory-azure-lab
│
├── windows-server-setup/
├── active-directory-setup/
├── group-policy-setup/
├── azure-fundamentals/
├── scripts/
├── troubleshooting/
└── notes/

```

Each section documents a different part of the infrastructure configuration.

---

## ⚙️ Automation

PowerShell scripts are used to automate several administrative tasks:

- User creation
- Bulk account import
- Account management
- Administrative automation

Scripts are located in the `/scripts` directory.

---

## 🧪 Troubleshooting Scenarios

This repository documents real-world issues encountered during the lab such as:

- DNS resolution problems
- Group Policy deployment failures
- Azure VM connectivity issues
- Active Directory configuration errors
- Authentication troubleshooting

Each scenario includes diagnostic steps and solutions.

---

## 🧠 Skills Demonstrated

- Windows Server installation & configuration
- Active Directory architecture design
- Organizational Unit structuring
- AGDLP permission model
- NTFS permission management
- Group Policy configuration
- PowerShell automation
- Microsoft Azure infrastructure deployment
- Cloud resource management
- Hybrid identity concepts
- Infrastructure troubleshooting

---

## 🎯 Target Role

This project demonstrates practical skills aligned with roles such as:

- Junior System Administrator
- IT Infrastructure Engineer
- Cloud Support Engineer
- Internal IT Support
- Data Center Technician

The focus is on **enterprise-style infrastructure implementation and documentation**.

---

## 📌 Project Status

🔧 In Progress – The lab will continue evolving with additional Azure services, hybrid identity configuration, and automation improvements.

---

## 📘 Purpose of This Repository

This repository serves as:

- A **hands-on enterprise infrastructure simulation**
- A **technical documentation portfolio**
- A demonstration of **real-world Windows and Azure administration practices**
- A structured learning progression toward **professional infrastructure roles**
```