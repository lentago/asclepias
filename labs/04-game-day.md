# Lab 04 — Game day

**Level:** L4 · own a pattern
**Status:** scheduled runs, not self-serve — coordinate with a maintainer.
The format below is the contract; the first scheduled game day will turn it
into a full lab.

**What you're about to do:** deliberately break something real, watch the
estate catch it, and write up what happened — a *game day*, the practice of
testing your systems by staging a failure on purpose.

**Why bother:** you find out whether your monitoring and rollback actually work
when it's a scheduled exercise, not at 2 am during a real outage. Doing it once
against systems that are already built and instrumented shows you what "good"
looks like before you try to build it for your own org.

**Time:** a scheduled block with a maintainer — this rung is not self-serve,
and that's deliberate.

## The shape

1. **Pick a non-critical target with a maintainer** — the whole premise here
   is real systems, survivable stakes.
2. **Break it on purpose**, with a hypothesis: *what should catch this, and
   how fast?*
3. **Watch the estate react** — betula's capture, drosera's dashboards and
   alerts, the GitOps loops' rollback behavior.
4. **Write the post-mortem** for the
   [incident register](https://github.com/lentago/.github/blob/main/fleet-reports/incidents.md):
   what broke, what did *not*, and the governance lesson. Register entries are
   published verbatim — that's deliberate policy, and it's the fun part.

## Why this is the top rung

Everything below it builds toward this: you'll propose the change, read the
telemetry, review the fixes (some agent-authored), and produce the public
artifact. When you've run a game day end to end, you're not just watching these
patterns anymore — you're operating them.

**How you know it worked:** there's a post-mortem in the
[incident register](https://github.com/lentago/.github/blob/main/fleet-reports/incidents.md)
with your name on the work — what broke, what held, and the lesson — and it
reads as a record anyone in the fleet can learn from.

**In your own org this looks like:** once or twice a year you break something on
purpose, on a schedule, to find out whether your backups restore and your
alerts fire *before* a real failure asks the same question. The write-up
afterward is what turns one scare into something the whole team learns from.

*Interested? Say so on lentago/.github#90 (the engagement-pathways issue) or
open a lab-run issue here.*
