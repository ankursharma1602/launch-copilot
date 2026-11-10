---
name: brand-review
description: Review every launch asset against positioning, messaging, proof, persona and voice rules, with scores, pass or fail, and exact fixes. Use as the quality gate before any launch asset reaches a human.
---

# Review

## Rubric (score each asset 1 to 5 on each)
| Dimension | 5 looks like | Fail if |
|---|---|---|
| On-positioning and messaging | Matches `05-positioning.md` and `06-messaging.md`: the core message, pillars and persona angle | Invents a message, contradicts the positioning, or drifts from the messaging |
| Proof integrity | Every claim traces to `context/proof-points.md` or the closed beta handoff | Any unsupported claim stated as fact, or any closed beta number or customer quote in a customer-facing asset without `[NEED PROOF: approval to use closed beta results or quotes]` |
| Persona fit | Speaks the primary persona's language and fear | Generic copy that could be for any product |
| Voice | Follows every rule in `context/voice.md` | Any em dash, banned word or exclamation mark in customer copy |
| Spec fit | Meets the spec for that asset | Over a length limit or missing a required part |
| Reads like the company's own marketing (the quality bar) | Could sit next to the company's own help center article and event coverage in `context/proof-points.md` and `context/voice.md` and not look out of place. Plain, practical, task-focused. Names the real buttons and places. Says what the feature does, how it works in steps, and what the person does next. Short sentences. Limits stated matter of factly. | Reads like generic SaaS marketing: abstract claims, filler, internal jargon in customer-facing text ("pillar", "Must say", "persona"), a sentence that does not say what the thing does or what the reader does next, or tone that is noticeably more hype or more formal than the benchmark sources |

**Pass** = no fail condition AND an average of 4.0 or higher.

## The quality bar (benchmark test)
Every output must read like the company's own published product marketing, the kind its product marketing team would ship. The benchmark is the company's own help center article and event coverage cited in `context/proof-points.md`, and the tone in `context/voice.md`.
1. Read the benchmark sources first. Note their habits: the exact names of buttons and screens, steps in order, plain verbs, no adjectives doing the work of proof.
2. For each asset, set its weakest sentences next to the closest benchmark sentence. Quote both in the review.
3. Fail the asset on the quality bar dimension if it falls short, and give an exact replacement that uses only facts already in `context/` or the closed beta handoff. A rewrite must not add a claim.
4. A rewrite for style never removes a limitation, an illustrative label or a `[NEED PROOF: ...]` tag.

## What to check per asset type
- **Upstream docs (01 to 07):**
  - 02 states every limitation and does not turn roadmap hints into promises.
  - 03 shows the 4Cs maths, the tier lands in exactly one band, any override uses a reason from `context/tiering.md`, and the in-scope list matches the asset matrix.
  - 04 stays within `context/personas.md` and treats closed beta feedback as a small sample.
  - 05 follows the Dunford order (alternatives, attributes, value and proof, best-fit customers, category, trends), has no fill-in-the-blank statement, and makes no unsourced competitor claim.
  - 06 traces every message to 05.
  - 07 takes the tier from 03 and does not re-score or override it. Its asset list matches 03.
- **08 Channel copy:** channel specs, "Must say" limitations present in every asset, subject and headline lengths.
- **09 Design briefs and visuals:**
  - On-image text is word for word from 08, under 30 words (the one-pager layout may run to about 90), and matches what is in the SVG. No empty placeholder cards.
  - Sizes match the spec table. Check the PNG files exist and read their pixel sizes.
  - Every visual uses the colours, typeface and wordmark rule in `context/brand.md`, and the PNG shows the brand typeface. The wordmark is live text, and no logo file or brand mark is used. The brief flags the unconfirmed palette and typeface. No invented logos, screenshots, numbers or names.
  - No limitations, disclaimers or plan caveats on the email header, in-app banner or LinkedIn image. Only the one-pager layout carries one small limits line. The limitations are present in the accompanying copy.
  - No fear imagery, and no framing of AI or automation owners as the problem.
  - Open each PNG with the Read tool and check that text is not clipped or overlapping.
- **10 Sales enablement:** opens with the battlecard, talk track under 150 words, every limitation in the FAQ, one-pager has the "Limits to state up front" line, no unsourced competitor claim, no customer pattern stated as fact.
- **10b Enablement session:** agenda adds up to 30 minutes, three role-plays built from the personas.
- **10c Readiness quiz:** 8 questions with an answer key, covering positioning, top objections and limitations.
- **11 Checklist:** the CSV has the same column count on every row, fields with commas or quotes are quoted, and every "Depends On" entry matches a Task name.

## Showcase outputs (check every one)
Each showcase output must exist, render cleanly on GitHub, invent nothing and carry its illustrative label. A missing or broken one is a fail for that file.
| File | Showcase output to check |
|---|---|
| 01 launch brief | "Launch at a glance" table at the top. Mock dates labelled "illustrative". |
| 03 tiering | 4Cs scorecard table with weights, the weighted score with the maths shown, the tier, any override with its reason, in-scope and out-of-scope assets. |
| 04 audience | "Illustrative personas" table with "Target Audience" as the first column and one column per persona, all required rows present, plus `visuals/audience-personas.png` in brand colours only with each persona header in its own brand colour. Open the PNG and check it is not clipped. No real people or firms, no invented demographics. |
| 05 positioning | April Dunford canvas table with all six elements. |
| 06 messaging | One-line value proposition, three pillars with proof, message matrix (personas by headline, key benefit, proof, CTA), "Avoid saying" list. |
| 07 campaign strategy | Channel plan table across pre-launch, launch and post-launch, with a KPI per phase. |
| 10 sales enablement | One-page battlecard at the top: why now, who to target, 3 discovery questions, top 3 objections with responses, proof. |
| 11 launch checklist | Mermaid Gantt with owners and milestones by week, and a note that it is an illustrative calendar if there is no real date. Check the Mermaid syntax by reading it. |

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
- Showcase outputs: <each present, renders, labelled; list any missing>
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

## Full open items
(every [NEED PROOF: ...], unknown, reviewer advisory and anything that failed review twice, with file. The run report links here.)

## Open proof requests
- <each [NEED PROOF: ...], with file>

## Second pass
(appended after revision: pass or fail for each revised asset)
```
