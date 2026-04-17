# `carlosferreyra/.github`

This is a **special "magic" repository** owned by
[@carlosferreyra](https://github.com/carlosferreyra). GitHub treats a
repository named `.github` as the source of truth for two things:

1. **Default community health files** — `CODE_OF_CONDUCT`, `CONTRIBUTING`,
   `SECURITY`, `SUPPORT`, `GOVERNANCE`, `FUNDING.yml`, issue / PR / discussion
   templates — that any of my other repositories will inherit if they don't
   ship their own.
2. **The profile page README** rendered at
   <https://github.com/carlosferreyra>, sourced from
   [`profile/README.md`](./profile/README.md).

> ⚠️ **Inheritance caveat:** community health fallbacks only apply when the
> consuming repo is **public** *and* doesn't already define its own copy of
> the file. They are not "merged" — it's all-or-nothing per file.

---

## 📂 Repository layout

```
.
├── .github/                    # Community health files + per-repo config
│   ├── CODE_OF_CONDUCT.md
│   ├── CONTRIBUTING.md
│   ├── GOVERNANCE.md
│   ├── SECURITY.md
│   ├── SUPPORT.md
│   ├── FUNDING.yml
│   ├── PULL_REQUEST_TEMPLATE.md
│   ├── copilot-instructions.md
│   ├── dependabot.yml
│   ├── ISSUE_TEMPLATE/
│   │   ├── config.yml
│   │   ├── 01-bug_report.yml
│   │   ├── 02-feature_request.yml
│   │   ├── 03-documentation.yml
│   │   ├── 04-question.yml
│   │   └── 05-test_case.yml
│   ├── DISCUSSION_TEMPLATE/
│   │   ├── ideas.yml
│   │   ├── q-and-a.yml
│   │   └── show-and-tell.yml
│   └── workflows/              # GitHub Actions for *this* repo only
├── profile/
│   └── README.md               # Renders on https://github.com/carlosferreyra
├── LICENSE
└── README.md                   # You are here
```

---

## 📑 File index

The table below lists every file in this repo, what it's for, and one concrete
use case.

### Community health (inherited as fallback by other public repos)

| File | Purpose | Example use case |
| ---- | ------- | ---------------- |
| [`.github/CODE_OF_CONDUCT.md`](./.github/CODE_OF_CONDUCT.md) | Community behavior standards (Contributor Covenant 2.0) and enforcement ladder. | When a contributor asks "what's expected of me here?", GitHub auto-links this file from the **Insights → Community Standards** checklist of every public repo without its own COC. |
| [`.github/CONTRIBUTING.md`](./.github/CONTRIBUTING.md) | Default contribution guide: workflow, branch naming, commit conventions, PR checklist. | When someone clicks "Contribute" on a repo without a custom guide, GitHub shows this file as the contribution playbook. |
| [`.github/GOVERNANCE.md`](./.github/GOVERNANCE.md) | Who decides what gets merged, how decisions are made, how to become a maintainer. | A new contributor opens a large RFC-style PR and references the governance file to understand the lazy-consensus process before asking for review. |
| [`.github/SECURITY.md`](./.github/SECURITY.md) | Vulnerability reporting policy, supported versions, response timelines, safe harbor. | A researcher finds an XSS in one of my apps and uses the **Security → Report a vulnerability** flow surfaced by this file instead of opening a public issue. |
| [`.github/SUPPORT.md`](./.github/SUPPORT.md) | Where users should go for help vs. issues vs. security vs. private contact. | A user has a usage question; GitHub points them to this file when they click "New issue" so they self-route to Discussions before filing noise. |
| [`.github/FUNDING.yml`](./.github/FUNDING.yml) | Configures the **Sponsor** button shown on every repo. Lists GitHub Sponsors, Buy Me a Coffee, and PayPal. | A user finds a project useful and clicks the ❤️ Sponsor button — they're sent to the configured funding platforms without me touching each repo. |

### Templates (inherited as fallback)

| File | Purpose | Example use case |
| ---- | ------- | ---------------- |
| [`.github/PULL_REQUEST_TEMPLATE.md`](./.github/PULL_REQUEST_TEMPLATE.md) | Default PR description scaffolding: linked issue, description, test plan, checklist, breaking-change notice. | A contributor opens a PR and the body is pre-populated, so they don't forget to link the issue or check the test boxes. |
| [`.github/ISSUE_TEMPLATE/config.yml`](./.github/ISSUE_TEMPLATE/config.yml) | Disables blank issues and adds curated "contact links" (Discussions, security advisory, status, support). | A user clicks "New issue" and is steered toward Discussions for questions and Security Advisories for vulns — the issue tracker stays clean. |
| [`.github/ISSUE_TEMPLATE/01-bug_report.yml`](./.github/ISSUE_TEMPLATE/01-bug_report.yml) | Modern YAML **issue form** for bug reports — requires repro steps, expected/actual, version, OS. | A user reports a regression; the form refuses to submit without a version and steps to reproduce, saving back-and-forth triage. |
| [`.github/ISSUE_TEMPLATE/02-feature_request.yml`](./.github/ISSUE_TEMPLATE/02-feature_request.yml) | YAML form for feature proposals — problem-first, with priority dropdown. | A user wants a new flag; the form makes them describe the *problem* before the solution, leading to better discussion. |
| [`.github/ISSUE_TEMPLATE/03-documentation.yml`](./.github/ISSUE_TEMPLATE/03-documentation.yml) | YAML form for docs-only issues with location field and change-type dropdown. | A reader spots a typo in the README and files a tightly scoped docs issue in 30 seconds. |
| [`.github/ISSUE_TEMPLATE/04-question.yml`](./.github/ISSUE_TEMPLATE/04-question.yml) | YAML form for questions, with a soft nudge toward Discussions. | A user has a narrow usage question that doesn't fit Discussions; the form captures what they've already tried. |
| [`.github/ISSUE_TEMPLATE/05-test_case.yml`](./.github/ISSUE_TEMPLATE/05-test_case.yml) | YAML form to propose a new test case (unit/integration/e2e/perf/security/regression). | A contributor finds an untested edge case and proposes the exact test to add before writing the PR. |
| [`.github/DISCUSSION_TEMPLATE/ideas.yml`](./.github/DISCUSSION_TEMPLATE/ideas.yml) | Structured template for the **Ideas** discussion category: pitch, motivation, details, alternatives. | A user has a half-baked feature idea and posts it to Discussions instead of opening a premature feature-request issue. |
| [`.github/DISCUSSION_TEMPLATE/q-and-a.yml`](./.github/DISCUSSION_TEMPLATE/q-and-a.yml) | Structured template for the **Q&A** category: question, context, environment. | A user asks "how do I configure X with Y?" and the structured answer becomes a searchable reference for the next person. |
| [`.github/DISCUSSION_TEMPLATE/show-and-tell.yml`](./.github/DISCUSSION_TEMPLATE/show-and-tell.yml) | Template for users to share what they've built with the project. | Someone built a side project on top of one of my libraries and posts a writeup — great social proof + roadmap signal. |

### This-repo-only files (not inherited)

| File | Purpose | Example use case |
| ---- | ------- | ---------------- |
| [`.github/copilot-instructions.md`](./.github/copilot-instructions.md) | Default style and behavior guidance for GitHub Copilot / Copilot Chat. **Inherits per-repo only**, not across the org — but I keep it here as a canonical template to copy. | When I bootstrap a new repo, I copy this file in so Copilot suggestions match my house style from day one. |
| [`.github/dependabot.yml`](./.github/dependabot.yml) | Dependabot config for *this* repo (monthly GitHub Actions updates). Dependabot config is **not inherited** across repos. | Dependabot opens a monthly PR bumping the actions versions used by the workflows in this repo. |
| [`.github/workflows/`](./.github/workflows/) | GitHub Actions workflows for *this* repo only. Workflows in `.github` are **not** auto-applied to other repos (use [starter workflows](https://docs.github.com/actions/using-workflows/creating-starter-workflows-for-your-organization) for that, which require an org account). | A future workflow here could lint markdown or validate the issue-form YAML on every PR. |
| [`profile/README.md`](./profile/README.md) | **Organization** profile page source (`<orgname>/.github/profile/README.md`). For *personal* accounts the profile page comes from `<username>/<username>/README.md` instead — see the hierarchy section below. This file is kept here as a synced mirror of [`carlosferreyra/carlosferreyra`](https://github.com/carlosferreyra/carlosferreyra) and would only auto-render if this account became an org. | Kitsune Studios (an org) would render its profile at `KitsuneStudios/.github/profile/README.md`; Carlos's personal profile at `github.com/carlosferreyra` renders from the separate `carlosferreyra/carlosferreyra` repo instead. |
| [`LICENSE`](./LICENSE) | MIT license for the contents of *this* repo. **License is not inherited** as a fallback — each repo needs its own. | Allows others to reuse the templates and docs in this repo under MIT. |
| [`README.md`](./README.md) | This file. Index + GitHub docs cheatsheet. | Future-me opens the repo and immediately remembers what every file does. |

---

## 📚 GitHub `.github` repo cheatsheet

Distilled from the official GitHub docs so you don't have to re-read them.
Each bullet is a fact you can act on.

### How fallback inheritance works

- A repo named **`.github`** under a user *or* organization is "magic": its
  community health files act as defaults for every **other public** repo
  owned by the same account.
- A file is inherited **only if** the consuming repo does **not** define its
  own copy of that file in any of: the repo root, the `docs/` folder, or the
  `.github/` folder.
- Inheritance is **all-or-nothing per file** — there is no merging. If a repo
  has its own `CONTRIBUTING.md`, it fully replaces the one here.
- Inherited files are **not visible** in the consuming repo's file tree, but
  GitHub surfaces them in the same UI spots (Community Standards, "New
  issue", Sponsor button, etc.).
- Fallbacks **don't apply to forks** of other people's repos.
- Fallbacks **don't apply to private repos** unless you have GitHub Enterprise
  with the right setting.

### What can be a fallback

| File | Allowed locations in `.github` repo | Notes |
| ---- | ----------------------------------- | ----- |
| `CODE_OF_CONDUCT.md` | root, `docs/`, `.github/` | Linked in Community Standards. |
| `CONTRIBUTING.md` | root, `docs/`, `.github/` | Shown when contributors open a PR. |
| `GOVERNANCE.md` | root, `docs/`, `.github/` | Optional. Surfaced in Community Standards. |
| `SECURITY.md` | root, `docs/`, `.github/` | Linked from the **Security** tab. |
| `SUPPORT.md` | root, `docs/`, `.github/` | Linked from "I have a question" UI. |
| `FUNDING.yml` | **`.github/` only** | Powers the Sponsor button. |
| `ISSUE_TEMPLATE/*` | **`.github/ISSUE_TEMPLATE/` only** | Both `.md` legacy and `.yml` issue forms. |
| `PULL_REQUEST_TEMPLATE.md` *or* `PULL_REQUEST_TEMPLATE/*.md` | **`.github/`** | Single file or a directory of templates (selected via `?template=name.md` query). |
| `DISCUSSION_TEMPLATE/*.yml` | **`.github/DISCUSSION_TEMPLATE/` only** | One YAML file **per category slug**. |
| `config.yml` (issue template chooser) | `.github/ISSUE_TEMPLATE/config.yml` | Disables blank issues, adds contact links. |

### What is **NOT** inherited

- `LICENSE` — every repo needs its own.
- `README.md` — except `profile/README.md`, which is the user/org profile.
- `.github/workflows/*.yml` — workflows run only in the repo they live in.
  For org-wide reusable workflows, use **starter workflows** under
  `workflow-templates/` in the **org-level** `.github` repo (orgs only, not
  user accounts).
- `dependabot.yml` — Dependabot config is per-repo.
- `CODEOWNERS` — per-repo.
- `.gitattributes`, `.gitignore`, `CITATION.cff` — per-repo.
- Repository **labels**, **branch protection**, **secrets**, **rulesets** —
  configured at the repo or org level, not via this file tree.

### Profile README — full hierarchy

The path that renders at `github.com/carlosferreyra` depends on whether the
account is a **personal user** or an **organization**. They use different
mechanisms.

#### Personal user account (how `carlosferreyra` works today)

| Candidate path | Does it render as the profile page? |
| -------------- | ----------------------------------- |
| `carlosferreyra/carlosferreyra/README.md` | ✅ **Yes** — the only path GitHub reads for a personal profile. |
| `carlosferreyra/carlosferreyra/profile/README.md` | ❌ No — GitHub only looks at the **root** README of the profile repo. |
| `carlosferreyra/.github/profile/README.md` *(this file)* | ❌ No — `profile/README.md` inside a `.github` repo is for **organizations only**, not personal accounts. |
| `carlosferreyra/.github/README.md` | ❌ No — that's just this repo's own README, not a profile. |

**Rule for personal accounts:** create a public repo named **exactly** your
username (`carlosferreyra/carlosferreyra`), put `README.md` at the **root**.
GitHub renders it above your pinned repos at `github.com/<username>`. No other
path triggers this behavior.

#### Organization account (how it would work for e.g. `KitsuneStudios`)

| Candidate path | Does it render as the org profile page? |
| -------------- | --------------------------------------- |
| `KitsuneStudios/.github/profile/README.md` | ✅ **Yes** — the only path GitHub reads for a public org profile. |
| `KitsuneStudios/.github/README.md` | ❌ No — that's the `.github` repo's own README. |
| `KitsuneStudios/KitsuneStudios/README.md` | ❌ No — orgs cannot create a repo named the same as the org (the username namespace is reserved). |

**Rule for organizations:** in the org's `.github` repo, put
`profile/README.md` on the default branch and make the repo public.

#### Summary table

| What you see at `github.com/X` | Source file |
| ------------------------------- | ----------- |
| Personal user profile (`X` = username) | `X/X/README.md` *(root of the profile repo)* |
| Organization profile (`X` = org) | `X/.github/profile/README.md` |

#### Why `profile/README.md` still lives in this repo

- It is a **synced copy** of `carlosferreyra/carlosferreyra/README.md` — a
  single source of truth to copy from when updating the real profile repo.
- If `carlosferreyra` is ever converted to or mirrored as an org, the file is
  already in the right place.
- It does **not** render anywhere automatically for a personal account.

#### Other profile README facts

- The profile repo (`carlosferreyra/carlosferreyra`) and its README must be
  **public** to show on the profile page.
- The README renders **above** pinned repos and the contribution graph.
- Supports all GitHub-flavored Markdown, HTML, and third-party image-based
  stats cards (e.g., `github-readme-stats`, `github-readme-activity-graph`).
- Relative links (e.g., `resume/carlos-ferreyra.pdf`) resolve against the
  **profile repo** (`carlosferreyra/carlosferreyra`), not this `.github` repo.
  A copy of the same README here would have broken relative links unless they
  are converted to absolute URLs.

### Issue forms (`.yml`) vs. legacy templates (`.md`)

- **YAML forms** (`name`, `description`, `body:`) render as structured form
  fields with validation. Preferred for new templates.
- **Markdown templates** still work and are simpler for free-form issues.
- File order in `.github/ISSUE_TEMPLATE/` controls display order — prefix
  with `01-`, `02-`, … to sort.
- `config.yml` controls whether blank issues are allowed and adds
  "contact links" shown on the chooser page.

### PR templates: file vs. directory

- A single `.github/PULL_REQUEST_TEMPLATE.md` is auto-applied to every PR.
- A directory `.github/PULL_REQUEST_TEMPLATE/` lets you have many templates,
  each picked via the URL query string:
  `?template=feature.md&quick_pull=1`.

### Discussion templates

- One YAML file per **category slug** in `.github/DISCUSSION_TEMPLATE/`
  (e.g., `ideas.yml` matches the "Ideas" category).
- The category must already exist in the repo's Discussions settings — the
  template doesn't create it.

### Funding (`FUNDING.yml`)

- Lives only at `.github/FUNDING.yml`.
- Supports keys: `github`, `patreon`, `open_collective`, `ko_fi`, `tidelift`,
  `community_bridge`, `liberapay`, `issuehunt`, `lfx_crowdfunding`,
  `polar`, `buy_me_a_coffee`, `thanks_dev`, and `custom` (array of URLs).
- Each value is either a username or a URL depending on the platform.

### Copilot instructions

- A repo's `.github/copilot-instructions.md` is **auto-loaded** by GitHub
  Copilot Chat for that repo. **Not inherited** across repos via this
  `.github` repo — keep it as a copy-paste source of truth.
- Path-scoped instructions can live under `.github/instructions/*.md` with
  YAML front-matter `applyTo:` patterns (newer Copilot feature).

### Dependabot

- `.github/dependabot.yml` is per-repo. Define one `updates:` entry per
  ecosystem (`github-actions`, `npm`, `pip`, `gomod`, `docker`, …).
- Use `schedule.interval: monthly` for low-churn repos like this one.
- Use `groups:` to bundle related updates into one PR.

### Useful GitHub docs links

- [About community health files](https://docs.github.com/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Managing your profile README](https://docs.github.com/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [Configuring issue templates](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
- [Syntax for issue forms](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [Discussion category forms](https://docs.github.com/discussions/managing-discussions-for-your-community/managing-category-forms-for-discussions)
- [About FUNDING files](https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository)
- [Adding repository custom instructions for Copilot](https://docs.github.com/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot)
- [Dependabot configuration options](https://docs.github.com/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot-yml-file)

---

## 🤝 How to use this repo from another repo of mine

For a brand-new repo:

1. Create the repo (public).
2. **Don't** add a CODE_OF_CONDUCT, CONTRIBUTING, SECURITY, SUPPORT, FUNDING,
   or templates — they'll be inherited from here automatically.
3. Add a per-repo `LICENSE` and `README.md` (these are not inherited).
4. Add a per-repo `.github/dependabot.yml` if needed.

To override a fallback for a specific repo, just commit a file with the same
name to that repo's root, `docs/`, or `.github/`.

## 📝 License

The contents of this repository are released under the [MIT License](./LICENSE).
