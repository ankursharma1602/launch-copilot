---
name: launch-brief
description: Write the launch kickoff doc from a PRD: what is launching, why it matters to the business, goals, timeline, stakeholders and open questions. Use when a launch needs a shared starting point before strategy work begins.
---

# Launch brief

The kickoff doc. It frames the launch so everyone starts from the same facts. It does not decide the tier, the positioning or the messages. Those come later, and they build on this.

## Method
1. State what is launching in one sentence, using the PRD's facts and the customer's words, not the feature's internal name.
2. Explain why it matters to the business. Tie it to a growth driver in `context/company.md`. Say which one and how.
3. Set goals. Use the PRD's success metrics. Baselines and targets the PRD does not give are `[NEED PROOF: ...]`.
4. Lay out the timeline. If there is no date, use launch day as "L" and flag the missing date as an open question.
5. List stakeholders as roles, each with what they own in this launch.
6. List open questions: gaps, contradictions with `context/`, decisions a human must make, and who could answer each.

## Output template

```
# Launch brief: <release name>

**Source:** <PRD file> | **Launch date:** <date or [NEED PROOF: GA date]> | **Status:** Kickoff

## What is launching
<one to three sentences, in the customer's words>

## Why it matters to the business
<tie to a growth driver in context/company.md; say which, and the commercial logic>

## Goals
| Goal | Metric | Baseline | Target | Source |
|---|---|---|---|---|

## Timeline
| Milestone | When | Depends on |
|---|---|---|
(Use L-offsets if no date.)

## Stakeholders
| Role | Owns in this launch |
|---|---|

## Open questions
| Question | Why it matters | Who can answer |
|---|---|---|
```
