# 📁 Azure File Server Configuration

This document describes the installation and configuration of a **File Server role on the Azure virtual machine AZ-FILE01**.

The objective is to provide centralized storage accessible through SMB network shares.

---

# 🎯 Objectives

- Install the File Server role
- Create a shared directory
- Configure an SMB share
- Validate network access

---

# 🛠️ File Server Role Installation

The File Server role was installed using **Server Manager**.

Path used:

Server Manager → Add Roles and Features → File and Storage Services → File Server

📸 Screenshot:

- `screenshots/file-server/01-file-server-role-installed.png`

---

# 📂 Shared Folder Creation

A folder structure was created to store shared company data.

Folder path:


C:\Shares\CompanyData


This directory will store shared files accessible by network users.

📸 Screenshot:

- `screenshots/file-server/02-companydata-folder.png`

---

# 🌐 SMB Share Configuration

The folder was shared using SMB.

Share name:


CompanyData


Share path:


C:\Shares\CompanyData


📸 Screenshot:

- `screenshots/file-server/03-companydata-share.png`

---

# 🧪 Share Access Validation

The share was tested using the Run dialog.

Command used:

The share appeared successfully, confirming the SMB configuration works. 

📸 Screenshot: 

- `screenshots/file-server/04-share-access-test.png` 

---

# 🏗️ Infrastructure Architecture 

Microsoft Azure 
│ 
└── AZ-DC01-vnet 
    │ 
    └── Subnet-Servers 
        │ 
        ├── AZ-DC01 
        │ 
        └── Active Directory 
            │ 
            └── AZ-FILE01 
                └── File Server 
                
--- 

# ✔ Status 

✔ File Server role installed 
✔ Shared folder created 
✔ SMB share configured 
✔ Network share validated 