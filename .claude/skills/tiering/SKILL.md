---
name: tiering
description: Score a release on the 4Cs (Commercial, Customer, Competitive, Category) with the rubric in context/tiering.md, decide Tier 1, 2 or 3, and show the scorecard. Use when deciding how big a launch should be, before audience and positioning work begins.
---

# Tiering

The tier decision, on its own. It runs after the launch context and before the audience, so every later step knows how big this launch is. The tier decides what gets built.

## Method
1. Read `context/tiering.md` for the 4Cs, weights, thresholds, overrides and asset matrix.
2. Read the closed beta handoff, `01-launch-brief.md` and `02-launch-context.md`.
3. Score each C from 1 to 5 with one line of reasoning that cites the handoff, the launch brief, the launch context or `context/`. No score without a reason.
4. Never invent commercial numbers (revenue, pipeline, customer counts, shares). If an input is missing, write `[NEED PROOF: ...]`, score on what is known, and say the score is a judgement.
5. Calculate the weighted score and show the maths. Map it to a tier with the thresholds. A score lands in exactly one tier. Check the boundary.
6. Decide whether an override applies. Only for a reason listed in `context/tiering.md`, and say which. State the override and its reason in the file.
7. List what this tier gets and what it deliberately does not, from the asset matrix, including the "Visual assets" rows.
8. Say what would change the tier.

## Output template (a scorecard a PMM can share)

```
# Tiering: <release name>

**Tier <n>** | Weighted score <x.xx> | Override: <none, or up/down one tier>

## 4Cs scorecard
| Criterion | Score (1-5) | Weight | One-line reason (source) |
|---|---|---|---|
| Commercial | | 25% | |
| Customer | | 25% | |
| Competitive | | 25% | |
| Category | | 25% | |

**Maths:** (a x 0.25) + (b x 0.25) + (c x 0.25) + (d x 0.25) = <x.xx>
**Tier:** <1, 2 or 3>, because <threshold>
**Override:** <none, or up/down one tier and the reason from context/tiering.md>

## Assets in scope
| Asset | In scope? |
|---|---|
(One row per row of the asset matrix for this tier, including the Visual assets rows.)

## Out of scope on purpose
- <asset>, and why that is the right call

## What would change the tier
- ...

## Open items
- <every [NEED PROOF] and judgement call>
```

## Showcase check
This file is shared as is. The scorecard table must render on GitHub, show the maths, and carry no invented numbers.
