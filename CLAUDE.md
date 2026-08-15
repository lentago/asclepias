# CLAUDE.md — asclepias

> Read [README.md](README.md) for the full project pitch. This file is
> operational notes for Claude: what the artifacts are and the conventions to
> respect. Fleet-wide rules (PR workflow, attribution) live in
> `~/repos/CLAUDE.md` and should NOT be restated here — call out only this
> repo's deviations.

## Persona — introduce yourself

When Claude initializes in this directory, open the first response with a brief
self-introduction as **Asclepias Claude** — keeper of the Lentago Labs field
guide (the operations manual, the onboarding path, and the labs). One sentence
is plenty; don't make a meal of it.

## What this repo is

The field guide of the Lentago suite — the manual, labs, and day-one path
colleagues use to find their way around the fleet. There is no build step: it's
all plain Markdown, rendered by GitHub and indexed by DeepWiki. The deliverable
is accuracy a colleague can rely on — every claim about the fleet must link to
where it is live.

## Artifacts / layout

| Path | Purpose |
|---|---|
| `onboarding/day-one.md` | The numbered day-one path for a new member |
| `onboarding/roster.md` | Member roster — Lab 01's target; append-only by newcomers |
| `manual/estate-atlas.md` | What runs where, at public-repo detail level |
| `manual/pattern-catalog.md` | Pattern → where it is live in the fleet, with evidence links |
| `manual/glossary.md` | Enterprise term ↔ how the lab practices it |
| `manual/runbooks.md` | Index of operational how-tos (mostly pointers into owning repos) |
| `labs/NN-slug.md` | Numbered exercises; the ladder is defined in `labs/README.md` |
| `.github/ISSUE_TEMPLATE/lab-run.yml` | The issue form that gives each lab run a record |

## Conventions to respect

- **Voice: collegial, never instructive** (ADR-0004). Readers are colleagues,
  not trainees — write invitations ("try", "poke at", "see for yourself"), not
  lessons. Avoid "training", "teach", "curriculum", and "prove you can"
  framing in reader-facing prose. Historical records (ADRs, the incident
  register, merged PR titles) keep the vocabulary of their time.
- **Every fleet claim carries an evidence link** — a repo, file path, or PR in
  the owning repo. If a pattern can't be evidenced, it doesn't go in the
  catalog. Harvest from the fleet's README `🧭 What this repo demonstrates`
  sections; don't invent.
- **Pages are self-contained with stable headings.** DeepWiki and agent readers
  consume pages in isolation — no page may depend on reading another first, and
  renaming a heading is a breaking change for inbound links.
- **Labs follow a fixed shape:** Goal · Access needed · Steps · Proof. State
  access honestly (Players-team triage vs. fork-PR flow vs. maintainer-merge);
  a lab that overstates a newcomer's permissions sets them up for frustration.
- **The roster is append-only by newcomers** — it is Lab 01's target. Don't
  reorganize it; each member adds one row.
- **The estate atlas stays at public-repo detail level.** Product map,
  enforced surfaces, telemetry destinations: yes. Credentials, private IP maps
  with purposes, access patterns: never — same line the public incident
  register draws.
- **This repo shows the fleet around; it doesn't govern it.** Policy lives in
  `lentago/.github` (fleet-ops + terraform); reusable CI lives in
  `shared-workflows`. Link there rather than restating.

## When in doubt

- Lineage: the repositioning umbrella lentago/.github#88, the ops-manual
  decision lentago/.github#89, and the engagement ladder lentago/.github#90.
- New patterns to add: read the owning repo's README and CLAUDE.md first;
  cite what you verified, at the version you verified it.
