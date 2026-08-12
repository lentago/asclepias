# Runbooks

The fleet's runbooks live **next to the systems they operate** — each repo's
README (`🛠️ Make a change yourself`) is the operator entry point, and its
CLAUDE.md carries the deeper operational notes. This page is the index, not a
copy; it grows as labs surface the how-tos people actually need.

| I want to… | Go to |
|---|---|
| Ship a new workload on the AWS platform | [solidago → Make a change yourself](https://github.com/lentago/solidago#%EF%B8%8F-make-a-change-yourself) |
| Add or change a Grafana dashboard | [drosera → Make a change yourself](https://github.com/lentago/drosera#%EF%B8%8F-make-a-change-yourself) |
| Create a purpose-built container on the cluster | [kalmia → Make a change yourself](https://github.com/lentago/kalmia#%EF%B8%8F-make-a-change-yourself) |
| Dispatch a job to the agent fleet / add a runner | [claytonia → Make a change yourself](https://github.com/lentago/claytonia#%EF%B8%8F-make-a-change-yourself) |
| Add a log source | [betula → Make a change yourself](https://github.com/lentago/betula#%EF%B8%8F-make-a-change-yourself) |
| Change a smart-home automation | [homeassistant-config → Make a change yourself](https://github.com/lentago/homeassistant-config#%EF%B8%8F-make-a-change-yourself) |
| Change a fleet-wide policy (checks, labels, settings) | [.github → Make a change yourself](https://github.com/lentago/.github#%EF%B8%8F-make-a-change-yourself) |
| Improve CI for every repo at once | [shared-workflows](https://github.com/lentago/shared-workflows) |
| Start a brand-new fleet repo | [repo-template → SETUP.md](https://github.com/lentago/repo-template/blob/main/SETUP.md) |

**Convention for adding a runbook here:** if the how-to belongs to one system,
write it in that repo and link it; write it *here* only when it genuinely spans
repos (like an onboarding flow or a cross-system exercise).
