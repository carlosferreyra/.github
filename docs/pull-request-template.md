---
layout: default
title: Pull request template
---

`.github/PULL_REQUEST_TEMPLATE.md` pre-populates the body of a new pull request
when a repository does not provide its own template.

## What the default asks for

- an issue-closing reference;
- a description of what changed and why;
- concrete test evidence;
- a contributor checklist;
- breaking-change and migration details;
- supporting context such as screenshots or benchmarks.

The comments in the template guide authors without cluttering the rendered pull
request after submission.

## Use the default when

- most changes should link to an issue;
- repositories share the same review expectations;
- tests and documentation are standard acceptance gates.

## Override when

- a repository uses a different issue tracker;
- release notes, migrations, screenshots, or security review are mandatory;
- generated changes use a shorter automation-specific template;
- the repository needs multiple templates.

## Multiple local templates

A consuming repository can create `.github/PULL_REQUEST_TEMPLATE/` and select a
template with a URL query:

```text
https://github.com/OWNER/REPOSITORY/compare/main...BRANCH?quick_pull=1&template=feature.md
```

Multiple templates are selected explicitly; GitHub does not display a pull
request template chooser equivalent to the issue chooser.

## Verification

1. Create a branch with a harmless documentation edit.
2. Open **Compare & pull request**.
3. Confirm the body is populated before typing anything.
4. Confirm local templates override the account default when present.
5. Close the disposable pull request without merging.
