# Active Directory Enterprise Lab

## Project Overview

This project simulates a small enterprise Active Directory environment to demonstrate real-world IT Analyst and Helpdesk responsibilities.

The lab was built using Windows Server and domain-joined client machines in a virtual environment. The goal was to practice user administration, access control, Group Policy management, and common troubleshooting tasks.

## Environment

* VirtualBox / VMware
* Windows Server 2022 (Domain Controller)
* Windows 10/11 Client
* Domain: Jojacorp.local

## Key Skills Demonstrated

* Active Directory user and group management
* Organizational Unit (OU) design
* Role-based access control using security groups
* User lifecycle management (onboarding, password resets, account lockout, offboarding)
* Group Policy configuration and deployment
* File share permissions (NTFS + security groups)
* Domain join and client management
* Basic PowerShell automation

## Lab Structure

1. [Environment Setup](./01-Environment-Setup/environment-setup.md)
2. [OU and Security Group Design](./02-OU-and-Group-Design/ou-design.md)
3. [User Lifecycle Management](./03-User-Lifecycle/user-lifecycle.md)
4. [Group Policy Implementation](./04-Group-Policy/group-policy.md)
5. [File Server and Access Control](./05-File-Server/file-server.md)
6. [Domain Join and Client Configuration](./06-Domain-Join/domain-join.md)
7. [PowerShell Automation](./07-Powershell/powershell.md)


Each section includes step-by-step documentation and screenshots.

## Business Scenario

A fictional company ("Joja Corp") with multiple departments (HR, Sales, IT) required centralized identity management, secure file access, and standardized security policies.

This lab demonstrates how an IT Analyst would deploy and manage this environment.

## Author

Jordon Faoro
