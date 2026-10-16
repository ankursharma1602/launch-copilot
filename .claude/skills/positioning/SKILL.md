---
name: positioning
description: Build positioning with April Dunford's Obviously Awesome method, in order: competitive alternatives, unique attributes, value and proof, best-fit customers, market category, relevant trends. Use when a launch needs positioning grounded in evidence, not a slogan.
---

# Positioning (Obviously Awesome method)

Positioning is context that helps customers understand what a product is, why it is special and why they should care. Build it from the evidence, in this order. Each step feeds the next. Do not start from a conclusion.

There is no fill-in-the-blank positioning statement in this output. The six parts are the positioning.

## Method
1. **Competitive alternatives.** What would the best-fit customer do if this did not exist? Include doing nothing, doing it by hand, native tools and other vendors. These are what customers compare against, not only direct competitors. For each, say why people choose it and where it stops. Sources: `context/company.md`, the PRD, `02-launch-context.md`. Anything else is `[NEED PROOF: ...]`.
2. **Unique attributes.** Capabilities the alternatives lack, taken from the PRD. Only attributes you can source. If you cannot verify the comparison, say the attribute is "not yet confirmed as unique".
3. **Value and proof.** For each unique attribute, what does it let the customer do that matters to them? Then the proof: an approved proof point, a PRD fact, or `[NEED PROOF: ...]`.
4. **Best-fit customers.** Who cares most about that value, and what do they look like? Use `03-audience.md` and refine it from steps 1 to 3.
5. **Market category.** The frame of reference that makes the value obvious. Consider two or three options, choose one, and say what it makes customers assume (good and bad). Do not coin a category with no basis.
6. **Relevant trends.** Trends that make the category matter now. Use only trends in `context/company.md` or the PRD. Do not invent market data.

Then write what this means for messaging: the three or four ideas messaging must carry. This is a handoff, not a statement.

## Output template

```
# Positioning: <release name>

## 1. Competitive alternatives
| Alternative | Why customers pick it | Where it stops | Source |
|---|---|---|---|
| Do nothing | | | |
| Do it by hand | | | |
| Native tool | | | |
| Other tools | | | |

## 2. Unique attributes
| Attribute | Alternatives that lack it | Confirmed? | Source |
|---|---|---|---|

## 3. Value and proof
| Attribute | Value to the customer | Proof | Source |
|---|---|---|---|

## 4. Best-fit customers
<who cares most, observable signals, who does not>

## 5. Market category
- **Options considered:** ...
- **Chosen frame:** ...
- **What it makes customers assume:** ...
- **Risk:** ...

## 6. Relevant trends
- <trend, source, why it makes this matter now>

## What this means for messaging
- ...

## Open questions
- ...
```
