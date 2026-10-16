---
name: launch-tiering
description: Score a release on the company's tiering rubric and decide Tier 1, 2 or 3 with reasons. Use when deciding how big a launch should be.
---

# Launch tiering

## Method
1. Read `context/tiering.md` for the criteria, weights, thresholds and overrides.
2. Score each criterion 1 to 5. For each, write one line of reasoning that cites the input or `context/`. No score without a reason.
3. Calculate the weighted score. Show the math.
4. Map to a tier using the thresholds.
5. Decide whether an override applies. Only use one for a reason listed in `context/tiering.md`, and say which.
6. List the assets this tier gets and the assets it deliberately does not get, from the asset matrix.

## Output template

```
# Tier decision: <release name>

| Criterion | Score (1-5) | Weight | Reason |
|---|---|---|---|
| Customer reach | | 25% | |
| Commercial impact | | 25% | |
| Strategic fit | | 20% | |
| Competitive weight | | 15% | |
| Story value | | 15% | |

**Weighted score:** <math> = <x.x>
**Tier:** <1, 2 or 3>
**Override:** <none, or up/down one tier and why>

## What this tier gets
- <asset list>

## What it deliberately does not get
- <asset list, and one line on why that's the right call>

## What would change the tier
<one or two lines: the evidence that would move it up or down>
```
