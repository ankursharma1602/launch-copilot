---
name: messaging
description: Derive messaging from positioning: core message, value pillars with proof, and angles per persona. Use when turning positioning into words that every channel will reuse.
---

# Messaging

Messaging is how positioning sounds. Every message here must trace back to `04-positioning.md`. If a message needs support the positioning does not have, report a positioning gap. Do not invent the claim.

## Method
1. Write the core message: one sentence, what the customer gets. Problem first, then capability, then proof.
2. Write three value pillars. Each comes from a row in the positioning's value and proof table. Each has a claim, a proof (approved, from the PRD, or `[NEED PROOF: ...]`) and the source.
3. For each persona in `03-audience.md`, write an angle: what to lead with, which pillar, which words, which proof, what to avoid.
4. Write the "Must say" list: the limitations from `02-launch-context.md` that every asset repeats, in the exact wording to use.
5. List vocabulary: words to use (admin language) and words to avoid (`context/voice.md` banned list, plus any term the positioning rules out).
6. Check the headlines: they say what the customer gets, not what the feature is called.

## Output template

```
# Messaging: <release name>

## Core message
<one sentence> 
Support: <one sentence>

## Value pillars
| Pillar | Claim | Proof | Source |
|---|---|---|---|
| 1. | | | |
| 2. | | | |
| 3. | | | |

## Angles by persona
### <Persona>
- **Lead with:** ...
- **Pillar:** ...
- **Words to use:** ...
- **Proof to use:** ...
- **Avoid:** ...

## Must say (limitations every asset repeats)
1. <exact wording>

## Vocabulary
- **Use:** ...
- **Avoid:** ...

## Traceability
| Message | Comes from (04-positioning.md section) |
|---|---|

## Positioning gaps found
- ...
```
