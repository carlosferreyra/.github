---
layout: default
title: Discussion templates
---

Discussion category forms live in `.github/DISCUSSION_TEMPLATE/`. This
repository supplies forms for ideas, questions and answers, and show-and-tell
posts.

## Prerequisites

- Discussions must be enabled in the consuming repository.
- Matching categories must already exist.
- The form filename must match the category slug expected by GitHub.

The templates cannot enable Discussions, create categories, or guarantee that
labels exist. The shared forms therefore avoid repository-specific labels.

## Form responsibilities

### Ideas

Captures a concise pitch, motivation, implementation details, and alternatives.
Use it before work is sufficiently defined for a feature issue.

### Q&A

Captures a focused question, user context, attempted work, and environment. Use
the Q&A category so accepted answers remain searchable.

### Show and tell

Captures what someone built, a project link, implementation context, and the
feedback requested from the community.

## Local customization

Create a local form when a repository uses different category names, requires
domain-specific fields, or has labels known to exist. Keep field IDs stable if
automation reads discussion form output.

## Verification

1. Enable Discussions in repository settings.
2. Create or verify the expected categories.
3. Start a new discussion in each category.
4. Confirm the matching form appears and required validation works.
5. Cancel the test before publishing, or delete the disposable discussion.

See GitHub's [discussion category form documentation](https://docs.github.com/en/discussions/managing-discussions-for-your-community/creating-discussion-category-forms)
for schema and category requirements.
