# ADR-0001: A dedicated public Training repo

**Status:** Accepted (2026-08-12; reconstructed 2026-08-13)

## Context

The Lentago org was being repositioned as a shared learning lab, with the
first colleague aboard and more invites pending
([lentago/.github#88](https://github.com/lentago/.github/issues/88)). The
fleet's knowledge was spread across sixteen READMEs, `CLAUDE.md` files, the
weekly fleet report, the incident register, and DeepWiki — good individually,
but no single front door. A new member needed one place answering: what is
this estate, what patterns does it run, how do I do X.

## Decision

Create a **dedicated public Training repo** rather than fold the manual into
`lentago/.github`
([lentago/.github#89](https://github.com/lentago/.github/issues/89)). The
manual becomes the Training product in the suite: DeepWiki indexes it as one
coherent, queryable wiki; the repo doubles as the first sandbox where members
make their first PR without touching a production-ish repo; labs live as
issue templates; onboarding is a day-one checklist. `.github` stays
governance-only.

The codename **asclepias** (milkweed — the host plant that raises the next
generation of monarchs) was chosen over the other candidates on the roster,
**epigaea** (trailing arbutus) and **lupinus** (lupine).

## Alternatives

- **Fold into `lentago/.github`** — rejected. Already the governance home
  (fleet-ops, fleet reports, incident register, org profile); mixing in a
  growing labs/curriculum tree would swamp the meta-repo's actual job and
  muddy the DeepWiki index (settings-as-code scripts blended with manual
  prose).
- **GitHub wiki or an external docs site** — rejected. A wiki bypasses PRs and
  status checks, undermining the "every change is a PR" lesson the lab exists
  to teach; an external site adds hosting and auth for no gain.
- **Retrospective — not considered at the time: start the repo private, make
  it public once the manual was more complete.** Worse. DeepWiki's free tier
  indexes public repos only — a private start would have deferred the
  queryable-textbook payoff this decision was optimizing for, and the repo's
  own first PR (seeding the manual) is itself the first practiced pattern;
  hiding it would have undercut "the repo itself practices every pattern it
  teaches."

## Consequences

- `asclepias` was created from `lentago/repo-template` and adopted into fleet
  settings-as-code (squash-only merges, a `main` ruleset, a required
  `docs-check`), then seeded with the manual, onboarding path, and labs 00–04
  via [asclepias#1](https://github.com/lentago/asclepias/pull/1).
- The manual grows by harvest from the fleet's verified README evidence, not
  by invention — the discipline this repo now enforces on itself.
- `.github` remains the single governance home; any future curriculum content
  belongs here, not there.
