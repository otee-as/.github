# Contributing to otee-as repositories

These rules apply to every repository in the organization unless the
repository's own `CONTRIBUTING.md` says otherwise.

## Branches

- One branch per issue. Name: `<issue-key>-short-description`.
- Never push to `main`. Open a pull request.
- A production hotfix goes on a maintenance line named `N.N.x` (example:
  `1.16.x`), cut from the release tag with the repository's hotfix script.
  The same fix goes on `main` by `git cherry-pick -x`, main first as the
  rule. A line is never merged into `main`.

## Commits

- [Conventional Commits](https://www.conventionalcommits.org/):
  `type(scope): description`. Types: `feat`, `fix`, `docs`, `chore`, `ci`,
  `refactor`, `revert`. A breaking change: `feat(scope)!: ...`.
- Every commit on a pull request is a Conventional Commit. Release tooling
  reads the commits. commit-lint checks them on the pull request.
- Commits are signed. The organization requires it on `main`.
- On a maintenance line, only `fix:` and `revert:` commits.

## Pull requests

- The PR template gives the sections. Fill every section. Write `None.`
  rather than delete one.
- One approval from a person who did not make the last push. Merge with a
  merge commit. Resolve every review thread.

## Writing

Documentation, PR text and commit messages use Simplified Technical
English: short sentences, one fact each, active voice, the same word for the
same thing.

## Decisions

A decision that shapes a repository goes in `docs/adr/` as an Architecture
Decision Record (MADR format).

## CI

Call the shared reusable workflows. Pin to the moving major tag (`@v3`).
Never `@main`.
