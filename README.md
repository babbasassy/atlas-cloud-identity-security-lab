# ATLAS Cloud Identity Security Lab

**Microsoft Entra ID | Identity & Access Management | Security Monitoring | User Lifecycle Management**

## Project Overview

This project demonstrates the configuration and management of a cloud identity environment using Microsoft Entra ID Free.

The lab simulates a small organization with separate IT, HR, and Finance departments. It focuses on identity administration, user access management, security configuration, authentication monitoring, and employee offboarding.

The objective was to gain hands-on experience with identity and access management (IAM) and understand how cloud identities can be managed and secured in an enterprise environment.

## Technologies Used

- Microsoft Entra ID Free
- Microsoft Azure Portal
- Identity and Access Management (IAM)
- Role-Based Access Control (RBAC) concepts
- Microsoft Entra Security Defaults
- Authentication and sign-in logs
- User and group administration

## Lab Environment

The environment was created in a dedicated Microsoft Entra tenant named **ATLAS Cloud Lab**.

Three departments were established with corresponding test identities and security groups.

| Department | Test User | Security Group |
|---|---|---|
| IT | Alice IT | GRP-IT |
| HR | Sara HR | GRP-HR |
| Finance | Omar Finance | GRP-FINANCE |

A separate administrator account, **ATLAS Cloud Admin**, was also created for privileged administration.

All identities are fictional and used exclusively for demonstration and testing.

## Implemented Features

### 1. Identity and Group Management

Created cloud users and organized them into department-specific security groups.

This demonstrates the foundation of group-based access management and identity administration.

### 2. Administrative Role Management

Created a dedicated administrator identity and assigned the Global Administrator role.

The purpose was to separate ordinary test identities from privileged administrative access.

The Global Administrator role was used within the isolated lab; a production environment should apply least-privilege administration.

### 3. Security Configuration

Reviewed Microsoft Entra ID Security Defaults as a baseline identity security control, including its role in multifactor authentication and authentication protection.

Security Defaults and Conditional Access are different capabilities. Custom Conditional Access policies were not implemented in this Entra ID Free lab.

### 4. Authentication Monitoring

Performed authentication tests and inspected Microsoft Entra sign-in logs.

The investigation included:

- Successful user authentication
- Sign-in status and timestamps
- Application information
- Authentication requirements
- Interrupted sign-in events
- Password-related authentication issues

**Important observation:** A successful Alice IT sign-in was recorded with a single-factor authentication requirement. This event demonstrates sign-in logging but does not establish that MFA was completed during that specific sign-in.

### 5. User Offboarding

Simulated the departure of an employee using the Sara HR test account.

The offboarding workflow covered:

1. Disabling the user account
2. Removing department group membership
3. Revoking existing sign-in sessions

This demonstrates essential identity lifecycle procedures used when employees leave an organization.

## Evidence and Screenshots

### Tenant Overview

![Tenant Overview](screenshots/01-tenant-overview.png)

### User Management

![User Management](screenshots/02-users.png)

### Security Groups

![Security Groups](screenshots/03-groups.png)

### Administrator Role

![Administrator Role](screenshots/04-admin-role.png)

### Sign-in Monitoring

![Successful Sign-in](screenshots/05-alice-signin-success.png)

### Employee Offboarding

![Employee Offboarding](screenshots/06-sara-offboarding.png)

## Security Considerations

This lab was designed as a controlled learning environment.

- No production identities were used.
- Test account passwords and authentication secrets must not be published.
- Administrative access was separated from standard test accounts.
- Authentication logs were reviewed to understand identity
