# .github Configuration Repository

This repository contains GitHub-specific configuration files and templates that can be used across multiple repositories in the organization.

## Repository Structure

```
.github/
├── FUNDING.yml                      # Funding and sponsorship configuration
├── ISSUE_TEMPLATES/                 # Templates for creating new issues
│   ├── 01-bug_report.yml           # Template for bug reports
│   └── 02-feature_request.yml         # Template for feature requests
└── PULL_REQUEST_TEMPLATES/         # Templates for pull requests
    └── pull_request_template.md    # Default pull request template
```

## Contents

### Issue Templates
- **Bug Report Template**: Structured template for reporting bugs
- **Feature Request Template**: Template for proposing new features

### Pull Request Template
A standardized template for creating pull requests, ensuring all necessary information is provided.

### Funding Configuration
Configuration for GitHub Sponsors and other funding platforms.

## Usage

This repository serves as a central configuration hub for GitHub-specific settings and templates. The templates and configurations here will be automatically applied to repositories within the organization.

## How It Works

When you have a `.github` repository in your organization or user account, GitHub automatically applies its contents as defaults to all your other repositories. Here's an example:

```
Your GitHub Account/Organization
├── .github (this repository)
│   ├── ISSUE_TEMPLATES/
│   │   └── feature_request.yml
│   └── PULL_REQUEST_TEMPLATES/
│       └── pull_request_template.md
│
├── project-a/
│   └── (inherits templates from .github)
│
└── project-b/
    └── (inherits templates from .github)
```

For instance, when someone creates a new issue in `project-a` or `project-b`, they'll automatically see the templates defined in this `.github` repository. If a repository has its own `.github` folder with templates, those will take precedence over these default ones.

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

## Code of Conduct

Please review our [Code of Conduct](CODE_OF_CONDUCT.md) to understand the community guidelines and expectations.
