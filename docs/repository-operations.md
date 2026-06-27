# Repository operations

## Bootstrap a public repository

1. Create the repository under `carlosferreyra` and make it public.
2. Add a project `README.md` and an appropriate `LICENSE`.
3. Do not add shared health files unless the project needs an override.
4. Configure repository features: Issues, Discussions, private vulnerability
   reporting, and sponsorship as applicable.
5. Add project-specific automation such as workflows, Dependabot, CODEOWNERS,
   labels, rulesets, and secrets locally.
6. Check **Insights > Community Standards** and exercise the issue/PR UI.

## Override a default

Copy the relevant source file into the consuming repository and adapt it. For
Markdown health files, use the root, `docs/`, or `.github/`. Use the required
`.github/ISSUE_TEMPLATE/` and `.github/DISCUSSION_TEMPLATE/` paths for forms.

Document why the project differs from the account default. Otherwise the local
copy can drift without maintainers realizing it no longer inherits updates.

## Validate this repository

Run structural checks before merging template changes:

```bash
# YAML syntax
ruby -e 'require "yaml"; ARGV.each { |f| YAML.load_file(f) }' \
  .github/**/*.yml

# Markdown links, using your preferred link checker
npx --yes markdown-link-check README.md docs/*.md

# Inspect the exact propagated file set
find .github -maxdepth 3 -type f | sort
```

Then test the rendered GitHub UI in a public repository without local
overrides. Parsing YAML cannot prove GitHub accepts every form schema or that
repository settings are enabled.

## Publish these docs with GitHub Pages

The `docs/` directory is a plain Markdown source tree and requires no
repository-local build configuration.

1. Configure the existing Pages publishing workflow to use `docs/` as its
   source directory.
2. Use `docs/index.md` as the documentation entry page.
3. Preserve the directory structure so relative `.md` links keep working.
4. Publish with the same plain-Markdown renderer used by the other projects.
5. Verify navigation from the deployed index to every guide.

GitHub Pages configuration and deployment workflows are repository settings;
they are not inherited through this `.github` repository.

## Change review checklist

- Does every file under `.github/` belong to GitHub's supported default set?
- Are shared templates free of labels, teams, assignees, and repository URLs
  that may not exist elsewhere?
- Do policy contacts and response expectations remain accurate?
- Do docs explain both inheritance and local override behavior?
- Do YAML, Markdown links, and Pages rendering pass validation?
- Has a consuming repository been checked after merge?
