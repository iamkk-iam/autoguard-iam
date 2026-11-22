# Federation and provisioning

Federation lets a relying application accept an authentication result from a trusted identity provider. Provisioning manages the account and entitlement lifecycle in connected applications. They solve related but distinct problems: SSO does not by itself create, update, or remove every application account.

## Common standards

- **OpenID Connect (OIDC):** an identity layer built on OAuth 2.0, commonly used for modern web and native application sign-in.
- **SAML 2.0:** an XML-based federation protocol widely used for enterprise browser SSO.
- **SCIM:** a standard API for exchanging identity and group lifecycle data between systems. SCIM is for provisioning, not sign-in.

Choose protocols supported by both parties and document the trust model, supported flows, and operational owners.

## Trust configuration checklist

- Identify the identity provider, relying party, application owner, and support contacts.
- Use exact issuer, audience, redirect or assertion-consumer endpoints, and approved signing keys.
- Validate signature, issuer, audience, timestamps, nonce or state, and protocol-specific requirements.
- Send only required claims; define stable subject identifiers and avoid relying on mutable email addresses as permanent keys.
- Restrict who can create or change federation configuration and monitor those changes.
- Plan key rollover, certificate expiry, metadata refresh, logout behavior, and incident revocation.
- Test account linking, duplicate identities, guest flows, deprovisioning, and recovery paths.
- Use SCIM or another controlled provisioning path when application accounts and groups need lifecycle management.

## Operational records

For each integration, keep a non-secret record of protocol, owner, environment, identifiers that are safe to publish, claim mappings, provisioning scope, key rotation owner, test date, and recovery contact. Never commit private keys, client secrets, bearer tokens, or signed production assertions.
