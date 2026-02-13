# Environment Setup

## Objective

Build a virtual Active Directory environment with a Domain Controller and a domain-joined client.

## Infrastructure

| Machine | Role              |
| ------- | ----------------- |
| DC01    | Domain Controller |
| PC01    | Domain Client     |

## Configuration

### Domain Controller

* OS: Windows Server 2022
* Hostname: DC01
* Static IP configured
* Active Directory Domain Services installed
* New domain created: **Jojacorp.local**

### Client Machine

* OS: Windows 10/11
* Hostname: PC01
* Joined to the domain: Jojacorp.local

## Verification

* Domain login successful on PC01
* Active Directory Users and Computers accessible
* DNS is functioning correctly

## Screenshots

### Server Renamed
#### The server was renamed according to enterprise naming standards.
![Server renamed](../screenshots/environment/server-renamed-DC01.png)


### Static IP Configuration
#### A static IP address was configured to ensure reliable DNS and domain services.
![Static IP configuration](../screenshots/environment/static-ip-config.png)


### Active Directory Role Installation
#### Active Directory Domain Services (AD DS) was installed on the server using Server Manager.
![Active Directory installation](../screenshots/environment/ad-ds-installed.png)


### Domain Created
#### The new Active Directory forest and domain jojacorp.local was successfully created.
![Domain created](../screenshots/environment/domain-created.png)


### DNS Configuration
#### Forward Lookup Zone for jojacorp.local confirming integrated DNS required for Active Directory.
![DNS forward lookup zone](../screenshots/environment/dns-forward-lookup.png)


### Client Joined to Domain
#### Workstation PC01 successfully joined to the domain and registered in Active Directory.
![PC01 joined to domain](../screenshots/environment/pc01-domain-join.png)


### Domain Authentication Verified
#### Successful login to PC01 using a domain user account, confirming authentication and connectivity.
![Successful domain login](../screenshots/environment/domain-login-success.png)
