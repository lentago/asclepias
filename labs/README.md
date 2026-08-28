# The lab ladder

Each lab is one rung more agency than the last. Every lab follows the same
shape — **Goal · Access needed · Steps · Proof** — and every run gets its own
[lab-run issue](https://github.com/lentago/asclepias/issues/new/choose), so
there's a durable record and a place for questions.

| Lab | Level | Access needed | What you'll have done |
|---|---|---|---|
| [00 — Ask the fleet](00-ask-the-fleet.md) | L0 · observe | A browser | Asked AI-generated docs a real question — and checked the answer against source |
| [01 — First PR: the roster](01-first-pr-roster.md) | L1 · first change | GitHub account (fork or branch) | Been through the whole change gate: branch → PR → checks → review → squash merge |
| [02 — Move a real dashboard](02-dashboard-change.md) | L2 · real system | Fork PR; a maintainer merges | Merged a change that automation, not hands, applied to a live system |
| [03 — Review an agent](03-review-an-agent.md) | L3 · agentic | Org membership (write, org-wide) | Reviewed AI-produced work with the same care as a colleague's |
| [04 — Game day](04-game-day.md) | L4 · own a pattern | Scheduled with a maintainer | Broken something on purpose, watched the estate react, and written the post-mortem |

**How to run one:** open the lab-run issue, work the steps, post the proof,
close the issue. Stuck ≠ failed — post where you're stuck on the issue; the
answer usually becomes a manual improvement.

**Honesty rule for lab authors:** state access plainly. Org membership grants
**write** on every repo in the fleet — no team, no per-repo request, enough
to branch and open a PR anywhere. It does not grant merge: on every public
repo, `main` opens only through the maintainer named in the branch-protection
push allowlist (`lentago/.github`'s `terraform/protection.tf`), who reviews
and merges — that's realistic change management: submitter and approver are
different people. Fork PRs still run the required `docs-check` fine, but
secret-dependent workflows don't run against a fork's PR — one reason a
direct branch is often simpler now that write is there for the asking.
