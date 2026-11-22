# Cloud IAM

Cloud IAM defines access to cloud control planes and workloads. Build a separate model for human operators and software workloads, then connect both to the organization’s identity lifecycle and monitoring.

## Human access

- Federate workforce users through a managed identity provider where supported.
- Use short-lived sessions and require stronger authentication for privileged or sensitive actions.
- Assign roles by job function and resource scope; avoid broad account-wide administrator access for routine work.
- Use time-bound elevation for exceptional administrative tasks.
- Review cross-account, cross-project, and external-tenant access.

## Workload access

- Prefer platform-native workload identities or role assumption with short-lived credentials.
- Avoid embedding long-lived access keys in source code, images, or CI logs.
- Restrict trust policies to expected workloads, repositories, environments, and audiences.
- Separate production and non-production identities and permission sets.
- Rotate or revoke credentials when a workload is retired or suspected to be compromised.

## Policy lifecycle

1. Identify the principal, owner, workload, and business purpose.
2. Scope allowed actions to required resources and conditions.
3. Validate the policy and test both intended access and denied access.
4. Deploy through reviewed, version-controlled configuration when practical.
5. Monitor use and unexpected policy changes.
6. Remove unused roles, keys, grants, and trust relationships.

## Cloud review checklist

- Is the cloud root or tenant recovery identity protected and excluded from routine use?
- Are human users and workloads using distinct identities?
- Are permissions scoped to required actions and resources?
- Are trust relationships limited to expected principals and conditions?
- Are unused credentials and access paths removed?
- Are policy changes and privileged actions logged and alertable?
- Is there an owner and review date for each high-privilege grant?

Provider-specific configuration belongs in clearly named subpages, such as `aws.md`, `azure.md`, or `gcp.md`. Validate every example against the provider’s current documentation before use. See the [AWS IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) for an official provider-specific example.
