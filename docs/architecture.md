ATLAS Cloud Identity Security Lab – Architecture

1. Overview

ATLAS Cloud Lab is a simulated cloud identity environment built using Microsoft Entra ID Free.

The environment represents a small organization with three departments: IT, HR, and Finance.

The lab focuses on identity administration, group-based access management, authentication monitoring, privileged administration, and employee offboarding.

2. Environment

Component

Configuration

Identity provider

Microsoft Entra ID

Tenant name

ATLAS Cloud Lab

License

Microsoft Entra ID Free

Cloud users

5

Security groups

3

Administrative role

Global Administrator

Management interface

Microsoft Azure Portal

No production systems or paid Azure infrastructure resources were required for this lab.

3. Identity Structure

The following test identities were created:

Account

Purpose

Alice IT

IT department user

Sara HR

HR department user and offboarding test

Omar Finance

Finance department user

ATLAS Cloud Admin

Dedicated administrative account

Tenant owner

Initial tenant administrator

Three department-specific security groups were also configured:

GRP-IT

GRP-HR

GRP-FINANCE

These groups demonstrate how organizations can organize identities and manage access based on departmental responsibilities.

4. Administrative Architecture

A dedicated administrator account was created and assigned the Global Administrator role.

This separates privileged administration from ordinary test user accounts.

The Global Administrator role provides extensive directory management permissions. In a production environment, more restricted administrative roles should be preferred wherever possible.

5. Authentication and Monitoring

Microsoft Entra ID provides authentication services for cloud identities.

Sign-in logs were used to examine:

Authentication outcomes

Successful and interrupted sign-ins

Authentication requirements

Sign-in timestamps

Application information

Password-related authentication problems

A successful Alice IT sign-in was recorded, demonstrating the availability of identity authentication logs.

6. Identity Lifecycle

The environment was used to simulate basic employee identity lifecycle operations:

Provisioning: Creating a user account.

Access assignment: Adding a user to an appropriate department group.

Monitoring: Reviewing authentication events.

Offboarding: Disabling a user account, removing group membership, and revoking sign-in sessions.

Sara HR was selected as the offboarding test identity.

7. Security Design Considerations

Department-specific security groups

Separate administrative identity

Authentication monitoring

Account disabling during offboarding

Group membership removal

Session revocation

No production user credentials

No exposed authentication secrets

This architecture is intended for security education and portfolio demonstration rather than production deployment.

8. Conclusion

The ATLAS Cloud Identity Security Lab demonstrates the foundational architecture of a cloud-based identity management environment.

The lab provides practical experience with Microsoft Entra ID, privileged administration, authentication logging, and secure user lifecycle operations.
