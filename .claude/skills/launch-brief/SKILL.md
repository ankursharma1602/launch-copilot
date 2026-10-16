---
name: launch-brief
description: Write a launch brief (problem, audience, positioning, key messages, proof, goals) grounded in company context. Use when a release needs a single source of truth for everyone working on the launch.
---

# Launch brief

The brief is the single source of truth. Every other asset copies its positioning and messages. Get it right and short.

## Method
1. Find the problem in the customer's words, not the product's. Use the persona language in `context/personas.md`.
2. Choose ONE primary persona and at most one secondary. Say why.
3. Name the real alternative the customer uses today, including "do it by hand" or "do nothing."
4. Write the positioning statement using the template below.
5. Write three key messages. Each needs a proof point from `context/proof-points.md` or the input, or `[NEED PROOF: ...]`.
6. Tie the launch to a company growth driver from `context/company.md`. This is the "why now."
7. Set success metrics. Use the input's metrics if given. Add a leading and a lagging indicator.

For a Tier 3 release, keep only: summary, primary persona, positioning statement, one key message, success metric.

## Output template

```
# Launch brief: <release name>

**Tier:** <x> | **Launch date:** <date or [NEED PROOF: GA date]> | **Primary persona:** <persona>

## In one sentence
<what it is and who it's for>

## The problem
<2-3 sentences in the customer's language. The moment of failure they recognize.>

## Who it's for
- **Primary:** <persona>, because <reason>
- **Secondary:** <persona or none>

## Today's alternative
<what they do now, and why it hurts>

## Positioning statement
For <primary persona> who <need>, <product/feature> is the <category> that <key benefit>. Unlike <alternative>, it <key difference>.

## Key messages
1. **<message>** Proof: <proof point or [NEED PROOF: ...]>
2. **<message>** Proof: <...>
3. **<message>** Proof: <...>

## Why now
<link to a growth driver in company.md>

## Success metrics
- Leading: <metric, timeframe>
- Lagging: <metric, timeframe>

## Open questions
- <contradictions, missing facts, decisions a human must make>
```
