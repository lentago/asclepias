# Day one

**What you're about to do:** take one guided lap around a real, working
estate — the org's front door, one product repo, this week's public report —
and then make your own first change to it.

**Why bother:** this fleet runs the way you'll probably want your own org to
run one day — every change reviewed, every change recorded, nothing edited live
by hand at 9 pm. The fastest way to decide whether that's worth building is to
walk through one that already works. Nothing here is yours to break, so poke at
all of it.

**Time:** about an hour. Stop wherever you like; it keeps.

Everything below works from a browser. Nothing needs a VPN, LAN access, or
cloud credentials.

1. **Get a free GitHub account, and that's it.** There's no invite to accept
   and no org to join — you'll do everything from your own account and, when
   you're ready to change something, your own *fork* (your personal copy of a
   repo on GitHub). If you already have an account, you're done with step one.
2. **Read the front door.** The [org profile](https://github.com/lentago)
   says what this place is, and its *"Every merge changes something real"*
   table is the fastest mental model of the fleet.
3. **Pick one product repo** — [solidago](https://github.com/lentago/solidago)
   (AWS platform), [drosera](https://github.com/lentago/drosera)
   (observability — the dashboards and alerts that watch everything),
   [kalmia](https://github.com/lentago/kalmia) (provisioning),
   [claytonia](https://github.com/lentago/claytonia) (the agent fleet), or
   [betula](https://github.com/lentago/betula) (log capture) — and read its
   **🛠️ Make a change yourself** section. Follow one proof-PR link and read
   the actual merged change (the *diff* — the before-and-after of the files).
4. **Read this week's [fleet report](https://github.com/lentago/.github/blob/main/fleet-reports/fleet-report.md)
   and one entry from the [incident register](https://github.com/lentago/.github/blob/main/fleet-reports/incidents.md).**
   The post-mortems — plain write-ups of what broke and why — are the best
   reading in the fleet: what broke, what did *not*, and the lesson that came
   out of it.
5. **Run [Lab 01](../labs/01-first-pr-roster.md)** — add yourself to the
   [guestbook](roster.md) by pull request (a proposed change someone reviews
   before it lands). You'll feel the whole change gate end to end: branch → PR
   → automatic checks → a human review → merge.
6. **Say `@claude` somewhere.** On any issue or PR in the fleet, mention
   `@claude` with a question or a request — the agent responder answers from
   that repo's context. That's the same agent layer the fleet runs on;
   [Lab 03](../labs/03-review-an-agent.md) builds on it.

Then keep climbing: the [lab ladder](../labs/README.md) runs from your first
change (L1) to changing real systems (L2) to reviewing an agent's work (L3).

**How you know you're done:** your name is sitting in the [guestbook](roster.md)
on `main` — your first change all the way through the gate.

**Something confusing on day one?** That's worth writing down, not something
you got wrong — open an issue here. Confusion reports are how these pages get
better.
