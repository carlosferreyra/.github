# GitHub Copilot Instructions

These are the default Copilot / Copilot Chat instructions applied to any
repository owned by [@carlosferreyra](https://github.com/carlosferreyra) that
does not ship its own `.github/copilot-instructions.md`. Repository-level files
take precedence.

## General principles

- Prefer **clarity and correctness** over cleverness. Generated code should
  read like it was written by a careful human.
- **Match the surrounding code style.** If the file uses 2-space indentation
  and single quotes, do the same — do not reformat.
- **Do not invent APIs.** If you are unsure whether a function, flag, or
  import exists, ask or leave a TODO rather than guessing.
- **Small, focused changes.** Avoid unrelated refactors, whitespace churn, or
  reordering imports when the task does not require it.

## Code style

- Follow the project's linter / formatter. If none is configured, default to:
  - **JavaScript / TypeScript**: Prettier defaults, ESLint recommended rules.
  - **Python**: Black (88-col), Ruff, type hints on public functions.
  - **Go**: `gofmt`, `go vet` clean.
  - **Shell**: `shellcheck` clean, `set -euo pipefail` in scripts.
- Use descriptive identifiers; avoid single-letter names outside tight loops.
- Prefer pure functions and early returns over deep nesting.
- Do not add comments that restate the code. Write comments when the *why*
  is non-obvious.

## Testing

- When you add or change behavior, add or update tests.
- Prefer fast, deterministic unit tests. Use integration tests for cross-
  boundary behavior.
- Mirror the project's existing test framework (Jest, Vitest, Pytest, Go
  test, etc.).

## Security

- Never hard-code secrets, tokens, or credentials — use env vars or a secret
  manager.
- Validate and sanitize all external input at trust boundaries.
- Prefer parameterized queries; never build SQL via string concatenation.
- Avoid dependencies that are unmaintained or have open critical CVEs.

## Commits and PRs

- Use [Conventional Commits](https://www.conventionalcommits.org/) for
  commit messages.
- Reference related issues in PR descriptions (`Closes #123`).
- Keep PRs focused; split unrelated changes into separate PRs.

## When in doubt

Ask a clarifying question before making large or ambiguous changes.
