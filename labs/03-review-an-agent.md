# Lab 03 — Review an agent

**Level:** L3 · agentic

**What you're about to do:** read a pull request an AI agent actually opened,
and review it the way you'd review a change from any teammate — does it do what
was asked, and would you have merged it?

**Why bother:** in this fleet, agents open PRs constantly and **never merge** —
a person reading the diff is the control that keeps that safe. If you're going
to let AI touch your systems at all, this review is the skill that decides
whether that's a good idea or a bad one. It's some of the most consequential
reading anyone does here.

**Time:** about twenty minutes.

**You'll need:** a free GitHub account. Anyone can comment on a PR; if you want
to open one of your own (the live variant below), a fork PR works.

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

**How you know it worked:** your review comment names two things the change got
right, one thing you'd have pushed back on, and whether you'd have merged it —
grounded in the diff and the checks, not in whether the PR body sounds
confident.

**In your own org this looks like:** you can let an agent do real work — draft
a change, fix a link, open a PR — without letting it change production on its
own. The agent does the work; a human reads the diff and clicks merge. That one
rule is what makes the whole thing safe to try.
