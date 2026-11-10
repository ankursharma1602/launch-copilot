---
name: messaging
description: Derive messaging from positioning: core message, value pillars with proof, and angles per persona. Use when turning positioning into words that every channel will reuse.
---

# Messaging

Messaging is how positioning sounds. Every message here must trace back to `05-positioning.md`. If a message needs support the positioning does not have, report a positioning gap. Do not invent the claim.

## Method
1. Write the core message: one sentence, what the customer gets. Problem first, then capability, then proof.
2. Write three value pillars. Each comes from a row in the positioning's value and proof table. Each has a claim, a proof (approved, from the closed beta handoff, or `[NEED PROOF: ...]`) and the source.
3. For each persona in `04-audience.md`, write an angle: what to lead with, which pillar, which words, which proof, what to avoid.
4. Write the "Must say" list: the limitations from `02-launch-context.md` that every asset repeats, in the exact wording to use.
5. List vocabulary: words to use (the customer's own language) and words to avoid (`context/voice.md` banned list, plus any term the positioning rules out).
6. Check the headlines: they say what the customer gets, not what the feature is called.

## Showcase output: the messaging framework
The file is written as a document a PMM shares with Sales and Marketing. Order:
1. The one-line value proposition.
2. Three pillars, each with its message, supporting points and proof. Where proof is missing, write the pillar anyway and add the gap to the Open questions list at the end, not inline.

Keep the framework tight: no notes to writers inside pillars, an "Avoid saying" list of at most 6 lines, and the whole file readable in 5 minutes. Messages are for the generally available product.
3. A message matrix: rows are personas, columns are headline, key benefit, proof, CTA.
4. An "Avoid saying" list.
Then the Must say list, vocabulary, traceability and positioning gaps.

## Output template

```
# Messaging: <release name>

## One-line value proposition
<one sentence: problem, then capability, then proof>

## Three pillars
### Pillar 1: <name>
- **Message:** ...
- **Supporting points:** ...
- **Proof:** <approved proof, handoff fact, or [NEED PROOF: ...]>
### Pillar 2: <name>
(same)
### Pillar 3: <name>
(same)

## Message matrix
| Persona | Headline | Key benefit | Proof | CTA |
|---|---|---|---|---|

## Avoid saying
- <phrase or claim, and why>

## Angles by persona (detail behind the matrix)
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
| Message | Comes from (05-positioning.md section) |
|---|---|

## Positioning gaps found
- ...
```
