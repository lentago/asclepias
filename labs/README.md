# The lab ladder

Each lab is one rung more agency than the last. Every lab follows the same
shape — **Goal · Access needed · Steps · Proof** — and every run gets its own
[lab-run issue](https://github.com/lentago/asclepias/issues/new/choose), so
there's a durable record and a place for questions.

| Lab | Level | Access needed | What it proves |
|---|---|---|---|
| [00 — Ask the fleet](00-ask-the-fleet.md) | L0 · observe | A browser | You can orient with AI-generated docs *and* verify them against source |
| [01 — First PR: the roster](01-first-pr-roster.md) | L1 · first change | GitHub account (fork or branch) | You've been through the whole change gate: branch → PR → checks → review → squash merge |
| [02 — Move a real dashboard](02-dashboard-change.md) | L2 · real system | Fork PR; a maintainer merges | Your merged change was applied to a live system by automation, not by hands |
| [03 — Review an agent](03-review-an-agent.md) | L3 · agentic | Org membership (Players) | You can review AI-produced work with the same rigor as a colleague's |
| [04 — Game day](04-game-day.md) | L4 · own a pattern | Scheduled with a maintainer | You can break, observe, and write the post-mortem |

**How to run one:** open the lab-run issue, work the steps, post the proof,
close the issue. Stuck ≠ failed — post where you're stuck on the issue; the
answer usually becomes a manual improvement.

**Honesty rule for lab authors:** state access plainly. `Players` grants
triage (assignable reviewer, issue management), not push. Fork PRs run the
required `docs-check` fine; secret-dependent workflows don't run on forks; and
on most repos a maintainer clicks the merge — which is realistic change
management: submitter and approver are different people.
