# Active Directory Configuration

## 1. Overview
Active Directory Domain Services (AD DS) was configured on Windows Server 2022 to manage users, computers, and security groups within the lab domain.

The domain controller is named **DC01**, and the domain is **lab.local**.

## 2. Domain Configuration

| Setting | Configuration |
| :--- | :--- |
| **Server hostname** | DC01 |
| **Domain name** | lab.local |
| **NetBIOS name** | LAB |
| **Server IP address** | 192.168.0.10 |
| **Server role** | Active Directory Domain Services |

## 3. Organizational Unit
An Organizational Unit (OU) named **IT-Department** was created.

An OU allows administrators to organize directory objects and apply Group Policy settings to specific groups of users or computers.

## 4. User Accounts
Two domain user accounts were created:

| Full Name | Username |
| :--- | :--- |
| John Smith | jsmith |
| Jane Brown | jbrown |

These accounts are located inside the IT-Department OU.

## 5. Security Group
A security group named **IT Support** was created inside the IT-Department OU.

The following users were added as members:
* John Smith (jsmith)
* Jane Brown (jbrown)

Security groups simplify permission management by allowing administrators to assign permissions to a group instead of managing each user individually.

## 6. Domain Client Integration
A Windows 11 Pro workstation named **CLIENT01** was joined to the lab.local domain.

Domain authentication was tested by signing in with a domain user account.

The workstation uses the domain controller for DNS and domain services.

## 7. Verification
The following activities were completed:
* [x] Confirmed the lab.local domain was available.
* [x] Verified the IT-Department OU.
* [x] Confirmed both user accounts existed.
* [x] Verified both users were members of IT Support.
* [x] Successfully joined CLIENT01 to the domain.
* [x] Successfully signed in using a domain account.

## 8. Skills Practised
* Active Directory Domain Services.
* Domain controller administration.
* Organizational Unit management.
* User account creation and administration.
* Security group management.
* Domain joining and authentication.
* Basic Windows Server troubleshooting.

## 9. Next Steps
Further exercises will cover DNS administration, shared folder permissions, PowerShell administration, and additional Group Policy configurations.
