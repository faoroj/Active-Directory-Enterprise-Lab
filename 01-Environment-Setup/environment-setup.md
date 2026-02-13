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
![Server renamed](../screenshots/environment/server-renamed-DC01.png)

![Static IP configuration](../screenshots/environment/static-ip-config.png)

![Active Directory installation](../screenshots/environment/ad-ds-installed.png)

![Domain created](../screenshots/environment/domain-created.png)

![DNS forward lookup zone](../screenshots/environment/dns-forward-lookup.png)

![PC01 joined to domain](../screenshots/environment/pc01-domain-join.png)

![Successful domain login](../screenshots/environment/domain-login-success.png)
