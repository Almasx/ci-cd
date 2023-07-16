# UNIT DEMO CRA

This repository contains the source code for Project Name. It uses automated checks, tests, and a release process. Below are details of these processes:

## Commit Message Guidelines

We have very precise rules over how our git commit messages can be formatted. This leads to more readable messages that are easy to follow when looking through the project history.

We use `commitlint` to lint commit messages. Commit messages should follow the [Conventional Commits specification](https://www.conventionalcommits.org/). The commit message should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## Continuous Integration (CI)

We use GitHub Actions for Continuous Integration. On each commit to a Pull Request, the following actions are performed:

- Code is checked out
- Node.js is set up
- Dependencies are installed
- Tests are run

If any of these steps fail, the commit is marked as failed.

## Release Process

The release process is automated with GitHub Actions. When a new tag matching the `v*` pattern is pushed, the following actions are performed:

- Code is checked out
- Node.js is set up
- Dependencies are installed
- Changelog is generated with `standard-version`
- GitHub release is created
- Code is deployed to GitHub Pages

The release version matches the release tag, and the changelog is generated from the commit history since the last release tag.
