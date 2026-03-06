# Windows Server Infrastructure Lab

This project demonstrates a **complete Windows Server infrastructure setup** created in a virtual lab environment.  
The goal of this lab is to simulate a **small company network** and implement essential Microsoft server services used in real organizations.

The environment includes **Active Directory, Group Policy, File Server configuration, network services, and security hardening**.

---

# Lab Environment

- Hypervisor: VirtualBox  
- Server: Windows Server (Domain Controller)  
- Client: Domain joined workstation  
- Domain Name: lab.local  

---

# Implemented Components

## Active Directory Domain Services

Installed and configured Active Directory Domain Services to create a centralized identity management system.  
The server was promoted to a Domain Controller and a new domain was created.

---

## Organizational Unit (OU) Structure

Designed an OU structure to organize users, computers, and resources by department.
ABC
├── HR
├── Accounts
├── Sales
├── IT
├── Workstations
├── Servers
└── Groups


This helps simplify **administration and policy management**.

---

## User Accounts

Created domain users for different departments and assigned appropriate permissions based on their roles.  
This simulates **employee accounts in an organization**.

---

## Security Groups

Created security groups for departments and resource access.

Example groups:

- HR_SG  
- Accounts_SG
- Sales_SG
- IT_SG

Groups simplify **access control and permission management**.

---

## AGDLP Permission Model

Implemented the **AGDLP model**:

**Accounts → Global Groups → Domain Local Groups → Permissions**

This model is commonly used in enterprise environments to manage permissions efficiently.
Example groups:

- DL_HR_SG  
- DL_Accounts_SG
- DL_Sales_SG
- DL_IT_SG
---

## File Server Configuration

Configured shared folders on the server to allow department-based file storage.

Example shares:

- HR Share  
- Accounts Share  
- Sales Share  
- IT Share  

Permissions were controlled using **NTFS permissions and security groups**.

---

## Drive Mapping using Group Policy

Configured **Group Policy Preferences** to automatically map network drives when users log in.

Example:

HR users automatically receive **HR shared drive**.

This improves **user productivity and simplifies access**.

---

## Home Folder Configuration

Configured home directories for users to provide **personal storage space** on the server.

Each user receives a dedicated folder mapped automatically during login.

---

## Folder Redirection

Configured folder redirection to store user data centrally on the server.

Redirected folders:

- Desktop  
- Documents  

Benefits include **centralized storage and easier backup**.

---

## File Server Resource Manager (FSRM)

Configured storage quotas using FSRM to control disk usage.

Example:

- User storage quota limit set to **2 GB**

This helps manage server storage efficiently.

---

## Shadow Copy

Enabled Shadow Copy on shared folders to allow **previous versions of files**.

Users can restore accidentally deleted or modified files without administrator intervention.

---

## DHCP Server Configuration

Configured DHCP to automatically assign IP addresses to client systems.

DHCP scope includes:

- IP address range  
- Subnet mask  
- Default gateway  
- DNS server  

This simplifies **network management**.

---

## Print Server Management

Configured printer sharing through the server and managed printer access for users.

Users can connect to network printers through the domain.

---

## Security Hardening

Implemented basic server security policies including:

- Password complexity policy  
- Account lockout policy  
- Restricted RDP access  
- Firewall configuration  
- User access control  

These measures help improve **server security and protect the network**.

---

## Windows Server Backup

Configured Windows Server Backup to protect system data and ensure recovery in case of failure.

Backups include:

- System state  
- Server data  

This supports **disaster recovery planning**.

---

# Skills Demonstrated

- Windows Server Administration  
- Active Directory Management  
- Group Policy Configuration  
- File Server Management  
- Network Services (DNS / DHCP)  
- Security Hardening  
- Backup and Recovery  
- IT Infrastructure Setup  

---

# Project Objective

This lab demonstrates **practical system administration skills** used to deploy and manage a Windows Server infrastructure for a small organization.

The project focuses on **identity management, file services, network configuration, and server security**.
