# ADR-0004: Collegial voice — a field guide, not a training ground

**Status:** Accepted (2026-08-15)

## Context

The repo launched as "the Lentago Labs training ground," and that framing ran
through everything: the banner tagline, the GitHub description and a `training`
topic, "curriculum," lab columns headed *What it proves*, and closers like
*What you just practiced*. The audience, though, is professional colleagues —
IT-ops peers being invited to explore a shared lab — and instructive framing
casts the author as trainer and the reader as trainee. That posture is neither
accurate nor inviting, and it reads as presumptuous when the org is shared
with people who operate systems for a living.

## Decision

Reposition the repo's voice as **an invitation among colleagues**:

- The identity noun is **field guide** (keeping the botanical register), not
  training ground. The brand tagline, GitHub description, topics, and
  org-profile blurb changed with it in `lentago/.github`
  ([#110](https://github.com/lentago/.github/pull/110)).
- Reader-facing prose drops "training," "teach," "curriculum," and
  "prove you can" framing in favor of *try it*, *see for yourself*, and
  *what you'll have done*. The voice convention now lives in this repo's
  `CLAUDE.md` so future content follows it.
- The substance is unchanged: the lab ladder, the fixed lab shape, the honesty
  rules about access, and the evidence-link discipline all stay exactly as
  they were. Only the posture moved.

**Historical records keep their original wording.** ADRs 0001–0003, the
incident register, fleet reports, and merged PR titles are records of their
moment — retitling them would falsify history, the same line the incident
register already draws.

## Alternatives

- **Keep the training framing.** Rejected — the org profile had already been
  adjusted for the colleague audience (lentago/.github#103 dropped the
  employer name and reframed patterns as candidates); a repo still calling
  itself the training ground undercut that repositioning at its front door.
- **Rename the historical ADRs and reconstruct the record in the new
  vocabulary.** Rejected — the ADR index's own preamble promises a faithful
  reconstruction; editing decision records to match a later voice is exactly
  the drift it warns against.

## Consequences

- `CLAUDE.md` carries the voice convention; content PRs are reviewed against
  it.
- The founding artifacts (ADR-0001's title, `0003-curriculum-as-issues.md`'s
  filename, asclepias#1's PR title) still say "training" and "curriculum" —
  deliberately, as history.
- The regenerated social-preview card (`og.png`) requires a manual upload in
  repo settings; until then the link unfurl shows the old tagline.
