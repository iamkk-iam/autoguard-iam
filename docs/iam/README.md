# Core IAM

Identity and access management (IAM) establishes who or what can access a resource, under which conditions, and how that access is maintained and removed. It includes workforce, customer, partner, administrator, and workload identities.

## Access lifecycle

1. **Establish identity:** define authoritative sources and verify identity attributes appropriate to the service and risk.
2. **Authenticate:** verify the claimant with suitable authenticators and assurance; apply stronger controls to higher-risk access.
3. **Authorize:** grant only task-relevant permissions, scoped to the resource and action.
4. **Monitor:** record sign-ins, authorization changes, failures, and sensitive actions; alert on meaningful anomalies.
5. **Review and change:** update access when roles, devices, risk, or business needs change.
6. **Revoke:** promptly disable accounts, sessions, credentials, and grants when access is no longer needed.

## Core design principles

- Prefer unique identities and attributable activity; avoid shared human accounts.
- Use least privilege and deny access by default where practical.
- Separate routine user access from administration.
- Use MFA and risk-aware controls, especially for administrators and sensitive actions.
- Prefer short-lived credentials and federated access over long-lived secrets.
- Use role-based access control (RBAC) for stable job functions; consider attribute-based access control (ABAC) when decisions depend on context such as resource, device, or environment.
- Design for recovery: keep emergency access limited, monitored, tested, and documented.
- Protect identity infrastructure itself as a critical control plane.

## Access decision checklist

For each application or resource, record:

- Resource owner and data classification.
- Identity types that need access.
- Required actions and scope.
- Authentication and session requirements.
- Approval and separation-of-duties requirements.
- Provisioning and deprovisioning path.
- Logging, review frequency, and exception process.

## Useful operating measures

Track measures such as time to remove access after departure, MFA coverage, number of standing administrator assignments, stale or orphaned accounts, overdue access reviews, and permissions with no observed business use. Define a clear denominator and owner for each metric.

## Related topics

See [IGA](../iga/README.md) for governance, [PAM](../pam/README.md) for elevated access, and [federation and provisioning](../federation/README.md) for cross-system identity flows.
