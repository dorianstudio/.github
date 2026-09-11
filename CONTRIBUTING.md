# Contributing

These guidelines apply to every repository in the dorianstudio organization unless a repository's own
`CONTRIBUTING.md` says otherwise.

## Reporting issues

Open an issue using one of the forms: **Bug report**, **Feature request**, **Task / chore**, or
**Security issue**. Blank issues are disabled. Each form ends with an optional R&D section; fill it in
whenever the work involves technical uncertainty so the record exists from the start.

Use the **Security issue** form for internal security findings. For an active credential leak or customer
data exposure, do not open an issue at all; follow [SECURITY.md](SECURITY.md) so the report reaches as
few people as possible.

## Branches

Branch from the repository's default branch. Name branches `type/short-description`, using the same
types as commits, for example `fix/omr-parse-error` or `feat/shipping-tracking-webhook`.

## Commits

We use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
type(scope): short summary

optional body

optional footer, e.g. Closes #123
```

Allowed types:

| Type       | Use for                                              |
| ---------- | ---------------------------------------------------- |
| `feat`     | New functionality                                    |
| `fix`      | Bug fixes                                            |
| `chore`    | Maintenance with no production code change           |
| `docs`     | Documentation only                                   |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `perf`     | Performance improvement                              |
| `test`     | Adding or correcting tests                           |
| `build`    | Build system or dependency changes                   |
| `ci`       | CI configuration                                     |
| `revert`   | Reverting a previous commit                          |

Scope is optional and names the area touched, for example `feat(shipping): add UPS tracking sync`.
Mark breaking changes with `!` after the type or scope, and explain them in the footer:

```
feat(api)!: remove v1 order endpoints

BREAKING CHANGE: clients must migrate to /v2/orders.
```

Pull request titles use the same format, because we squash-merge and the PR title becomes the commit
message on the default branch.

## Pull requests

- Fill in the pull request template.
- Keep each PR focused on one change. Split unrelated work into separate PRs.
- Link the issue it resolves with `Closes #123`.
- Request review from `@dorianstudio/software-development`.
- CI must pass before merge.
- Squash-merge, keeping the Conventional Commits title.

## Code style

Follow the linter and formatter configuration checked into each repository. Python repositories use
the configured tools (typically `ruff` or `black`); JavaScript repositories use the configured
`eslint` and `prettier` settings. Run them before opening a PR.
