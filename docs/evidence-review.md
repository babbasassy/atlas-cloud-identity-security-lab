# Evidence and publication review

[Back to project overview](../README.md)

**Review date: 10 October 2026.**

This review covers the six existing PNG screenshots and the repository documentation. It does not provide live access to the Entra tenant or certify its current security configuration.

## Screenshot inventory

| File | What is visible | What it does not establish |
| --- | --- | --- |
| [01-tenant-overview.png](../screenshots/01-tenant-overview.png) | ATLAS Cloud Lab; Entra ID Free; 5 users; 3 groups; 0 applications and 0 devices in the overview | Security Defaults status or current tenant state |
| [02-users.png](../screenshots/02-users.png) | Three department test users, ATLAS Cloud Admin, and the tenant owner | Group membership, full role inventory, or each user's status |
| [03-groups.png](../screenshots/03-groups.png) | GRP-FINANCE, GRP-HR, and GRP-IT | Their member lists or resource permissions |
| [04-admin-role.png](../screenshots/04-admin-role.png) | Direct assignment of the built-in Global Administrator role | Account attribution, because the heading is outside the crop |
| [05-alice-signin-success.png](../screenshots/05-alice-signin-success.png) | Alice IT; Success; single-factor requirement; 2 October 2026 at 13:23:55 UTC | Completed MFA, authentication method sequence, or tenant-wide policy state |
| [06-sara-offboarding.png](../screenshots/06-sara-offboarding.png) | sara.hr; Account enabled: No; sessions-valid-from value on 2 October 2026 | A revocation audit event, removed membership, or a blocked sign-in test |

## Owner-confirmed facts

The lab owner confirms that:

- The Global Administrator assignment belongs to ATLAS Cloud Admin.
- Sara's sessions were revoked on 2 October 2026.
- Sara's group membership was removed during offboarding.

These statements are retained with attribution. The documentation does not present them as independently proven by screenshot fields that are outside the crop or absent.

## Secrets and privacy review

All six PNGs were opened and visually inspected at their original resolution. No visible passwords, bearer or access tokens, client secrets, private keys, MFA recovery codes, or enrollment QR codes were found. Labels such as Reset password and Password profile are controls in the portal, not exposed password values.

The images do contain the tenant domain, tenant and object identifiers, user display names, portions of user principal names, and sign-in request/correlation identifiers. These are identifiers, not authentication secrets. The user list includes the tenant owner's name. The images are therefore not represented as anonymized or as containing only fictional identities.

No screenshot redaction was needed for a visible authentication secret. The original image bytes were preserved while their paths were corrected. This visual review is scoped to the six published images and is not an exhaustive audit of every historical repository object.

## Publication corrections

- Moved the six original root-level .png.png files into screenshots/ with one .png extension.
- Moved identity-management.md from docs/docs/ into docs/.
- Completed the truncated README and repaired relative document and image links.
- Rebuilt the architecture document with Markdown headings, tables, and an identity diagram.
- Added security-control, sign-in, and offboarding documentation.
- Removed unsupported statements of tested features and clarified the strength of each result.

## Unverified items

Security Defaults status, completed MFA, individual group membership screenshots, the administrator identity in the role crop, the revocation audit event, and a blocked post-offboarding sign-in are not independently established by the published evidence.

Custom Conditional Access and paid Azure security services are outside the implemented lab scope. The repository remains a documented foundational IAM exercise, with evidence limits made explicit.
