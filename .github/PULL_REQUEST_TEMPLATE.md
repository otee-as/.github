<!--
Title: a Conventional Commit - `feat(scope): ...`, `fix(scope): ...`,
`chore(scope): ...`. The squash title IS the commit; release tooling
(release-please / semantic-release) reads it. A non-conventional title
skips the release silently.

Write in Simplified Technical English: short sentences, one fact each,
active voice, the same word for the same thing. Write "None." rather than
delete a section - a missing section makes the reader guess.
-->

## Summary

<!-- What this PR does and why, in 1-3 sentences. Link the Linear issue
(OPS-NNNN) and the ADR if one applies. -->

## Changes

<!-- One bullet per file or theme. Skip what the diff already makes obvious. -->

-

## Verification

<!-- What the AUTHOR did before asking for review: tests run, environment
used, commands, screenshots or logs where they help.
IaC repos: `plan` output, and whether it is APPLIED - merged HCL is not
applied HCL. -->

- [ ]

## Acceptance Criteria

<!-- What a REVIEWER can check after merge (and deploy / apply). Tick after. -->

- [ ]

## Risk and rollback

<!-- Blast radius if this is wrong: which services, environments, repos,
people. Rollback: revert, previous image tag, feature flag, restore a
config. Anything that cannot be undone (migration, state change)? -->

- **Blast radius:**
- **Rollback:**

## Security

<!-- New secrets, IAM / RBAC / team grants, network exposure, new
dependencies, auth paths touched? Name each in Changes with the reason. -->

- [ ] No new secret, permission, network exposure, or dependency.
- [ ] If there is one: it is listed in Changes, with the reason.

## Out of scope

<!-- Adjacent work a reader may expect here but that is not in this PR. -->
