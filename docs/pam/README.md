# Privileged access management (PAM)

PAM reduces the likelihood and impact of misuse or compromise of identities that can change security controls, administer infrastructure, access sensitive data, or create further privileged access.

## Scope

Inventory privileged human accounts, cloud roles, service and automation identities, emergency accounts, secrets, consoles, and the systems through which privileged work is performed. Record an owner and business purpose for every privileged path.

## Baseline controls

- Use separate, attributable administrator identities when the platform supports them.
- Require strong authentication and trusted access paths for privileged activity.
- Keep routine accounts unprivileged.
- Prefer eligible or just-in-time elevation with a specific task, narrow scope, short duration, and approval where risk requires it.
- Remove unused standing assignments and prohibit shared administrator credentials where feasible.
- Store necessary secrets in an approved vault; restrict retrieval, rotate according to risk, and audit access.
- Use hardened administrator workstations or equivalent device controls for critical systems.
- Log elevation, approvals, privileged commands or sessions where supported, and changes to identity policy.
- Alert on unexpected role grants, new credentials, bypasses, and emergency-account use.

## Emergency access

Maintain only the minimum break-glass access needed to recover the identity control plane. Protect credentials separately, limit who can use them, alert on every use, test recovery on a schedule, and document how credentials are rotated after use. Never store live emergency credentials in this repository.

## PAM review checklist

- Can every privileged identity and path be tied to an owner and purpose?
- Are permanent assignments justified and periodically reviewed?
- Can elevation be time-bound and scoped?
- Are approvals and sessions attributable and logged?
- Are secrets, service identities, and certificates included in inventory?
- Do alerts reach an on-call owner with a tested response?
- Has the recovery path been tested without weakening normal controls?

## Metrics

Useful measures include standing privilege, eligible versus active assignments, time to revoke access, privileged accounts without a clear owner, vault coverage, and time to detect or investigate privileged changes. Interpret these with workload and platform context.
