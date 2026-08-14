# ADR-0002: Plain public Markdown, engineered for LLM consumption at zero cost

**Status:** Accepted (2026-08-12; reconstructed 2026-08-13)

## Context

Once a dedicated Training repo was chosen
([ADR-0001](0001-dedicated-training-repo.md)), the manual needed a format.
The goal stated in
[lentago/.github#89](https://github.com/lentago/.github/issues/89) was
indexability — "can Devin use it?" — without adding hosting, auth, or a
build step to a repo whose whole point is a low-friction first PR for new
members.

## Decision

The manual is **plain public Markdown, no static-site machinery**. GitHub
renders it natively and DeepWiki indexes a public repo free of charge; a
private DeepWiki index requires a paid Devin org plan, and nothing in the
manual needs privacy (the same line the incident register's publish-verbatim
policy already draws). Headings are treated as a stable API — DeepWiki, an
agent with a checkout, and a colleague with a browser all consume the same
self-contained pages, and renaming a heading is a breaking change for inbound
links.

## Alternatives

- **Private DeepWiki index** — rejected. Requires a paid Devin org plan,
  breaking the zero-cost goal for no privacy benefit this repo actually
  needs.
- **Static-site generator / custom rendering** — rejected. Adds build
  machinery, a deploy step, and a maintenance surface to a repo whose value is
  being readable with nothing more than a browser or `git clone`.
- **Retrospective — not considered at the time: MkDocs (or similar) served
  from the LAN webserver.** Worse. It would have made the manual dependent on
  LAN access to view rendered, defeating the browser-only onboarding this
  decision was explicitly optimizing for — a new member's first stop should
  not require homelab access before they've even done Lab 01.

## Consequences

- No CI/build step is needed to publish the manual — GitHub rendering and the
  `docs-check` workflow (link validation) are the entire toolchain.
- Every page must stay self-contained with stable headings; a heading rename
  is treated as a breaking change, same as an API contract elsewhere in the
  fleet.
- If the manual ever needed to go private, this decision would need
  revisiting — DeepWiki private mode exists but costs money, and the
  zero-cost premise would no longer hold.
