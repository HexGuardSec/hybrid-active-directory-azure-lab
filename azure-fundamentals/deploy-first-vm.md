# ☁️ Azure Virtual Machine Deployment

This document describes the deployment of a **Windows Server 2022 Virtual Machine in Microsoft Azure** as part of the cloud infrastructure lab.

The goal is to create a basic compute resource in Azure and validate connectivity and network configuration.

---

# 🎯 Objectives

* Create an Azure Resource Group
* Deploy a Windows Server Virtual Machine
* Configure administrative access
* Validate connectivity via Remote Desktop (RDP)
* Verify network configuration inside the VM

---

# 🗂️ Resource Group Creation

A **Resource Group** was created to organize and manage Azure resources used in this lab.

Configuration:

* Resource Group Name: `RG-AD-LAB`
* Region: `West Europe`

📸 Screenshots:

* `screenshots/deploy-first-vm/01-azure-virtual-machines.png`

The resource group acts as a logical container for all infrastructure components deployed during the lab.

---

# 🖥️ Virtual Machine Deployment

A Windows Server virtual machine was deployed using the Azure Portal.

Configuration used:

* Virtual Machine Name: `AZ-DC01`
* Operating System: `Windows Server 2022 Datacenter`
* Region: `West Europe`
* VM Size: `Standard D2als v7`
* Administrator Account: `azureadmin`

📸 Screenshots:

* `screenshots/deploy-first-vm/02-vm-overview.png`

During deployment, Azure automatically created several networking resources required for connectivity.

---

# 🌐 Networking Configuration

Azure automatically provisioned the following components:

* Virtual Network
* Subnet
* Public IP Address
* Network Security Group (NSG)

These components allow secure access to the virtual machine.

📸 Screenshots:

* `screenshots/deploy-first-vm/03-vm-networking.png`

---

# 🔑 Remote Access (RDP)

The server was accessed remotely using **Remote Desktop Protocol (RDP)** through the Azure portal.

Connection method:

```text
Azure Portal
→ Virtual Machine
→ Connect
→ RDP
```

Login credentials:

```
Username: azureadmin
Password: <configured during deployment>
```

📸 Screenshots:

* `screenshots/deploy-first-vm/04-rdp-connection.png`

---

# 🧪 Network Verification

After connecting to the server, network configuration was verified using the following command:

```powershell
ipconfig
```

The virtual machine received a private IP address from the Azure Virtual Network.

Example:

```
10.x.x.x
```

This confirms the VM is properly connected to the Azure virtual network.

📸 Screenshots:

* `screenshots/deploy-first-vm/05-windows-server-desktop.png`
* `screenshots/deploy-first-vm/06-ipconfig-check.png`

---

# ✔ Status

✔ Azure Resource Group created
✔ Windows Server VM deployed
✔ Networking resources provisioned automatically
✔ RDP access validated
✔ Network configuration verified
