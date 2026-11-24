# .github

Default community health files, shared workflows and scripts for all repositories under [@kishor-rajbanshi](https://github.com/kishor-rajbanshi).

## Community health files

GitHub uses these files for any public repository of this account that does not define its own:

| File | Purpose |
| --- | --- |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Expected behaviour in issues, PRs and discussions |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to report bugs, propose changes and open pull requests |
| [`SECURITY.md`](SECURITY.md) | How to report a vulnerability privately |
| [`SUPPORT.md`](SUPPORT.md) | Where to ask for help |
| [`ISSUE_TEMPLATE/`](ISSUE_TEMPLATE) | Bug report and feature request forms |
| [`PULL_REQUEST_TEMPLATE.md`](PULL_REQUEST_TEMPLATE.md) | Pull request checklist |

A repository overrides any of these by adding its own copy (in its root, `.github/` or `docs/` folder).

> [!NOTE]
> `LICENSE` files are not inherited — each repository needs its own.

## Shared workflows

Reusable workflows live in [`.github/workflows/`](.github/workflows) and are called from other repositories with:

```yaml
jobs:
  example:
    uses: kishor-rajbanshi/.github/.github/workflows/<workflow>.yml@main
```
