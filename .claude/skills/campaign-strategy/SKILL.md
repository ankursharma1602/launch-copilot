---
name: campaign-strategy
description: Take the tier from 03-tiering.md and plan the campaign for that tier: goals, channels, assets in scope, timeline and success metrics. Use when deciding how a launch will reach people.
---

# Campaign strategy

The campaign plan for a tier that is already decided. It does not score the release and it does not override the tier. That is the Tiering agent's job.

## Method
1. Read the tier, the in-scope assets and any override from `03-tiering.md`. Check the asset list against the asset matrix in `context/tiering.md`.
2. Goals: from `01-launch-brief.md`, restated for this tier.
3. Audience: the primary persona and segments from `04-audience.md`.
4. Channels: one row per channel in scope, with its job, the asset, an owner role and timing as L-offsets.
5. Assets in scope: exactly what `03-tiering.md` says, with the file that will hold each.
6. Timeline: phases from preparation to measurement. Label proposed offsets "proposed, to confirm". Include numbered go/no-go gates.
7. Success metrics: leading and lagging, from the closed beta handoff where given. Baselines and targets not given are `[NEED PROOF: ...]`.
8. Risks and dependencies, and what we are choosing not to do.
9. Write the channel plan table across pre-launch, launch and post-launch, with a KPI per phase. This is the showcase output.

For Tier 3, keep it short: goal, assets in scope, one metric, and the channel plan table.

## Output template

```
# Campaign strategy: <release name>

**Tier <n>** (from [03-tiering.md](03-tiering.md))

## Channel plan
| Phase | When (L-offsets) | Channel | Tactic and asset | Owner (role) | KPI for the phase |
|---|---|---|---|---|---|
| Pre-launch | | | | | |
| Launch | | | | | |
| Post-launch | | | | | |

## Campaign plan
### Goals
### Audience
### Assets in scope
| Asset | File |
|---|---|
### Timeline
| Phase | Window | What happens |
|---|---|---|
### Go/no-go gates
1. ...
### Success metrics
| Metric | Type | Baseline | Target | Source |
|---|---|---|---|---|
### Risks and dependencies
### What we are not doing
### Open questions
```

## Showcase outputs (required)
1. **KPI tree.** A north star metric at the top, then 2 or 3 output KPIs that drive it, then the input KPIs under each. Every KPI has a target and a time frame. Use the handoff's GA metrics; where targets are missing, set realistic ones and label them illustrative. Show it as a Mermaid flowchart (top to bottom) plus a table.
2. **Launch scorecard (how the launch is judged).** Four layers, read in order, one or two metrics each, with a target and a read date: (1) Readiness: was the field ready on day one; (2) Campaign: did each launch channel reach and move people (email, in-app, social, sales use of the kit); (3) Adoption: did customers turn it on and keep using it; (4) Business impact: did it change a customer outcome and a business result (retention, expansion, revenue). Then one line on what we fix if each layer misses, and the day-90 retrospective. At most 8 metrics. Do not list every input metric, and drop the KPI tree.
3. **Channel plan** by phase (pre-launch, launch day, post-launch), with a KPI per phase.
