# 🖥️ Azure File Server Virtual Machine Deployment

This document describes the deployment of a **Windows Server Virtual Machine in Microsoft Azure** used as a File Server within the lab environment.

The objective is to deploy a dedicated server that will host shared folders and simulate centralized storage used in enterprise infrastructures.

---

# 🎯 Objectives

- Deploy a second Windows Server VM in Azure
- Place the server in the correct Virtual Network
- Connect the server to the Servers subnet
- Prepare the machine for File Server configuration

---

# 🛠️ Virtual Machine Deployment

A new virtual machine was deployed using the Azure Portal.

Configuration used:

| Setting | Value |
|------|------|
Virtual Machine Name | `AZ-FILE01`
Resource Group | `RG-AD-LAB`
Region | `West Europe`
Image | Windows Server 2022 Datacenter
Size | Standard B1s
Administrator Account | `azureadmin`

📸 Screenshots:

- `screenshots/deploy-file-server/01-vm-configuration.png`

---

# 🌐 Networking Configuration

The virtual machine was connected to the existing Azure network infrastructure.

Configuration:

Virtual Network:


AZ-DC01-vnet


Subnet:


Subnet-Servers


This ensures that all infrastructure servers remain in the same secure subnet.

📸 Screenshot:

- `screenshots/deploy-file-server/02-networking-settings.png`

---

# 🖥️ Virtual Machine Deployment Validation

After deployment, the VM was verified in the Azure portal.

The infrastructure now contains two servers.

📸 Screenshot:

- `screenshots/deploy-file-server/03-azure-vm-list.png`

---

# 🏗️ Infrastructure Architecture

The Azure infrastructure now contains multiple servers.


Microsoft Azure
│
└── AZ-DC01-vnet
    │
    └── Subnet-Servers
        │
        ├── AZ-DC01
        └── Domain Controller
            │
            └── AZ-FILE01
                └── File Server


---

# ✔ Status

✔ Azure Virtual Machine deployed  
✔ Connected to Subnet-Servers  
✔ Infrastructure expanded with File Server VM