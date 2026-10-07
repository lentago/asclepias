# Glossary — enterprise term ↔ how we do it here (and how you can too)

You already know these disciplines by their enterprise names. We run the same
ones — just with lighter machinery you can actually afford and maintain. This
table is the translation layer, and the right-hand column is a decent shopping
list for your own org.

| Enterprise term | How we do it here | Where |
|---|---|---|
| Change management / CAB | Pull request + required status checks + human review; nothing reaches `main` without passing the gate | Branch rulesets fleet-wide ([fleet-ops](https://github.com/lentago/.github/tree/main/fleet-ops)) |
| Change record | The squash-merged PR — title, body, diff, checks, and reviewer in one durable artifact | Every repo; the PR body becomes the squash commit message |
| Standard (pre-approved) change | Auto-merge armed on green checks — the gate still gates, the human round-trip disappears | `gh pr merge --auto --squash` per fleet convention |
| CMDB / asset inventory | `repos.json` as source of truth for repo existence; Terraform state for cloud and hypervisor resources; the weekly census for code | [.github fleet-ops](https://github.com/lentago/.github/blob/main/fleet-ops/repos.json), [solidago](https://github.com/lentago/solidago), [kalmia](https://github.com/lentago/kalmia), [fleet report](https://github.com/lentago/.github/blob/main/fleet-reports/fleet-report.md) |
| Drift detection | `terraform plan` on every PR; generated-artifact CI checks; an append-only ledger for agent config | solidago/kalmia/drosera plans; [music-curator integrity](https://github.com/lentago/music-curator/blob/main/.github/workflows/integrity.yml); [context ledger](https://github.com/lentago/claytonia/blob/main/docs/context-ledger.md) |
| Runbook | The owning repo's README `🛠️` section plus its CLAUDE.md operational notes — versioned next to the thing they operate | Fleet-wide; index at [runbooks](runbooks.md) |
| Post-incident review / PIR | Public post-mortems, published verbatim, indexed in a register | [Incident register](https://github.com/lentago/.github/blob/main/fleet-reports/incidents.md) |
| Monitoring vs. log management | Split by product: live pane (dashboards/alerts) vs. full-volume capture and long retention — adding a source to one never touches the other | [drosera](https://github.com/lentago/drosera) vs. [betula](https://github.com/lentago/betula) |
| Least privilege | Scoped OIDC subject claims; a repo-scoped deploy key for the one writer that needs it; a GitHub App permission ceiling on agent jobs | [solidago IAM split](https://github.com/lentago/solidago/blob/main/docs/WORKLOAD_RELATIONSHIP.md); [claytonia auth](https://github.com/lentago/claytonia#auth) |
| Golden image / SOE | A template forge builds the container image; guests are declared in Terraform and cut from it | [kalmia forge](https://github.com/lentago/kalmia) |
| Service catalog | Platform modules a workload composes (VPC, ECS, ALB, DNS, budgets) — ship a workload by wiring modules, not by filing a ticket | [solidago modules/](https://github.com/lentago/solidago/tree/main/modules) |
| Segregation of duties | The agent that writes code cannot merge it; the pipeline that deploys workloads cannot touch infrastructure | [claytonia](https://github.com/lentago/claytonia) merge gate; solidago trust split |
| Cost management | Budgets-as-code with staged alerts; teardown patterns for idle capacity | [solidago budgets](https://github.com/lentago/solidago/tree/main/modules/budgets) |
| Knowledge base | Plain-Markdown manual written to be read directly, plus a grounded assistant that checks live state before answering from the docs in git | This manual + [mitchella](https://github.com/lentago/mitchella) |

**A mapping feels wrong or incomplete?** Perfect — that disagreement is
exactly what the glossary is for. Open a PR with your version and let review
settle it.
