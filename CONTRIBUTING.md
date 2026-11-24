# Contributing

Thanks for taking the time to contribute! This guide applies to every repository under [@kishor-rajbanshi](https://github.com/kishor-rajbanshi) unless the repository has its own `CONTRIBUTING.md`.

## Reporting bugs

1. Search [existing issues](../../issues) first — it may already be reported.
2. Open a new issue using the **Bug report** form and include steps to reproduce, expected vs actual behaviour, and your environment.

Security problems should **not** be reported as issues — see [SECURITY.md](SECURITY.md).

## Suggesting features

Open an issue using the **Feature request** form. Describe the problem you want solved before the solution you have in mind.

## Pull requests

1. Fork the repository and create a branch from the default branch:
   ```sh
   git switch -c feat/short-description
   ```
2. Keep changes focused — one logical change per pull request.
3. Follow the existing code style and run the project's linters and tests before pushing.
4. Write commit messages in the [Conventional Commits](https://www.conventionalcommits.org) style, for example:
   ```
   feat: add queue retry option
   fix(deploy): handle missing .env file
   ```
5. Open the pull request, fill in the template, and link related issues (`Closes #123`).

For large or breaking changes, please open an issue to discuss the approach first.

## Code of Conduct

By participating you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
