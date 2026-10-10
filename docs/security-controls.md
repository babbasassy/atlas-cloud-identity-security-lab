# Security controls and evidence status

[Back to project overview](../README.md)

## Recorded controls

| Control or activity | Lab result | Evidence and limit |
| --- | --- | --- |
| Dedicated administrative identity | ATLAS Cloud Admin exists; its Global Administrator assignment is owner-confirmed | [Users](../screenshots/02-users.png) and [role view](../screenshots/04-admin-role.png); role crop omits the account heading |
| Department groups | Three groups exist | [Group directory](../screenshots/03-groups.png); membership and application authorization are not shown |
| Authentication review | Alice IT has a successful event with a single-factor requirement | [Sign-in details](../screenshots/05-alice-signin-success.png); completed MFA is not demonstrated |
| Account disabling | Sara's Account enabled value is No | [User properties](../screenshots/06-sara-offboarding.png) |
| Session revocation | Performed on 2 October 2026 according to the lab owner | The same properties view shows the sessions-valid-from timestamp; no revocation audit event is published |
| Group membership removal | Completed according to the lab owner | No membership screenshot or audit event is published |

## Security Defaults and MFA

**Security Defaults status is unverified in this tenant.** None of the six screenshots shows its configuration. No statement that it is enabled or disabled can be supported by this evidence.

Security Defaults is available with the free tier. Feature availability is different from confirmed tenant configuration. Microsoft's [Security Defaults documentation](https://learn.microsoft.com/en-us/entra/fundamentals/security-defaults) describes the setting and its protections.

Alice's event says **Single-factor authentication**. This documents the event's authentication requirement; it is not proof of completed MFA or proof that Security Defaults is disabled. A future MFA result should include the authentication details for the relevant event.

To close the configuration gap, capture the tenant's Security Defaults setting with the tenant context visible and record the observation date. Treat a later capture as current evidence, not retroactive proof of the 2 October state.

## License and implementation boundaries

The tenant overview shows Microsoft Entra ID Free. Custom Conditional Access policies were not implemented in this lab. Microsoft lists Conditional Access under premium licensing in its [Entra licensing reference](https://learn.microsoft.com/en-us/entra/fundamentals/licensing).

The repository makes no implementation claim for Privileged Identity Management, risk-based policies, Microsoft Sentinel, Log Analytics export, or other paid Azure security services. A visible Conditional access tab in a sign-in screen is not evidence that a policy was configured.

## Interpretation of the controls

A dedicated admin account does not establish least privilege. The published role assignment is Global Administrator, and the evidence does not contain a full role review.

Disabling Sara and revoking sessions are recorded offboarding actions. Their end-to-end effect on every application session was not tested in the published evidence. Application-managed sessions can require separate handling; see Microsoft's [access revocation guidance](https://learn.microsoft.com/en-us/entra/identity/users/users-revoke-access).

## Evidence improvements

- Capture the Security Defaults setting.
- Capture authentication details for a completed MFA test before claiming MFA validation.
- Include the administrator's identity and role in one view.
- Capture Sara's final membership state and an audit record of revocation.
- Record a blocked new sign-in after offboarding.

These are proposed follow-up validations. The [evidence review](evidence-review.md) records the current publication scope and screenshot privacy findings.
