# Identity and Access Management

## 1. Overview

This document describes the identity and access management configuration implemented in the ATLAS Cloud Identity Security Lab using Microsoft Entra ID Free.

The lab simulates a small organization with three departments: IT, HR, and Finance.

The main objective was to gain practical experience with user provisioning, security groups, administrative roles, and identity lifecycle management.

## 2. User Accounts

Five cloud identities were present in the lab environment.

| Account | Purpose |
|---|---|
| Alice IT | IT department test user |
| Sara HR | HR department test user |
| Omar Finance | Finance department test user |
| ATLAS Cloud Admin | Dedicated administrator |
| Tenant owner | Initial tenant administration |

The accounts were managed through Microsoft Entra ID in the Azure portal.

### User Provisioning

The provisioning workflow included:

1. Navigating to Microsoft Entra ID.
2. Opening Users → All users.
3. Selecting New user → Create new user.
4. Configuring the display name and user principal name.
5. Creating the cloud identity.
6. Reviewing the new account in the user directory.

This process demonstrates basic user onboarding in a cloud identity environment.

## 3. Security Groups

Three security groups were created to represent departmental organization.

| Security Group | Department | Initial Test Member |
|---|---|---|
| GRP-IT | Information Technology | Alice IT |
| GRP-HR | Human Resources | Sara HR |
| GRP-FINANCE | Finance | Omar Finance |

Security groups provide a foundation for group-based access management.

Group membership can be used when assigning access to supported applications and resources.

In this lab, the groups primarily demonstrate identity organization and membership administration. No production application access permissions were configured.

## 4. Administrative Role Management

A dedicated account named **ATLAS Cloud Admin** was created and assigned the **Global Administrator** role.

The purpose was to separate privileged administrative operations from ordinary departmental accounts.

### Global Administrator

The Global Administrator role provides extensive permissions to manage Microsoft Entra ID and supported Microsoft services.

For this isolated lab, the role was used to demonstrate administrative role assignment.

In production environments, organizations should follow the principle of least privilege and use narrower administrative roles whenever possible.

## 5. Access Control Principles

The project demonstrates several identity security concepts.

### Separation of Duties

Departmental identities are distinct from the dedicated administrator account.

### Group-Based Administration

Departmental users are organized into security groups rather than managed as one undifferentiated collection.

### Privileged Access

Administrative permissions are assigned using built-in Microsoft Entra roles.

### Identity Lifecycle Management

User identities can be created, managed, monitored, disabled, and removed from groups.

These practices provide a foundation for enterprise identity and access management.

## 6. User Offboarding

An offboarding scenario was performed using the Sara HR test account.

The workflow included:

1. Disabling the account by setting Account enabled to No.
2. Removing membership from GRP-HR.
3. Revoking existing sign-in sessions.

The objective was to demonstrate how an organization can restrict access when an employee leaves.

Sara HR was retained as a disabled test identity for documentation purposes.

## 7. Evidence

### Cloud Users

![Cloud Users](../screenshots/02-users.png)

### Security Groups

![Security Groups](../screenshots/03-groups.png)

### Administrative Role

![Administrator Role](../screenshots/04-admin-role.png)

### User Offboarding

![User Offboarding](../screenshots/06-sara-offboarding.png)

## 8. Lessons Learned

This lab provided practical experience with:

- Microsoft Entra ID user provisioning
- Security group creation and membership management
- Administrative role assignments
- Separation of standard and privileged identities
- Cloud identity lifecycle management
- Secure employee offboarding
- Identity administration documentation

## 9. Conclusion

The ATLAS Cloud Identity Security Lab demonstrates foundational IAM practices using Microsoft Entra ID Free.

The project provides hands-on experience relevant to IT administration, identity security, cloud security, and entry-level cybersecurity roles.
