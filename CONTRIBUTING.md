# Contributing to otee-as repositories

These rules apply to every repository in the organization unless the
repository's own `CONTRIBUTING.md` says otherwise. They are short on purpose.
The reason for each rule is in the linked document.

## Branches

- One branch per Linear issue. Name: `ops-NNNN-short-description` (the
  issue key, then what the branch does).
- Never push to `main`. Open a pull request.
- Hotfixes for production go on a maintenance line named `N.N.x`
  (example: `1.16.x`), cut from the release tag. `hotfix/**` is the legacy
  shape and makes no release. Make the line with the script, not by hand:
  [tg-devops-gh/docs/hotfix-line.md](https://github.com/otee-as/tg-devops-gh/blob/main/docs/hotfix-line.md).

## Commits

- [Conventional Commits](https://www.conventionalcommits.org/):
  `type(scope): description`. Types: `feat`, `fix`, `docs`, `chore`, `ci`,
  `refactor`, `revert`. A breaking change: `feat(scope)!: ...`.
- The pull request title is the squash commit. Release tooling reads it. A
  title that is not a Conventional Commit skips the release, and nothing
  tells you.
- Commits are signed. The organization requires it on `main`.
- On a maintenance line, only `fix:` and `revert:` commits.

## Pull requests

- The PR template gives the sections. Fill every section. Write `None.`
  rather than delete one.
- One approval from a person who did not make the last push. Merge with a
  merge commit. Resolve every review thread.
- Automation (`otee-release-bot`, `otee-kargo`) and the `devsecops` team can
  bypass the review rules. Every bypass is in the audit log. Use it for an
  incident, not for speed.

## Writing

Documentation, PR text and commit messages use Simplified Technical
English: short sentences, one fact each, active voice, the same word for the
same thing. A reader who is tired, or not a native speaker, must understand
it at the first reading.

## Decisions

A decision that shapes a repository goes in `docs/adr/` as an Architecture
Decision Record (MADR format). Fleet-wide decisions are in
[tg-devops-dev/docs/adr](https://github.com/otee-as/tg-devops-dev/tree/main/docs/adr);
GitHub org governance in
[tg-devops-gh/docs/adr](https://github.com/otee-as/tg-devops-gh/tree/main/docs/adr).

## CI

- Call the shared reusable workflows from
  [tg-devops-gh](https://github.com/otee-as/tg-devops-gh#shared-reusable-workflows).
  Pin to the moving major tag (`@v3`). Never `@main`.
- Starter workflows for the common cases are in this repository under
  `workflow-templates/`; they appear in the Actions tab of every repository.

## Infrastructure repositories (`tg-devops-*`)

- Merged HCL is not applied HCL. The tree is applied by hand. Say in the PR
  whether you applied it.
- Ask before `apply` or `destroy` on anything that is not yours.
