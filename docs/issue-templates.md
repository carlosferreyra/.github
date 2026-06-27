# Issue templates

The default issue forms live in `.github/ISSUE_TEMPLATE/`:

- `01-bug_report.yml`: reproducible defects; requests steps, expected and
  actual behavior, version, and operating system.
- `02-feature_request.yml`: product improvements; requests the problem,
  proposed outcome, and alternatives.
- `03-documentation.yml`: documentation corrections; requests the location,
  problem, and proposed change.
- `04-question.yml`: focused usage questions; requests the goal, attempted
  work, and environment.
- `05-test_case.yml`: missing test coverage; requests the scenario, expected
  behavior, and test type.

`config.yml` disables blank issues for contributors. Maintainers with sufficient
permission can still create a blank issue.

## Why defaults omit labels and assignees

Labels must exist in both this `.github` repository and every repository where
an inherited form is used. Teams, collaborators, and issue types also vary.
Portable defaults therefore collect information without assigning metadata.

Add metadata in a local override when the consuming repository owns the labels
and assignees:

```yaml
name: Bug report
description: Report a reproducible defect.
title: "[Bug]: "
labels: ["bug", "triage"]
assignees: ["maintainer-login"]
type: Bug
```

## Form anatomy

Each issue form contains:

- top-level chooser metadata: `name`, `description`, and optional `title`;
- a `body` list containing `markdown`, `input`, `textarea`, `dropdown`, or
  `checkboxes` entries;
- stable, unique `id` values for fields;
- `validations.required: true` only where triage cannot proceed without an
  answer.

Use required fields sparingly. A form should prevent avoidable back-and-forth,
not force users to invent irrelevant information.

## Local override procedure

1. Create `.github/ISSUE_TEMPLATE/` in the consuming repository.
2. Copy every default form that should remain available.
3. Copy and adjust `config.yml`.
4. Add local labels, assignees, issue types, and contact links.
5. Merge to the default branch.
6. Open the repository's **New issue** chooser and submit a disposable test
   issue.

Remember: adding one local file disables the entire default issue-template
folder for that repository.

## Contact links

Contact links in `config.yml` require absolute URLs and cannot interpolate the
current repository. Do not place a link to this `.github` repository's security
advisory or Discussions page in the shared config. Add repository-specific
contact links only in a local override.

## Validation checklist

- Parse every YAML file.
- Ensure `name` and `description` are present.
- Ensure every form field has a supported `type`.
- Ensure field IDs are unique within a form.
- Ensure dropdowns have options.
- Confirm referenced labels and assignees exist when a local override uses them.
- Preview the chooser and submit each form once after structural changes.

See GitHub's [issue form syntax](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
for the complete schema.
