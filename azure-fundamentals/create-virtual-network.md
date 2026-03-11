# 🌐 Azure Virtual Network Configuration

This document describes the creation and configuration of the **Virtual Network used in the Azure lab environment**.

The objective is to build a basic network architecture that will host future cloud resources such as servers and services.

---

# 🎯 Objectives

- Understand Azure Virtual Network architecture
- Create a Virtual Network
- Configure the address space
- Create dedicated subnets
- Prepare the network for enterprise-style infrastructure

---

# 🛠️ Virtual Network Creation

A Virtual Network was created in Microsoft Azure to host infrastructure resources.

Configuration used:

- Virtual Network Name: `AZ-DC01-vnet`
- Resource Group: `RG-AD-LAB`
- Region: `West Europe`

📸 Screenshots:

- `screenshots/create-virtual-network/01-vnet-overview.png`

This network provides the internal connectivity layer for the virtual machines deployed in the Azure environment.

---

# 🌍 Address Space Configuration

The Virtual Network was configured with the following address space:


10.0.0.0/16


This range provides a large private IP pool that can be segmented into multiple subnets.

📸 Screenshot:

- `screenshots/create-virtual-network/02-address-space.png`

Using a `/16` network allows the infrastructure to scale while maintaining proper segmentation.

---

# 🧩 Subnet Configuration

To organize infrastructure resources properly, a dedicated subnet for servers was created.

### Subnet Configuration

- Subnet Name: `Subnet-Servers`
- Address Range: `10.0.1.0/24`

This subnet will host infrastructure components such as:

- Domain Controllers
- File Servers
- Future infrastructure services

📸 Screenshot:

- `screenshots/create-virtual-network/03-subnets.png`

---

# 🏗️ Network Architecture

The resulting network architecture is structured as follows:


Microsoft Azure
│
└── AZ-DC01-vnet
│
├── default subnet
│
└── Subnet-Servers


This structure allows separation of infrastructure components and prepares the environment for more advanced networking configurations.

---

# ✔ Status

✔ Virtual Network created  
✔ Address space configured  
✔ Subnet created  
✔ Infrastructure network ready