# Lab 02 — Move a real dashboard

**Level:** L2 · real system

**What you're about to do:** propose a small change to a live Grafana dashboard
and, once it's merged, watch automation push it to production — no one logging
in and editing by hand.

**Why bother:** this is *apply-on-merge* — the merge itself is what changes the
live system, so the change that ran and the change in git are always the same
thing. It's the pattern that ends "someone tweaked it in the console and forgot
to write it down." Seeing it once makes the case for building it at home.

**Time:** about thirty minutes of work, plus however long until a maintainer
merges.

**You'll need:** a free GitHub account and a fork — that's enough to propose.
A maintainer merges; the apply is CI's job, not yours.

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

**How you know it worked:** your panel looks different in live Grafana, and the
only thing you did to make that happen was merge a pull request. The apply job
in the Actions tab is the receipt — no console edits, no hands on production.

**In your own org this looks like:** the things people usually change by
clicking around — a dashboard, a DNS record, a firewall rule — become files in
git that a merge applies for you. You review the change before it ships, and
git is always the truth about what's running, because nothing reaches
production any other way.
