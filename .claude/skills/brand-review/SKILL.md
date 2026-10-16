---
name: brand-review
description: Review launch assets against positioning, proof, persona and voice rules, with scores, pass/fail and exact fixes. Use as the quality gate before any launch asset reaches a human.
---

# Brand review

## Rubric (score each asset 1 to 5 on each)
| Dimension | 5 looks like | Fail if |
|---|---|---|
| On-positioning | Uses the brief's positioning and key messages exactly | Invents a new message or contradicts the brief |
| Proof integrity | Every claim traces to `proof-points.md` or the input | Any unsupported claim stated as fact |
| Persona fit | Speaks the primary persona's language and fear | Generic copy that could be for any product |
| Voice | Follows every rule in `voice.md` | Any em dash, banned word or exclamation mark |
| Channel fit | Meets the channel spec in the channel-copy skill | Over length limits or missing required parts |

**Pass** = no fail conditions AND an average of 4.0 or higher.

### Design briefs (`07-design-briefs.md`)
Review each visual asset with the same rubric. Channel fit means the spec in `.claude/skills/design-brief/SKILL.md`. Also check:
- Every line of on-image text appears word for word in `03-channel-copy.md`. Any rewritten or added line is a fail.
- On-image text is under 30 words per asset. Count it.
- Each prompt has the asset name, pixel size, on-image text, layout, visual direction and an avoid list.
- The size matches the spec table in the design-brief skill.
- No invented brand colors, logos, screenshots, numbers or names. A `[NEED PROOF: ...]` placeholder is fine.
- The image does not contradict a limitation in the brief, for example by implying support beyond Jira Cloud.
- Visual direction has no fear imagery and does not frame AI or automation owners as the problem.

## Method
1. Run mechanical checks first with Grep across the output folder: em dashes (—), each banned word in `voice.md`, exclamation marks in customer copy, character counts on subject lines and in-app headlines.
2. Then judge each asset against the rubric.
3. For every fail, quote the exact text and give the exact fix.
4. Collect every `[NEED PROOF: ...]` into one list. These are not fails.

## Output template

```
# Review: <release name>

## Mechanical checks
- Em dashes: <count, locations>
- Banned words: <list, locations>
- Length limits: <any breaches>

## Scores
| Asset | Positioning | Proof | Persona | Voice | Channel | Avg | Result |
|---|---|---|---|---|---|---|---|

## Fixes required
### <asset>
- Quote: "<exact text>"
- Problem: <rule broken>
- Fix: <exact change>

## Open proof requests
- <each [NEED PROOF: ...], with file>
```
