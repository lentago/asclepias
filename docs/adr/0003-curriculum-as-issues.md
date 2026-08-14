# ADR-0003: Curriculum-as-issues, with honesty rules as content policy

**Status:** Accepted (2026-08-12; reconstructed 2026-08-13)

## Context

With the first colleague aboard and five invites pending, member engagement
needed a ladder: each rung a real interaction with a real system, one notch
more agency than the last
([lentago/.github#90](https://github.com/lentago/.github/issues/90)). The
ladder runs L0 (observe) through L4 (own a pattern); everything through L3
works from a browser, and nothing through L3 requires LAN access.

## Decision

Each lab is a **numbered exercise plus a tracked issue**: labs live under
`labs/` with an issue template
([`.github/ISSUE_TEMPLATE/lab-run.yml`](../../.github/ISSUE_TEMPLATE/lab-run.yml)),
so opening a lab-run issue gives each run a durable record, a review thread,
and a finish line. Lab 01's target — the member roster — is append-only by
newcomers, making it the fleet's first practiced PR.

Content is bound by two honesty rules recorded in this repo's own `CLAUDE.md`:
labs must **state access honestly** (a Players-team triage flow is not the
same as a fork-PR flow, is not the same as maintainer-merge access — "a lab
that overstates a newcomer's permissions teaches frustration"), and the manual
admits **no pattern without a link to where it is live** — harvested from the
fleet's verified evidence, never invented.

## Alternatives

- **Retrospective — not considered at the time: a Learning Management System
  (LMS) or third-party course platform.** Worse. It would have added an
  external, likely paid, tool to a lab whose entire pitch is "the systems are
  real" — tracking progress in a platform outside GitHub breaks the
  curriculum-as-issues model's core property, that a lab run *is* a durable,
  reviewable GitHub artifact like every other change in the fleet.
- **Retrospective — not considered at the time: a GitHub Projects board
  tracking lab completion instead of per-run issues.** Lateral. A board is
  reasonable for an at-a-glance view of who's done what, and could still be
  layered on top of the issue-per-run model without replacing it. But on its
  own it would not give each run the durable review thread and finish-line
  record an issue does — it tracks status, not the conversation — so it is a
  complement, not a substitute, for the decision actually made.

## Consequences

- Every lab run leaves a durable, reviewable trace — the same "the merged PR
  (or closed issue) is the change record" pattern the fleet practices
  elsewhere.
- Labs must be re-audited whenever access changes (e.g. a `players` team
  landing) so the stated access in each lab stays honest.
- The pattern catalog and glossary inherit the same evidence discipline: a
  row with no link to a live fleet artifact does not get added.
