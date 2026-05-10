# Contributing Guide

Thank you for your interest in contributing. This guide describes the general workflow, conventions, and expectations that apply to repositories under this account. Project-specific guides, when present, take precedence over this document.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Reporting Issues](#reporting-issues)
- [Submitting Changes](#submitting-changes)
- [Branching Model](#branching-model)
- [Commit Convention](#commit-convention)
- [Pull Request Process](#pull-request-process)
- [Code Review](#code-review)
- [Coding Standards](#coding-standards)
- [Documentation](#documentation)
- [Security Reports](#security-reports)
- [Licensing](#licensing)

## Code of Conduct

All contributors are expected to behave professionally and respectfully. Personal attacks, harassment, and discriminatory language are not tolerated. By participating, you agree to uphold a welcoming environment for everyone.

## Ways to Contribute

There are several ways to help, regardless of experience level:

- Reporting bugs and reproducible issues
- Proposing or implementing new features
- Improving documentation, examples, and tutorials
- Reviewing pull requests and providing constructive feedback
- Triaging issues and helping reproduce reports
- Suggesting tooling, performance, or security improvements

## Reporting Issues

Before opening a new issue, please:

1. Search existing issues to avoid duplicates.
2. Check the documentation and recent release notes.
3. Reproduce the problem on the latest released version when possible.

When opening an issue, use the relevant issue template and include:

- A clear, descriptive title
- The version, commit hash, or release tag affected
- Steps to reproduce, expected behavior, and actual behavior
- Relevant logs, stack traces, or screenshots
- Environment information (OS, runtime version, etc.)

## Submitting Changes

The general workflow is:

1. **Fork** the repository and clone your fork locally.
2. **Create a branch** from the default branch (`main` or `master`).
3. **Make your changes** with clear, atomic commits.
4. **Add or update tests** for behavioral changes.
5. **Run the project's checks** (formatting, linting, tests) locally.
6. **Open a pull request** against the upstream default branch.

Small, focused pull requests are preferred over large, sweeping changes.

## Branching Model

- `main` (or `master`) is the default branch and must always be in a releasable state.
- Feature branches use the prefix `feat/<short-description>`.
- Bug fix branches use the prefix `fix/<short-description>`.
- Documentation branches use the prefix `docs/<short-description>`.
- Long-running release branches, when used, follow `release/<version>`.

## Commit Convention

Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/) specification and **must be written in English**.

Format:

```
<type>(<optional scope>): <short summary>

<optional body>

<optional footer>
```

Allowed types:

| Type | Purpose |
| --- | --- |
| `feat` | A new feature |
| `fix` | A bug fix |
| `refactor` | A code change that neither fixes a bug nor adds a feature |
| `doc` | Documentation-only changes |
| `perf` | A performance improvement |
| `style` | Formatting or stylistic changes that do not affect behavior |
| `test` | Adding or correcting tests |
| `chore` | Build, tooling, or auxiliary changes |
| `ci` | Continuous integration changes |
| `revert` | Reverting a previous commit |

Append `!` after the type or include `BREAKING CHANGE:` in the footer to indicate a breaking change. Reference issues with `Closes #123` or `Refs #123` when applicable.

## Pull Request Process

1. Ensure the branch is up to date with the target branch.
2. Verify that all CI checks pass and pre-commit hooks have been run.
3. Provide a descriptive title that follows the commit convention; the title is used for semantic PR validation.
4. Fill out the pull request template, including motivation, summary, and testing notes.
5. Link related issues and design documents.
6. Mark the pull request as **draft** while still in progress.
7. Request review only when ready and self-review has been completed.

Pull requests are typically merged using **squash merge** to keep history linear.

## Code Review

- Address all review comments or explain why a change is not needed.
- Keep discussions technical, focused, and respectful.
- Reviewers should respond within a reasonable time and indicate when more time is needed.
- Resolve conversations only after the underlying concern has been addressed.

## Coding Standards

- Follow the conventions and tooling defined in the repository (formatters, linters, type checkers).
- Run `pre-commit` hooks before pushing changes when configured.
- Prefer clarity over cleverness; optimize for readability and maintainability.
- Add tests covering the behavior you change or add.
- Avoid unrelated refactors in feature or fix pull requests.

## Documentation

- Update README, inline documentation, and examples whenever public behavior changes.
- Documentation contributions are first-class and are very welcome.
- When adding new features, include a brief usage example where it makes sense.

## Security Reports

Please **do not** report security vulnerabilities through public issues. Refer to [`SECURITY.md`](./SECURITY.md) for the responsible disclosure process.

## Licensing

By contributing, you agree that your contributions will be licensed under the same license as the repository (typically MIT, unless stated otherwise). Ensure that you have the right to submit any code, content, or assets you contribute.
