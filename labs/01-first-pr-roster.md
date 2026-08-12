# Lab 01 — First PR: the roster

**Level:** L1 · first change
**Goal:** feel the fleet's change gate end to end — branch, PR, required
checks, review, squash merge — on a change that cannot break anything.
**Access needed:** a GitHub account. Org members can branch in this repo; a
fork works identically.

## Steps

1. Branch (or fork) this repo and edit
   [`onboarding/roster.md`](../onboarding/roster.md): **append one row** with
   your name, GitHub handle, and join month. Don't touch other rows.
2. Commit with a message you'd want to read in a year, and open a PR. Write
   the body for a reviewer: what and why (one sentence each is fine).
3. Watch the checks. `docs-check` validates every relative link in the repo —
   it must go green before merge is possible. If it fails, the log tells you
   exactly which link broke; fix and push again.
4. A maintainer reviews and squash-merges. (Submitter and approver are
   different people — that's not a lab limitation, that's change management.)
5. After it lands, find your change two more ways: the commit on `main`, and
   your rendered row in the roster. The merged PR is the change record.

## Proof

The merged PR link, and your name rendering in
[`onboarding/roster.md`](../onboarding/roster.md) on `main`.

**Bonus rep:** open a second PR filling in your `First merge` cell with the
first PR's number. Small PRs that finish the paperwork are a habit worth
building.
