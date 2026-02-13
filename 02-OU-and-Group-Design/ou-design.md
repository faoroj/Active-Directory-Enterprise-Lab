# OU and Security Group Design – JojaCorp

## Objective

Design a scalable Active Directory structure for JojaCorp that supports departmental organization, role-based access control, and efficient administration.

The goal was to follow enterprise best practices by separating users, computers, and security groups into dedicated Organizational Units (OUs).

---

## Business Scenario

JojaCorp is a small organization with multiple departments:

* Human Resources (HR)
* Sales
* Information Technology (IT)

The company requires:

* Centralized user management
* Department-based access control
* Structured placement of computers and service accounts
* A secure offboarding process for terminated employees

---

## Organizational Unit Structure

The following top-level OUs were created:

```
jojacorp.local
│
├── _Users
│   ├── HR
│   ├── Sales
│   └── IT
│
├── _Groups
├── _Computers
├── _Disabled
└── _ServiceAccounts
```

### Design Considerations

* **_Users**: Department-based user organization for easier administration and Group Policy targeting.
* **_Groups**: Central location for all security groups.
* **_Computers**: Dedicated container for domain-joined workstations.
* **_Disabled**: Used for offboarding to prevent accidental reactivation and maintain audit history.
* **_ServiceAccounts**: Reserved for future application or service identities.
* Underscore naming (`_`) ensures administrative OUs appear at the top of the directory.

---

## Default Container Redirection

To enforce administrative structure, default object locations were redirected:

```
redirusr "OU=_Users,DC=jojacorp,DC=local"
redircmp "OU=_Computers,DC=jojacorp,DC=local"
```

This ensures new users and computers are automatically placed into managed OUs instead of the default containers.

---

## Security Group Design

The following **Global Security Groups** were created inside `_Groups`:

| Group Name        | Purpose                          |
| ----------------- | -------------------------------- |
| HR_File_Access    | Access to HR shared resources    |
| Sales_File_Access | Access to Sales shared resources |
| IT_Admins         | Elevated privileges for IT staff |
| VPN_Users         | Remote access authorization      |

### Design Principles

* **Role-based access control (RBAC)**
* Permissions assigned to **groups**, not individual users
* Global scope for department-level membership
* Security type for use with NTFS, shares, and policies

---

## Screenshots

* OU structure
* Default container redirection
* Security group creation

Location:

```
/screenshots/ou/
/screenshots/groups/
```

---

## Skills Demonstrated

* Active Directory OU design and hierarchy planning
* Role-based access control (RBAC)
* Default container management
* Enterprise organizational standards
* Security-focused directory architecture
