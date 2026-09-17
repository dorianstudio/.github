# dorianstudio/.github

Organization-wide defaults for GitHub repositories in the dorianstudio organization.

Files in this repository are used automatically by every repository in the organization that does not
have its own copy:

- `.github/ISSUE_TEMPLATE/` – markdown issue templates for bug reports, feature requests, tasks, and
  security issues
- `PULL_REQUEST_TEMPLATE.md` – pull request body template
- `CONTRIBUTING.md` – contribution guide, including our Conventional Commits standard
- `SECURITY.md` – how to report a vulnerability

A repository's own file always takes precedence over the default here. To use the organization
defaults, delete the repository-level copy.

Not everything is inherited. `CODEOWNERS` and GitHub Actions workflows must live in each repository;
this repository cannot supply them. This repository is public because GitHub requires that for the
defaults to apply to private repositories, so do not add internal hostnames, credentials, or customer
information here.
