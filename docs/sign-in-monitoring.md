# Sign-in monitoring

[Back to project overview](../README.md)

## Recorded event

The published screenshot contains one successful sign-in for Alice IT.

| Field visible in the screenshot | Recorded value |
| --- | --- |
| User | Alice IT |
| Date | 2026-10-02T13:23:55Z |
| Status | Success |
| Authentication requirement | Single-factor authentication |
| Continuous access evaluation | No |

The timestamp explicitly uses UTC, indicated by the Z suffix.

![Alice IT successful sign-in with a single-factor authentication requirement](../screenshots/05-alice-signin-success.png)

## What this demonstrates

The image shows that Alice's sign-in was recorded and succeeded. It supports analysis of the user, time, outcome, and authentication requirement.

It does not demonstrate completed MFA. It does not show the Authentication details tab, the application name, location, device details, or a configured Conditional Access policy. Those details are not inferred from the visible tab names.

Earlier documentation mentioned interrupted events and password-related issues, but no such events are included in the published screenshots. They are not presented as verified results.

## Review procedure

The following is a procedure for repeating or extending the analysis, not a claim that additional evidence was collected.

1. Open the tenant's sign-in logs with an account authorized to read them.
2. Filter for the test user and the relevant time range.
3. Open the event and record its timestamp, status, and authentication requirement.
4. Inspect Authentication details before describing the methods used or any MFA result.
5. Record application and device information only when those fields are visible.
6. Save a capture that preserves the relevant context and omits authentication secrets.

Microsoft's [sign-in activity details reference](https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-in-log-activity-details) explains the event tabs and authentication details.

## Retention and evidence limits

The screenshot is a historical observation from 2 October 2026, not a live monitoring dashboard. Microsoft documents seven-day retention for sign-in and audit logs in Entra ID Free in its [data retention reference](https://learn.microsoft.com/en-us/entra/identity/monitoring-health/reference-reports-data-retention). The original event may therefore no longer be available in the live portal when this repository is reviewed.

No alerting, automated detection, log export, or SIEM integration is demonstrated. See [security controls](security-controls.md) for the unverified Security Defaults setting and [evidence review](evidence-review.md) for the screenshot inventory.
