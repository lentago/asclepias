# ADR-0005: One reader, one voice — vol. 1 of the guide

**Status:** Accepted (2026-09-30). Supersedes the audience premise of
[ADR-0004](0004-collegial-voice.md); keeps its mechanics.

## Context

[ADR-0004](0004-collegial-voice.md) repositioned this repo's voice from a
training ground to a field guide written for **peer colleagues** — IT-ops
professionals invited to explore a shared lab. That audience premise assumed
org membership: a new member accepted an invite, received org-wide write, and
worked the labs from inside the org.

On 2026-09-30 the org was repositioned again
([lentago/.github ADR-0008](https://github.com/lentago/.github/blob/main/docs/adr/0008-pro-bono-practice-one-reader.md)).
Lentago Labs is now a **pro-bono operations practice for organizations that run
on volunteers, donations, and one overworked tech person**, and its own estate
is the working demonstration of its methods. All reader-facing documentation is
written for one reader in one voice, defined in the fleet voice guide
([lentago/.github `docs/voice.md`](https://github.com/lentago/.github/blob/main/docs/voice.md)):
**the one tech person** — a nonprofit's tech director, the volunteer who does
the computers, or a lone technician covering an entire org. A competent
generalist, not a site-reliability engineer; no time, no budget, no backup.

Two facts made the old premise obsolete rather than merely dated:

- **The org-membership on-ramp is retired.** Org base permission is `none` as
  of 2026-09-30; there is no invite to accept and no org-wide write to grant.
  A contributor arrives with a free GitHub account and a fork.
- **This repo is now vol. 1 of a two-volume guide.** asclepias is vol. 1 —
  *how our estate works, with labs you can run against it* — and
  [lupinus](https://github.com/lentago/lupinus) is vol. 2 — *make it yours*.
  The reader of vol. 1 is someone deciding whether these methods fit their own
  org, not a colleague joining ours.

## Decision

Rewrite the audience premise, keep the mechanics.

- **The reader is the one tech person**, not a peer colleague. Reader-facing
  prose follows the fleet voice guide: second person, present tense, every
  term of art defined on first use, the trap named before the step, costs and
  times stated plainly. The voice convention in `CLAUDE.md` now points at
  `docs/voice.md` rather than restating a local rule.
- **Access statements go fork-first.** Labs no longer assume org membership.
  The path for everyone is a free GitHub account and a fork; a maintainer
  reviews and merges. Fork PRs run the required `docs-check` but not
  secret-dependent workflows, and `main` still opens only through the
  maintainer named in the branch-protection push allowlist
  ([lentago/.github `terraform/protection.tf`](https://github.com/lentago/.github/blob/main/terraform/protection.tf)).
- **ADR-0004's mechanics survive unchanged.** Every claim about the fleet
  carries a link to where it is live; access is stated honestly; historical
  records keep their original wording. Only the reader and the register moved.

**Historical records keep their original wording.** ADRs 0001–0004, the
incident register, fleet reports, and merged PR titles are records of their
moment. ADR-0004 is not edited to point here; this ADR supersedes its audience
premise by reference, the same way the fleet's ADR process records supersession
without falsifying the superseded record.

## Alternatives

- **Amend ADR-0004 in place.** Rejected — ADR-0004 recorded a real decision for
  a real audience that existed at the time. Editing it to describe a later
  audience would falsify the record, the line the ADR index's preamble and
  ADR-0004 itself both draw.
- **Keep the colleague voice and only fix the access statements.** Rejected —
  the access change follows from the audience change, not the reverse. A page
  that still addresses a peer colleague while telling them to fork reads as two
  documents stapled together; the voice guide exists precisely to make reader
  and register move together.
- **Fold vol. 1 and vol. 2 into one repo.** Rejected — the two volumes address
  different moments (understand our estate vs. build your own) and the split
  keeps each queryable on DeepWiki as a coherent wiki, the same reasoning
  [ADR-0001](0001-dedicated-training-repo.md) used to keep the manual out of
  `.github`.

## Consequences

- Reader-facing pages (README, onboarding, labs, manual prose) are rewritten in
  the voice guide's register; `CLAUDE.md` points at `docs/voice.md`.
- Access statements across the labs and onboarding are fork-first; the
  day-one "accept the org invite" step is gone, because the on-ramp it
  described no longer exists.
- The roster is reframed as a guestbook — the same append-only Lab 01 target,
  described for a visitor rather than a member.
- Evidence tables, tier labels, costs, times, commands, and status markers are
  unchanged. This ADR moves the voice and the audience, not the facts.
