# Day one

Welcome to the lab. Everything below works from a browser — nothing needs VPN,
LAN access, or cloud credentials. Budget an hour; stop wherever you like.

1. **Accept the org invite.** It adds you to the `Players` team automatically —
   that grants triage on the product repos (assignable to reviews, can manage
   issues) and everything you need for the labs.
2. **Read the front door.** The [org profile](https://github.com/lentago)
   says what this place is, and its *"Every merge changes something real"*
   table is the fastest mental model of the fleet.
3. **Pick one product repo** — [solidago](https://github.com/lentago/solidago)
   (AWS platform), [drosera](https://github.com/lentago/drosera)
   (observability), [kalmia](https://github.com/lentago/kalmia)
   (provisioning), [claytonia](https://github.com/lentago/claytonia) (agent
   fleet), or [betula](https://github.com/lentago/betula) (log capture) — and
   read its **🛠️ Make a change yourself** section. Follow one proof-PR link
   and read the actual merged diff.
4. **Ask DeepWiki something.** Every repo README carries starter questions and
   the big badge. Ask, then spot-check one claim in the answer against the
   source — figuring out how far to trust AI-generated answers is half the
   fun here.
5. **Read this week's [fleet report](https://github.com/lentago/.github/blob/main/fleet-reports/fleet-report.md)
   and one entry from the [incident register](https://github.com/lentago/.github/blob/main/fleet-reports/incidents.md).**
   The post-mortems are the best reading in the fleet — what broke, what did
   *not*, and the governance lesson.
6. **Run [Lab 01](../labs/01-first-pr-roster.md)** — add yourself to the
   [roster](roster.md) by pull request. You'll feel the whole change gate:
   branch → PR → required checks → review → squash merge.
7. **Say `@claude` somewhere.** On any issue or PR in the fleet, mention
   `@claude` with a question or a request — the agent responder answers from
   the repo's context. That's the agentic on-ramp; [Lab 03](../labs/03-review-an-agent.md)
   builds on it.

Then keep climbing: the [lab ladder](../labs/README.md) runs from asking
questions (L0) to changing real systems (L2) to reviewing an agent's work (L3).

**Something confusing on day one?** That's a finding, not a failure — open an
issue here. Confusion reports are how the manual gets better.
