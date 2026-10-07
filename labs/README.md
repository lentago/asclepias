# The lab ladder

Each lab is one rung more agency than the last. Every lab follows the same
shape — **Goal · Access needed · Steps · Proof** — and every run gets its own
[lab-run issue](https://github.com/lentago/asclepias/issues/new/choose), so
there's a durable record and a place for questions.

| Lab | Level | Access needed | What you'll walk away with |
|---|---|---|---|
| [01 — First PR: the roster](01-first-pr-roster.md) | L1 · first change | A free GitHub account + a fork | Been through the whole change gate: branch → PR → checks → review → squash merge |
| [02 — Move a real dashboard](02-dashboard-change.md) | L2 · real system | A free GitHub account + a fork; a maintainer merges | Merged a change that automation, not hands, applied to a live system |
| [03 — Review an agent](03-review-an-agent.md) | L3 · agentic | A free GitHub account; anyone can comment, a fork PR works | Reviewed AI-produced work as carefully as you'd review a person's |
| [04 — Game day](04-game-day.md) | L4 · own a pattern | Scheduled with a maintainer | Broken something on purpose, watched the estate react, and written the post-mortem |

**How to run one:** open the lab-run issue, work the steps, post the proof,
close the issue. Stuck ≠ failed — post where you're stuck on the issue; the
answer usually becomes a manual improvement.

**Honesty rule for lab authors:** state access plainly. The path for everyone
is the same — a free GitHub account and a *fork* (your own copy of the repo),
from which you open a pull request. There's no org to join and no write access
to request; org base permission is `none`. A fork PR runs the required
`docs-check` (it re-checks every relative link) just fine, but
secret-dependent workflows don't run against a fork's PR — so a lab that needs
one says so. And a green check is never a merge: on every public repo, `main`
opens only through the maintainer named in the branch-protection push allowlist
(`lentago/.github`'s `terraform/protection.tf`), who reviews and merges. That's
realistic change management — the person proposing a change and the person
approving it are different people.
