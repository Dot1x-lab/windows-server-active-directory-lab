## Windows Server Lab — Environment Setup


# 1. Project Overview
This project uses Proxmox VE to build a virtual Windows Server environment for practising system administration, networking, and Active Directory.
The lab simulates a small business network with a Windows Server domain controller and a Windows 11 workstation.

# 2. Lab Hardware
| Component | Specification |
| :--- | :--- |
| Physical machine | Lenovo ThinkCentre |
| Processor | Intel Core i7 |
| RAM | 16 GB |
| Storage | 512 GB SSD |
| Hypervisor | Proxmox VE |

# 3. Virtual Machines
| VM ID | Name | Operating System | Purpose |
| :--- | :--- | :--- | :--- |
| 100 | ubuntu-server | Ubuntu Server Linux | Administration and monitoring |
| 101 | windows-server | Windows Server 2022 | Active Directory domain controller |
| 102 | windows11-client | Windows 11 Pro | Domain workstation |


# 4. Windows Server Configuration
* Hostname: DC01
* Domain name: lab.local
* Server role: Active Directory Domain Services
* DNS: Active Directory-integrated DNS
* Server IP address: 192.168.0.10


# 5. Active Directory Structure
The domain contains an organizational unit named:

IT-Department

The OU contains:
* John Smith (jsmith)
* Jane Brown (jbrown)
* IT Support (Security Group)

Both domain users are members of the IT Support group.


# 6. Windows Client Configuration
* Computer name: CLIENT01
* Operating system: Windows 11 Pro
* Domain: lab.local
* Domain controller: DC01

The Windows 11 workstation was successfully joined to the domain, and domain-user sign-in was tested.


# 7. Project Objectives
The lab is designed to practise:
* Installing and configuring Windows Server.
* Creating and managing an Active Directory domain.
* Creating organizational units, users, and security groups.
* Joining Windows workstations to a domain.
* Configuring and testing Group Policy.
* Managing domain password and account security policies.
* Performing administrative tasks using PowerShell.
* Troubleshooting Windows networking and authentication.


# 8. Current Progress

Completed:
* Proxmox installation and virtual machine deployment.
* Windows Server 2022 installation.
* Active Directory domain configuration.
* User and security group administration.
* Windows 11 domain joining.
* Group Policy configuration and testing.
* Domain password policy configuration.

Remaining:
* Complete account lockout testing and verification.
* Practise DNS administration and troubleshooting.
* Practise shared folders and NTFS permissions.
* Perform additional PowerShell administration exercises.
* Complete final testing and project documentation.


# 9. Learning Outcome
This project provides practical experience with Windows Server administration, Active Directory, domain authentication, Group Policy, virtualization, and enterprise network administration.
The environment is a personal learning lab and does not represent a production deployment.
