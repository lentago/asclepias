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

**Vol. 1 of the Lentago Labs guide** — how our estate works, with labs you can
run against it before building your own. It's written for the one tech person
the fleet voice guide defines (a nonprofit's tech director, the volunteer who
does the computers, a lone technician covering a whole org), and it needs no
org membership. lupinus is vol. 2 — *make it yours*. There is no build step:
it's all plain Markdown, rendered by GitHub. The deliverable is accuracy the
reader can rely on — every claim about the fleet must link to where it is
live.

## Artifacts / layout

| Path | Purpose |
|---|---|
| `onboarding/day-one.md` | The numbered day-one path for a first-time reader |
| `onboarding/roster.md` | Guestbook — Lab 01's target; append-only by visitors |
| `manual/estate-atlas.md` | What runs where, at public-repo detail level |
| `manual/pattern-catalog.md` | Pattern → where it is live in the fleet, with evidence links |
| `manual/glossary.md` | Enterprise term ↔ how we do it here (and how you can too) |
| `manual/runbooks.md` | Index of operational how-tos (mostly pointers into owning repos) |
| `labs/NN-slug.md` | Numbered exercises; the ladder is defined in `labs/README.md` |
| `.github/ISSUE_TEMPLATE/lab-run.yml` | The issue form that gives each lab run a record |

## Conventions to respect

- **Voice: the fleet voice guide, for one reader** (ADR-0005, superseding
  ADR-0004's audience premise). Reader-facing prose follows
  `lentago/.github`'s [`docs/voice.md`](https://github.com/lentago/.github/blob/main/docs/voice.md)
  (the canon ADR-0008 points at): write to the one tech person, second person
  and present tense, define every term of art on first use, name the trap
  before the step, state costs and times plainly. Don't restate the guide
  here — follow it and its retire list. Historical records (ADRs, the incident
  register, merged PR titles) keep the vocabulary of their time.
- **Every fleet claim carries an evidence link** — a repo, file path, or PR in
  the owning repo. If a pattern can't be evidenced, it doesn't go in the
  catalog. Harvest from the fleet's README `🧭 What this repo demonstrates`
  sections; don't invent.
- **Pages are self-contained with stable headings.** Agent readers and
  grounded Ask boxes consume pages in isolation — no page may depend on reading another
  first, and renaming a heading is a breaking change for inbound links.
- **Labs follow a fixed shape:** Goal · Access needed · Steps · Proof. State
  access honestly (fork-first vs. maintainer-merge); a lab that overstates a
  reader's permissions sets them up for frustration. **Nobody holds org-wide
  write any more** — org base permission is `none` since 2026-09-30, so there
  is no team and nothing to request. The path for everyone is a free GitHub
  account and a fork; a maintainer reviews and merges. Fork PRs run the
  required `docs-check` but not secret-dependent workflows, and `main` on every
  public repo opens only through the maintainer named in the branch-protection
  push allowlist (`lentago/.github`'s `terraform/protection.tf`).
- **The guestbook is append-only by visitors** — `onboarding/roster.md` is
  Lab 01's target. Don't reorganize it; each person adds one row.
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
