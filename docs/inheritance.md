---
layout: default
title: Inheritance and precedence
---

## Requirements

Default files work when:

- the source repository is public and named exactly `.github`;
- the consuming repository is owned by the same user or organization;
- the consuming repository does not define its own file of that type.

The fallback files are displayed by GitHub but are not copied into the
consuming repository. They are absent from clones, archives, packages, and Git
history.

## Lookup order

For community health Markdown files, GitHub checks the consuming repository in
this order:

1. `.github/`
2. repository root
3. `docs/`
4. the account's public `.github` repository using the same order

The first matching file wins. GitHub does not merge local and default content.

## Folder-level override

Issue templates have a stronger boundary. If a consuming repository contains
any file in `.github/ISSUE_TEMPLATE/`, GitHub does not use any files from the
default `ISSUE_TEMPLATE/` folder. Copy every form that repository still needs,
including `config.yml`, when creating a local override.

Discussion category forms are matched to existing discussion categories. A
template does not enable Discussions or create its category.

## Supported defaults

| Default | Required path in this repository |
| --- | --- |
| Code of conduct | `.github/CODE_OF_CONDUCT.md` |
| Contribution guide | `.github/CONTRIBUTING.md` |
| Governance | `.github/GOVERNANCE.md` |
| Security policy | `.github/SECURITY.md` |
| Support policy | `.github/SUPPORT.md` |
| Funding | `.github/FUNDING.yml` |
| Issue forms and chooser | `.github/ISSUE_TEMPLATE/` |
| Pull request template | `.github/PULL_REQUEST_TEMPLATE.md` |
| Discussion category forms | `.github/DISCUSSION_TEMPLATE/` |

## Not inherited

These files and settings remain per repository:

- `README.md`, `LICENSE`, `CODEOWNERS`, `.gitignore`, and `CITATION.cff`;
- GitHub Actions workflows and Dependabot configuration;
- Copilot custom instructions;
- labels, milestones, issue types, rulesets, environments, secrets, and branch
  protection;
- repository features such as Issues, Discussions, private vulnerability
  reporting, and GitHub Pages.

Keep non-inherited examples in a separate template repository or automation
system. Putting them here does not make them available to other repositories.

## Practical decision

Use the default when the policy is genuinely account-wide. Add a local override
when a repository has a different release model, support window, contributor
workflow, security contact, or issue intake process.
