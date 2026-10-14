<!--
Title: a Conventional Commit - `feat(scope): ...`, `fix(scope): ...`,
`chore(scope): ...`. The squash title IS the commit; release-please reads it.
A non-conventional title skips the release silently (see README).

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

<!-- What the AUTHOR did before asking for review. Merging HCL under live/
does NOT apply it (live/org.hcl) - say whether it was applied. -->

- [ ] `terragrunt plan` is clean on every changed unit (as the Admin App).
- [ ] Applied: <!-- "not yet" / "yes, on YYYY-MM-DD" / "n/a, no live change" -->
- [ ] `scripts/check-github-drift.py` shows no new violation.

## Acceptance Criteria

<!-- What a REVIEWER can check on GitHub after merge + apply. Tick after. -->

- [ ]

## Risk and rollback

<!-- Blast radius if this is wrong: which repos, which people, which bots.
Rollback: revert + apply, `enforcement = "disabled"`, restore a v4 block.
Anything that cannot be undone (team deletion, state rm)? -->

- **Blast radius:**
- **Rollback:**

## Security

<!-- This repo is permissions. Any of these must be named in Changes and
justified in the unit comment or an ADR. -->

- [ ] No new bypass actor, App permission, team grant, or secret.
- [ ] If there is one: it is listed in Changes, with the reason.

## Out of scope

<!-- Adjacent work a reader may expect here but that is not in this PR. -->
