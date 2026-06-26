---
layout: default
title: GitHub Repository Templates
---

This guide explains how the files in `carlosferreyra/.github` become defaults
for other public repositories owned by the same account. It focuses on what to
use, when to override it, and what GitHub does not propagate automatically.

## Start here

1. Read [Inheritance and precedence](./inheritance.md) before adding files to a
   consuming repository.
2. Review [Community health files](./community-health-files.md) for policies
   such as `SECURITY.md`, `CONTRIBUTING.md`, and `SUPPORT.md`.
3. Use [Issue templates](./issue-templates.md), [pull request templates](./pull-request-template.md),
   and [discussion templates](./discussion-templates.md) to understand the
   contributor-facing forms.
4. Follow [Repository operations](./repository-operations.md) for labels,
   settings, validation, local overrides, and GitHub Pages deployment.

## What this repository provides

| Capability | Source |
| --- | --- |
| Contributor behavior | `CODE_OF_CONDUCT.md` |
| Contribution workflow | `CONTRIBUTING.md` |
| Decision ownership | `GOVERNANCE.md` |
| Private vulnerability reporting guidance | `SECURITY.md` |
| Support routing | `SUPPORT.md` |
| Sponsor button | `FUNDING.yml` |
| Structured issue intake | `ISSUE_TEMPLATE/` |
| Pull request descriptions | `PULL_REQUEST_TEMPLATE.md` |
| Structured discussions | `DISCUSSION_TEMPLATE/` |

## Core rule

Defaults are fallbacks, not copied files. They do not appear in a consuming
repository's clone or history. A repository-local file of the same type wins.

## Source of truth

Behavior described here follows GitHub's official documentation:

- [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Configuring issue templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
- [Creating a pull request template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository)
- [Configuring a GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
