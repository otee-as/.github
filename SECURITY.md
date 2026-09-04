# Security policy

This policy applies to every repository in the otee-as organization.

## Report a vulnerability

Do not open a public issue. Do not put details in a pull request.

- Members of the organization: open a Linear issue in the OPS project
  with the `security` label, or contact the DevSecOps lead
  (`@jp-devops-ot`) or the CTO (`@radek-otee`) directly.
- External reporters: use the contact on <https://otee.com>.

Include: the repository, the version or commit, the steps to reproduce,
and the impact you expect. We confirm receipt within two working days.

## What happens next

1. We confirm the report and assess severity.
2. We fix it on a maintenance line if it affects a released version, and on
   `main`.
3. We tell you when the fix is released. We credit you if you want that.

## Scope

- All repositories in the organization, including forks we maintain.
- Secrets in git history: report them; we rotate the secret first, then
  clean the history.

## Related

- The organization's security policies live in the `otee-cybersec-policy`
  repository (members only).
- Dependency alerts are enabled on every managed repository.
