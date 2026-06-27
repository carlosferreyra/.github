# Community health files

## `CODE_OF_CONDUCT.md`

**Purpose:** defines acceptable conduct, enforcement responsibility, reporting,
and consequences.

**Use the default when:** the same maintainer and enforcement contact apply.

**Override when:** a project has its own moderation team, reporting address, or
community-specific scope.

**Verify:** open **Insights > Community Standards** in a consuming repository
and confirm GitHub detects the code of conduct.

## `CONTRIBUTING.md`

**Purpose:** sets the contribution workflow, branch and commit conventions,
local verification expectations, and review process.

**Use the default when:** the repository follows the baseline fork, branch,
test, and pull request workflow.

**Override when:** setup commands, generated files, release branches, or review
requirements differ. A project-specific guide should include exact commands.

**Verify:** start a new issue or pull request and confirm GitHub links to the
contribution guide.

## `GOVERNANCE.md`

**Purpose:** documents decision authority, consensus rules, contributor roles,
and maintainer selection.

**Use the default when:** the projects share the same owner and decision model.

**Override when:** a repository has multiple maintainers, delegated ownership,
an RFC process, or a different escalation path.

## `SECURITY.md`

**Purpose:** tells researchers what versions are supported, how to report a
vulnerability privately, expected response times, and disclosure rules.

**Use the default when:** the same security contact and support window apply.

**Override when:** a project supports multiple release lines, has a dedicated
security team, or cannot use private vulnerability reporting.

**Repository setup:** enable **Settings > Security > Private vulnerability
reporting** where supported. The default policy cannot enable that feature.

**Verify:** open the consuming repository's **Security** tab and confirm the
policy is linked. Never test by publishing a real vulnerability as an issue.

## `SUPPORT.md`

**Purpose:** routes usage questions, bugs, feature requests, security reports,
and private contact to the right channel.

The default avoids hardcoded repository URLs because the same document is
rendered from many repositories. It refers to the current repository's tabs and
templates instead.

**Override when:** a project has dedicated documentation, chat, commercial
support, or response commitments.

## `FUNDING.yml`

**Purpose:** configures the Sponsor button.

The source is [`.github/FUNDING.yml`](https://github.com/carlosferreyra/.github/blob/main/.github/FUNDING.yml).
Platform values must follow GitHub's supported funding schema. Keep account-wide
funding here; use a local `FUNDING.yml` when proceeds belong to a different
project or organization.

**Verify:** open a consuming repository and check for the Sponsor button. GitHub
may suppress it when sponsorship is disabled or the configuration is invalid.

## Editing checklist

Before changing a shared health file:

1. Search for repository-specific names, paths, labels, teams, and URLs.
2. Phrase navigation relative to the consuming repository.
3. Avoid promises that cannot be met across every repository.
4. Preview Markdown and verify all public contact channels.
5. Test inheritance in a public repository without a local override.
