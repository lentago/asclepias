# Lab 03 — Review an agent

**Level:** L3 · agentic
**Goal:** review AI-produced work with the same rigor you'd give a colleague's
PR. In this fleet, agents open PRs constantly and **never merge** — the human
review is the load-bearing control, so reviewing agent output well is a
first-class operator skill.
**Access needed:** org membership (the `Players` team makes you assignable as
a reviewer; commenting works for anyone).

## Steps

1. Open [claytonia's merged PRs](https://github.com/lentago/claytonia/pulls?q=is%3Apr+is%3Amerged)
   and pick one authored by the `lentago-claude-runner` App — a real job a
   worker did.
2. Review it as if it were pending: read the PR body first (does it say what
   and why?), then the diff. Ask the reviewer questions: Is the change scoped
   to what was asked? Does anything look plausible-but-unverified? What would
   you have asked for before merging?
3. Check the CI signal the merger relied on — which checks ran, what they
   actually prove, and what they *don't* cover.
4. Write your review as a PR comment: two things done well, one thing you'd
   have pushed back on (there is almost always one), and whether you'd have
   merged.
5. **Live variant:** mention `@claude` on any issue with a scoped question or
   small request, then review what comes back the same way. The
   [shared-workflows](https://github.com/lentago/shared-workflows) README
   documents how the responder routes.

## Proof

A link to your review comment.

**What you just practiced:** the trust model that makes agentic operations
safe — autonomy on the work, humans on the merge, and reviewers who read the
diff instead of the vibes.
