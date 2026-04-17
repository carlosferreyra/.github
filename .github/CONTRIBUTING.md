# Contributing

Thanks for taking the time to contribute! This document describes the baseline
expectations for contributing to any repository owned by
[@carlosferreyra](https://github.com/carlosferreyra) that does not ship its own
`CONTRIBUTING.md`. Individual repositories may override or extend these rules.

## Code of Conduct

This project and everyone participating in it is governed by the
[Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you are expected to
uphold this code. Please report unacceptable behavior to
[contact@carlosferreyra.me](mailto:contact@carlosferreyra.me).

## Ways to contribute

- **Report a bug** using the [bug report template](./ISSUE_TEMPLATE/01-bug_report.yml).
- **Request a feature** using the [feature request template](./ISSUE_TEMPLATE/02-feature_request.yml).
- **Improve documentation** using the [documentation template](./ISSUE_TEMPLATE/03-documentation.yml).
- **Ask a question** via [Discussions](https://github.com/orgs/community/discussions) or the [question template](./ISSUE_TEMPLATE/04-question.yml).
- **Submit a pull request** following the workflow below.

## Development workflow

1. **Fork** the repository and clone your fork locally.
2. **Create a branch** from `main` using a descriptive name:
   - `feat/<short-description>` for new features
   - `fix/<short-description>` for bug fixes
   - `docs/<short-description>` for documentation-only changes
   - `chore/<short-description>` for tooling, CI, deps
3. **Make your changes**. Keep commits small and focused.
4. **Write or update tests** when behavior changes.
5. **Run the project's lint and test suites** locally before pushing.
6. **Open a pull request** against `main` using the
   [pull request template](./PULL_REQUEST_TEMPLATE.md). Link any related issue
   with `Closes #123`.

## Commit messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) spec:

```
<type>(<optional scope>): <short summary>

<optional body>

<optional footer>
```

Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`,
`build`, `ci`, `chore`, `revert`.

## Pull request checklist

Before requesting review, confirm:

- [ ] The branch is up to date with `main`.
- [ ] All tests and linters pass locally.
- [ ] New code is covered by tests where practical.
- [ ] Public API changes are documented.
- [ ] The PR description explains the *why*, not just the *what*.
- [ ] Related issues are linked.

## Review process

- A maintainer will review your PR as soon as possible.
- Address review feedback in new commits; do not force-push over reviewed
  commits unless asked.
- Once approved and CI is green, a maintainer will merge the PR. Prefer
  squash-merge unless the commit history is intentionally curated.

## License

By contributing, you agree that your contributions will be licensed under the
same terms as the repository (typically MIT — see the repository's `LICENSE`).
