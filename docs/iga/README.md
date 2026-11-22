# Identity governance and administration (IGA)

IGA governs how access is requested, approved, provisioned, reviewed, changed, and removed. It connects business ownership and policy to technical permissions.

## Core processes

- **Joiner, mover, leaver:** start, role change, and departure events should flow from trusted sources to access changes, with defined owners and completion targets.
- **Access requests:** present a clear entitlement, business purpose, duration, and data or system scope. Route decisions to accountable approvers.
- **Provisioning:** automate repeatable grants and removals where possible; reconcile the intended state with target systems and report failures.
- **Access reviews:** ask resource or data owners to confirm continued need. Escalate overdue reviews and track remediation to completion.
- **Separation of duties:** identify incompatible permissions, prevent or approve exceptions explicitly, and monitor compensating controls.
- **External identities:** define sponsors, expiry dates, permitted resources, and renewal or removal steps for partners and guests.
- **Non-human identities:** assign owners, purposes, scopes, expiry or rotation rules, and review dates to service accounts and automation identities.

## Minimum entitlement record

For each role or access package, document its owner, purpose, included permissions, eligible population, approval path, duration, review cadence, conflicts, and provisioning/deprovisioning behavior.

## Review workflow

1. Set a risk-based scope and review period.
2. Give reviewers understandable context: user, entitlement, last activity when available, and business owner.
3. Record approve, revoke, or reassign decisions with the reviewer and timestamp.
4. Track removals and exceptions until verified.
5. Retain evidence according to the organization’s policy.

## Common failure modes

- Approving access without a named owner or business reason.
- Treating a completed review as remediation when removals were not applied.
- Letting birthright access accumulate after role changes.
- Leaving guests and temporary workers without expiry or sponsor.
- Using broad groups as a shortcut around entitlement ownership.
- Treating an automated workflow as correct without reconciliation and exception monitoring.

## Implementation notes

Keep policy choices specific to the organization and applicable regulation. This guide is a starting point; it does not prescribe universal review intervals or approval thresholds.
