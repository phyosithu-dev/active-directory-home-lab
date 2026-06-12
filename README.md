Active Directory Home Lab Documentation
Project Title

Windows Server Active Directory Home Lab

Project Goal

The goal of this project is to build a small business-style IT environment using VirtualBox, Windows Server, and Active Directory. This lab is designed to practise real IT Support tasks such as server setup, user management, DNS configuration, and domain controller deployment.

Tools Used
VirtualBox
Windows Server ISO
Host PC with 32GB RAM
Ryzen 5 7600 CPU
Local Disk D: for VM storage
Step 1: Created Windows Server Virtual Machine

A new virtual machine was created in VirtualBox.

VM Name: DC01
Purpose: Domain Controller
RAM: 8GB
CPU: 2 cores
Storage: 80GB dynamically allocated
Location: D: drive

The Windows Server ISO was attached to the VM and used to install Windows Server.

Step 2: Installed Windows Server

Windows Server was installed successfully inside VirtualBox.

During installation, the Desktop Experience version was selected so the server could be managed using the graphical interface instead of Server Core.

After installation, the Administrator account was created and the server was booted successfully.

Step 3: Renamed the Server

The server was renamed to:

DC01

Reason:
DC stands for Domain Controller, and 01 means it is the first domain controller in the lab. This follows real-world server naming conventions.

Step 4: Configured VirtualBox Network

The VM network adapter was changed to:

Host-Only Adapter

Reason:
A Host-Only network creates a private lab network between the virtual machines. This allows the Windows Server and future Windows 11 client machine to communicate without affecting the real home Wi-Fi network.

Step 5: Configured Static IP Address

A static IP address was configured on DC01:

IP Address: 192.168.56.10
Subnet Mask: 255.255.255.0
Default Gateway: blank
Preferred DNS: 192.168.56.10

Reason:
A Domain Controller should have a static IP address because clients need a consistent address to locate Active Directory and DNS services. If the IP changed after restart, client computers might not be able to find the domain controller.

Step 6: Installed Active Directory Domain Services

Using Server Manager:

Manage → Add Roles and Features

The following role was installed:

Active Directory Domain Services

Reason:
Active Directory Domain Services allows the server to manage users, computers, groups, authentication, passwords, and policies in a centralized domain environment.

Step 7: Promoted Server to Domain Controller

After installing AD DS, the server was promoted to a Domain Controller.

The selected option was:

Add a new forest

Reason:
This was the first domain controller in the lab, so a new forest and domain had to be created.

Step 8: Created New Domain

A new domain was created:

corp.local

Reason:
This domain represents a small company-style network. Future users and computers will join this domain.

Example future login:

phyo@corp.local
Step 9: Domain Controller Options

The following options were selected:

DNS Server: Enabled
Global Catalog: Enabled
Read-Only Domain Controller: Disabled
DNS Server

DNS was enabled because Active Directory depends on DNS. Client computers use DNS to locate the domain controller.

Global Catalog

Global Catalog was enabled because it helps Active Directory locate users, groups, and other objects in the domain.

Read-Only Domain Controller

This was disabled because the lab needs a full domain controller that can create users, reset passwords, and manage policies.

Step 10: DNS Delegation Warning

A DNS delegation warning appeared during setup.

This warning was ignored because this is a home lab and there is no existing parent DNS zone.

Reason:
DNS delegation is only needed in larger environments where a new domain is being added under an existing DNS structure.

Step 11: Installation Completed

The Active Directory Domain Services installation completed successfully and the server restarted.

After restart, DC01 became a fully working Domain Controller.

Current Lab Status

Completed:

VirtualBox installed
Windows Server installed
Server renamed to DC01
Host-Only network configured
Static IP configured
Active Directory Domain Services installed
New forest created
Domain created: corp.local
DC01 promoted to Domain Controller
Skills Practised
Virtual machine creation
Windows Server installation
Server naming conventions
Static IP configuration
Host-only networking
Active Directory installation
Domain Controller promotion
DNS role understanding
Domain and forest creation
Next Steps

The next stage of the project will be:

Create Organizational Units
Create user accounts
Create security groups
Install Windows 11 client VM
Join CLIENT01 to corp.local domain
Test domain user login
Simulate help desk tickets
