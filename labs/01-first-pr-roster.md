# Lab 01 — First PR: the roster

**Level:** L1 · first change

**What you're about to do:** make one tiny change to a file in this repo and
watch it travel the whole way to live — branch, pull request, automatic checks,
a human review, merge. It can't break anything. That's the point.

**Why bother:** this exact flow is how you'll want changes to happen in your
own org — every change reviewed, every change recorded, nobody editing the live
thing by hand at 9 pm. Doing it once here, where it's free and safe, is the
fastest way to understand what you're about to set up at home.

**Time:** about twenty minutes, most of it waiting for a human to click merge.

**You'll need:** a free GitHub account. Nothing else.

> **Heads up.** You'll *fork* this repo rather than editing it directly. A fork
> is your own copy on GitHub; a *pull request* from it is you saying "here's a
> change, please take it." That's the whole mechanism, and it's the same one
> you'll use for everything else here.

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

**Bonus:** open a second PR filling in your `First merge` cell with the
first PR's number. Small PRs that finish the paperwork are always welcome
here.

**How you know it worked:** your name is on `main`, and the PR that put it
there is closed and merged — checks green, a human's approval on it. You just
watched a change go all the way in without anyone touching the live file by
hand.

**In your own org this looks like:** you stop editing production directly.
Every change — a config tweak, a new automation, a doc fix — becomes a small
pull request that runs its checks and gets a second set of eyes before it
lands. The merged PR is your change log, written for free.
