---
name: brand-review
description: Review every launch asset against positioning, messaging, proof, persona and voice rules, with scores, pass or fail, and exact fixes. Use as the quality gate before any launch asset reaches a human.
---

# Review

## Rubric (score each asset 1 to 5 on each)
| Dimension | 5 looks like | Fail if |
|---|---|---|
| On-positioning and messaging | Matches `04-positioning.md` and `05-messaging.md`: the core message, pillars and persona angle | Invents a message, contradicts the positioning, or drifts from the messaging |
| Proof integrity | Every claim traces to `context/proof-points.md` or the PRD | Any unsupported claim stated as fact |
| Persona fit | Speaks the primary persona's language and fear | Generic copy that could be for any product |
| Voice | Follows every rule in `context/voice.md` | Any em dash, banned word or exclamation mark in customer copy |
| Spec fit | Meets the spec for that asset | Over a length limit or missing a required part |

**Pass** = no fail condition AND an average of 4.0 or higher.

## What to check per asset type
- **Upstream docs (01 to 06):**
  - 02 states every limitation and does not turn roadmap hints into promises.
  - 04 follows the Dunford order (alternatives, attributes, value and proof, best-fit customers, category, trends), has no fill-in-the-blank statement, and makes no unsourced competitor claim.
  - 05 traces every message to 04.
  - 06 shows the score math, the tier lands in exactly one band, and the asset list matches the asset matrix.
- **07 Channel copy:** channel specs, "Must say" limitations present in every asset, subject and headline lengths.
- **08 Design briefs and visuals:**
  - On-image text is word for word from 07, under 30 words, and matches what is in the SVG.
  - Sizes match the spec table. Check the PNG files exist and read their pixel sizes.
  - Placeholder brand colors are marked as placeholders. No invented logos, screenshots, numbers or names.
  - No fear imagery, and no framing of AI or automation owners as the problem.
  - Open each PNG with the Read tool and check that text is not clipped or overlapping.
- **09 Sales enablement:** talk track under 150 words, every limitation in the FAQ, one-pager has the "Limits to state up front" line, no unsourced competitor claim, no customer pattern stated as fact.
- **09b Enablement session:** agenda adds up to 30 minutes, three role-plays built from the personas.
- **09c Readiness quiz:** 8 questions with an answer key, covering positioning, top objections and limitations.
- **10 Checklist:** the CSV has the same column count on every row, fields with commas or quotes are quoted, and every "Depends On" entry matches a Task name.

## Method
1. Run mechanical checks first with Grep across the output folder: em dashes, en dashes, each banned word in `context/voice.md`, exclamation marks in customer copy, subject and headline lengths, word counts.
2. Check consistency down the chain: copy to messaging to positioning to context.
3. Judge each asset against the rubric.
4. For every fail, quote the exact text and give the exact fix.
5. Collect every `[NEED PROOF: ...]` into one list. These are not fails.
6. Re-review: after one revision, append a second-pass section for the revised assets only.

## Output template

```
# Review: <release name>

## Mechanical checks
- Em dashes and en dashes: <count, locations>
- Banned words: <list, locations>
- Exclamation marks: <count>
- Length limits: <any breaches>

## Scores
| Asset | Positioning and messaging | Proof | Persona | Voice | Spec | Avg | Result |
|---|---|---|---|---|---|---|---|

## Fixes required
### <asset>
- Quote: "<exact text>"
- Problem: <rule broken>
- Fix: <exact change>

## Open proof requests
- <each [NEED PROOF: ...], with file>

## Second pass
(appended after revision: pass or fail for each revised asset)
```
