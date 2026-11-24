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

Reusable workflows live in [`.github/workflows/`](.github/workflows). Each file starts with a ready-to-copy caller example.

| Workflow | What it does |
| --- | --- |
| [`laravel-tests.yml`](.github/workflows/laravel-tests.yml) | Runs `php artisan test` across a PHP version matrix, building front-end assets when `package.json` exists |
| [`laravel-deploy.yml`](.github/workflows/laravel-deploy.yml) | Builds Composer (`--no-dev`) and assets on the runner, uploads with rsync over SSH, then runs migrations, `optimize` and `reload` on the server |
| [`upstream-sync.yml`](.github/workflows/upstream-sync.yml) | Merges an upstream repository (e.g. `laravel/laravel`) into a fork; pushes clean merges, opens a PR on conflicts |
| [`dependabot-auto-merge.yml`](.github/workflows/dependabot-auto-merge.yml) | Approves and auto-merges Dependabot patch/minor updates |

```yaml
jobs:
  tests:
    uses: kishor-rajbanshi/.github/.github/workflows/laravel-tests.yml@main
```

Callers use `@main`, so changes here reach every repository immediately — keep them backwards compatible.

## Shared actions

| Action | What it does |
| --- | --- |
| [`actions/build-assets`](actions/build-assets/action.yml) | Detects bun / pnpm / yarn / npm from the lockfile, installs and runs `build` |

```yaml
- uses: kishor-rajbanshi/.github/actions/build-assets@main
```
