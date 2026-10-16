---
name: campaign-strategy
description: Score a release with the GTM playbook in context/tiering.md, decide Tier 1, 2 or 3, and plan the campaign: goals, channels, assets in scope, timeline and success metrics. Use when deciding how big a launch should be and how it will reach people.
---

# Campaign strategy

Two parts in one file: the tier decision, then the campaign plan. The tier decides what gets built.

## Method
### Part A: Tier decision
1. Read `context/tiering.md` for the criteria, weights, thresholds and overrides.
2. Score each criterion 1 to 5 with one line of reasoning that cites the PRD or `context/`. No score without a reason.
3. Calculate the weighted score and show the math.
4. Map to a tier with the thresholds. Check the boundary: a score must land in exactly one tier.
5. Decide whether an override applies. Only for a reason listed in `context/tiering.md`, and say which.
6. List what this tier gets and what it deliberately does not, from the asset matrix, including the "Visual assets" rows.

### Part B: Campaign plan
1. Goals: from `01-launch-brief.md`, restated for this tier.
2. Audience: the primary persona and segments from `03-audience.md`.
3. Channels: one row per channel in scope, with its job, the asset, an owner role and timing as L-offsets.
4. Assets in scope: exactly what the asset matrix says for the tier, with the file that will hold each.
5. Timeline: phases from preparation to measurement.
6. Success metrics: leading and lagging, from the PRD where given. Baselines and targets not given are `[NEED PROOF: ...]`.
7. Risks and dependencies, and what we are choosing not to do.

For Tier 3, keep Part B to: goal, assets in scope, one metric.

## Output template

```
# Campaign strategy: <release name>

## Tier decision
| Criterion | Score (1-5) | Weight | Reason |
|---|---|---|---|
| Customer reach | | 25% | |
| Commercial impact | | 25% | |
| Strategic fit | | 20% | |
| Competitive weight | | 15% | |
| Story value | | 15% | |

**Weighted score:** <math> = <x.xx>
**Tier:** <1, 2 or 3>
**Override:** <none, or up/down one tier and why>

### What this tier gets
- ...
### What it deliberately does not get
- ... (and why that is the right call)
### What would change the tier
- ...

## Campaign plan
### Goals
### Audience
### Channels
| Channel | Job | Asset | Owner (role) | When |
|---|---|---|---|---|
### Assets in scope
| Asset | File |
|---|---|
### Timeline
| Phase | Window | What happens |
|---|---|---|
### Success metrics
| Metric | Type | Baseline | Target | Source |
|---|---|---|---|---|
### Risks and dependencies
### What we are not doing
```
