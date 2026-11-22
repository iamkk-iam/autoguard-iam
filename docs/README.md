# IAM workspace guide

This folder is a vendor-neutral reference library for identity and access management. Use it to collect concepts, design notes, implementation checklists, and links to authoritative sources.

## Topics

- [Core IAM](iam/README.md): identity lifecycle, authentication, authorization, and access controls.
- [Identity governance (IGA)](iga/README.md): access requests, approvals, reviews, lifecycle, and evidence.
- [Privileged access (PAM)](pam/README.md): elevated accounts, just-in-time access, secrets, sessions, and emergency access.
- [Federation and provisioning](federation/README.md): SSO protocols, trust, claims, and account provisioning.
- [Cloud IAM](cloud-iam/README.md): human and workload identities, roles, policy boundaries, and cloud access reviews.
- [References](references.md): standards and official implementation guidance.

## How to use this library

Keep each page focused on one topic. Mark organization-specific decisions as **local policy** and record the owner, rationale, and review date. Link to vendor documentation for product behavior instead of copying large sections.

This repository is public. Do not commit credentials, access tokens, private customer data, production identifiers, or internal-only security details.
