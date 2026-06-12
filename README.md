# Active Directory Home Lab

## Overview

This project demonstrates the deployment of a Windows Server Active Directory environment using VirtualBox. The purpose of this lab is to gain practical experience with common IT Support and System Administration tasks such as server installation, Active Directory deployment, DNS configuration, user management, and domain administration.

## Project Objectives

* Build a Windows Server lab environment using VirtualBox
* Configure a Domain Controller
* Deploy Active Directory Domain Services (AD DS)
* Configure DNS services
* Create and manage users and groups
* Join Windows 11 clients to the domain
* Simulate common IT Support tasks and troubleshooting scenarios
* Document all configuration steps and findings

## Environment

### Host Machine

* CPU: AMD Ryzen 5 7600
* RAM: 32 GB
* Storage: 400 GB available on Local Disk D:

### Virtualization Platform

* VirtualBox

### Virtual Machines

#### DC01

* Operating System: Windows Server
* Role: Domain Controller
* RAM: 8 GB
* CPU: 2 vCPUs
* Disk: 80 GB

#### CLIENT01 (Planned)

* Operating System: Windows 11
* Role: Domain-Joined Workstation
* RAM: 8 GB
* CPU: 2 vCPUs
* Disk: 60 GB

## Project Progress

### Completed

* Installed VirtualBox
* Created Windows Server virtual machine
* Installed Windows Server
* Renamed server to DC01
* Configured Host-Only Networking
* Assigned Static IP Address
* Installed Active Directory Domain Services
* Created New Forest
* Created Domain: lab.local
* Promoted DC01 to Domain Controller
* Installed DNS Server

### In Progress

* Active Directory User Management
* Organizational Units (OUs)
* Security Groups

### Planned

* Windows 11 Client Deployment
* Domain Join Process
* Group Policy Configuration
* Password Reset Scenarios
* User Account Management
* Help Desk Ticket Simulations
* DNS Troubleshooting
* Network Troubleshooting

## Skills Demonstrated

* Windows Server Administration
* Active Directory Administration
* DNS Configuration
* Virtualization
* Network Configuration
* User and Group Management
* IT Troubleshooting
* Documentation

## Screenshots

Screenshots can be found in the `/screenshots` directory.

## Learning Outcomes

This project is designed to develop practical skills commonly used in entry-level IT Support, Service Desk, and System Administrator roles.

Key concepts learned:

* Active Directory
* Domain Controllers
* Authentication and Authorization
* DNS Services
* Static IP Configuration
* User Account Management
* Group Management
* Windows Server Administration

# User and Group Management

## Overview

This section documents the creation and management of Organizational Units (OUs), user accounts, and security groups within the Active Directory environment.

The objective is to simulate a real company structure and demonstrate common IT Support administration tasks.

---

## Organizational Units (OUs)

Organizational Units were created to organize users by department.

### Created OUs

```text
corp.local
│
├── IT
├── HR
└── Sales
```

### Purpose

Organizational Units help administrators:

* Organize users and computers
* Apply Group Policies
* Delegate administration
* Simplify management of large environments

---

## User Account Creation

Several user accounts were created to simulate employees within different departments.

### IT Department

| Name        | Username |
| ----------- | -------- |
| Phyo Hein   | phyo     |
| John Smith  | john     |
| Sarah Jones | sarah    |

### HR Department

| Name       | Username |
| ---------- | -------- |
| Emma Brown | emma     |

### Sales Department

| Name         | Username |
| ------------ | -------- |
| James Wilson | james    |

### User Account Purpose

Active Directory user accounts provide:

* Centralized authentication
* Centralized password management
* Permission management
* Access to company resources

Example domain login:

```text
phyo@corp.local
```

---

## Security Group Creation

Security groups were created to simplify permission management.

### Groups

| Group Name  |
| ----------- |
| IT_Users    |
| HR_Users    |
| Sales_Users |

### Group Scope

```text
Global
```

### Group Type

```text
Security
```

### Purpose

Security groups allow permissions to be assigned to groups rather than individual users.

This follows Microsoft Active Directory best practices and simplifies administration.

---

## Group Membership

### IT_Users

```text
IT_Users
│
├── Phyo Hein
├── John Smith
└── Sarah Jones
```

### HR_Users

```text
HR_Users
│
└── Emma Brown
```

### Sales_Users

```text
Sales_Users
│
└── James Wilson
```

---

## Why Security Groups Are Important

Without security groups, permissions would need to be assigned to each user individually.

Example:

```text
IT Documentation Folder
├── Phyo
├── John
└── Sarah
```

This becomes difficult to manage as the company grows.

Using security groups:

```text
IT Documentation Folder
└── IT_Users
```

All users who are members of the IT_Users group automatically receive the required permissions.

This makes onboarding and offboarding employees significantly easier.

---

## Skills Demonstrated

* Organizational Unit (OU) creation
* Active Directory user administration
* User account creation
* Security group creation
* Group membership management
* Access control concepts
* Authentication and authorization concepts
* Enterprise user management practices

---

Examples include:

* Organizational Unit structure
* User account creation
* Group creation
* Group membership configuration

---

## Learning Outcome

Through this exercise, I gained practical experience with Active Directory user and group administration, which are common responsibilities performed by IT Support and System Administration teams in enterprise environments.

