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
* Created Domain: corp.local
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

## Documentation

Detailed project documentation can be found in the `/documentation` directory.

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

## Future Improvements

* Deploy additional client machines
* Configure DHCP services
* Create Group Policy Objects (GPOs)
* Implement file shares and permissions
* Simulate real-world support tickets
* Expand to a multi-server environment
