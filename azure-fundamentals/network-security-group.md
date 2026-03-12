# 🔒 Azure Network Security Group Configuration

This document describes the creation and configuration of a **Network Security Group (NSG)** used to secure the Azure network infrastructure.

The objective is to control inbound traffic and protect the subnet hosting infrastructure servers.

---

# 🎯 Objectives

- Understand the role of Network Security Groups in Azure
- Create a Network Security Group
- Associate the NSG with a subnet
- Review default inbound security rules
- Implement basic network security controls

---

# 🛠️ Network Security Group Creation

A Network Security Group was created to manage inbound and outbound traffic rules for the server subnet.

Configuration used:

- Network Security Group Name: `NSG-Servers`
- Resource Group: `RG-AD-LAB`
- Region: `West Europe`

📸 Screenshots:

- `screenshots/network-security-group/01-nsg-overview.png`

The NSG acts as a **network-level firewall controlling traffic to Azure resources**.

---

# 🔗 Subnet Association

The Network Security Group was associated with the subnet hosting infrastructure servers.

Configuration:

- Virtual Network: `AZ-DC01-vnet`
- Subnet: `Subnet-Servers`

Associating an NSG with a subnet ensures that all resources within the subnet are protected by the defined security rules.

📸 Screenshot:

- `screenshots/network-security-group/02-subnet-association.png`

---

# 🔐 Default Security Rules

Azure automatically creates several default security rules when an NSG is deployed.

### Default inbound rules

| Rule | Priority | Action |
|-----|------|------|
AllowVnetInBound | 65000 | Allow |
AllowAzureLoadBalancerInBound | 65001 | Allow |
DenyAllInbound | 65500 | Deny |

These rules allow internal Azure traffic while blocking all other inbound connections by default.

📸 Screenshot:

- `screenshots/network-security-group/03-inbound-rules.png`

---

# 🏗️ Network Security Architecture

The infrastructure network now follows this structure:


Microsoft Azure
│
└── AZ-DC01-vnet
    │
    ├── Subnet-Servers
    │
    └── NSG-Servers
        │
        └── default subnet


The Network Security Group protects all resources deployed within the **Subnet-Servers** subnet.

---

# ✔ Status

✔ Network Security Group created  
✔ NSG associated with Subnet-Servers  
✔ Default security rules validated  
✔ Basic network security implemented