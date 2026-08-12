# Lab 02 — Move a real dashboard

**Level:** L2 · real system
**Goal:** watch your merged PR change a live system with no human hands on the
apply — the heart of apply-on-merge.
**Access needed:** a fork PR is enough to propose; a maintainer merges. The
apply is CI's job, not yours.

## Steps

1. Read [drosera](https://github.com/lentago/drosera)'s **Make a change
   yourself** section, and its live-state-vs-code lesson (the
   [#119](https://github.com/lentago/drosera/pull/119) story): dashboards
   edited live in Grafana get silently reverted by the next merge — the JSON
   in git is the only durable home.
2. On your lab-run issue, propose a small, reversible change and ask which
   dashboard is fair game — a panel title or description clarification, a
   threshold tweak, a units fix. (The *Claytonia — Runner Fleet* dashboard is
   the fleet watching its own agents; cosmetic improvements there are usually
   welcome.)
3. Edit the dashboard JSON under
   [`dashboards/`](https://github.com/lentago/drosera/tree/main/dashboards)
   and validate it parses: `python3 -m json.tool dashboards/<file>.json`.
4. Open the PR. After a maintainer merges, open the repo's **Actions** tab and
   watch the terraform `apply` job push your change to Grafana Cloud.
5. Confirm it's live — via the public dashboard link if one is published for
   that board, or a screenshot from a maintainer.

## Proof

The merged PR link + the apply workflow-run link (and the before/after of your
panel, if you can capture it).

**What you just practiced:** proposing a production change you cannot apply
yourself, reviewed as a diff, applied by automation, with git as the single
source of truth.
