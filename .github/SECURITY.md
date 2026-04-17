# Security Policy

This policy is the default for repositories owned by
[@carlosferreyra](https://github.com/carlosferreyra) that do not define their
own `SECURITY.md`. Individual repositories may publish a stricter policy.

## Supported Versions

Unless a repository states otherwise, only the **latest release on the default
branch** receives security fixes. Older tags are supported on a best-effort
basis.

| Version        | Supported          |
| -------------- | ------------------ |
| latest release | :white_check_mark: |
| older releases | :x:                |

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security problems.**

### Preferred channel — GitHub Security Advisories

1. Go to the affected repository on GitHub.
2. Open the **Security** tab → **Advisories** → **Report a vulnerability**.
3. Fill out the private advisory form.

This keeps the report private until a fix is ready and lets us coordinate a
CVE if one is warranted.

### Alternative channel — Email

If the repository has private vulnerability reporting disabled, email
[contact@carlosferreyra.me](mailto:contact@carlosferreyra.me) with:

- A description of the vulnerability and its impact.
- Affected repository, versions, and commit SHA.
- Steps to reproduce (minimal PoC preferred).
- Any suggested mitigation.
- Whether you would like to be credited in the advisory.

If you want to encrypt the report, request a public key in a first,
content-free email.

## Response Timeline

We aim to:

- **Acknowledge** your report within **3 business days**.
- **Provide a triage assessment** (severity + next steps) within **7 days**.
- **Release a fix** for High/Critical issues within **30 days**, Medium within
  **90 days**. Low-severity issues are patched on the normal release cadence.

These are targets, not guarantees — these are personal projects maintained on
a best-effort basis.

## Disclosure Policy

- We follow **coordinated disclosure**: please give us a reasonable window to
  ship a fix before publishing details.
- We will credit reporters in the published advisory unless asked not to.
- We publish advisories via GitHub Security Advisories and, when applicable,
  request a CVE.

## Out of Scope

The following are generally **not** considered vulnerabilities:

- Missing security headers on static demo / documentation sites.
- Denial-of-service caused by exhausting resources on a local machine.
- Findings that require a compromised developer workstation or stolen
  credentials.
- Vulnerabilities in third-party dependencies — report those upstream, then
  open a regular issue here so we can bump the dependency.

## Safe Harbor

Researchers acting in good faith under this policy — avoiding privacy
violations, service disruption, and data destruction — will not have legal
action pursued against them for their research.

## Contact

- Security contact: [contact@carlosferreyra.me](mailto:contact@carlosferreyra.me)
- Maintainer: [Carlos Eduardo Ferreyra](https://github.com/carlosferreyra)
