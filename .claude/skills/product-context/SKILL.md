---
name: product-context
description: Turn a closed beta handoff into launch-ready context: what is built, what closed beta customers said, limitations, availability, dependencies and gaps, kept separate. Use when later agents need a trustworthy, customer-language source of facts.
---

# Closed beta handoff to launch context

A closed beta handoff is what a PM shares with a PMM when a feature in closed beta is heading to GA. It has two kinds of evidence: what has been built, and what closed beta customers have said. Keep them apart. Everything written later builds on this file. If a fact is not here, downstream agents should not state it.

## Method
1. Read the closed beta handoff end to end. Sort what you find into two piles:
   - **Built:** the epic and user stories, the release notes, the demo notes, availability, known limitations.
   - **Said:** the beta stats, customer feedback and quotes, and the open questions from the Slack thread.
2. Built pile. Rewrite each capability in customer terms: what can the customer do now that they could not do before? Name the real objects (issues, fields, projects, automation rules). Every capability must trace to the epic, release notes or demo notes.
3. Pull out every limitation. State each plainly, in one sentence, as the handoff states it. Mark which ones copy must always repeat ("must say").
4. Record availability: plans, platforms, date, and anything promised "later" with no commitment. Do not turn a roadmap hint into a promise.
5. List dependencies: other teams, other launches, data or permissions the customer needs.
6. Said pile. Report the beta numbers as given, with the sample size and what was measured. Then pull from the feedback:
   - who got the most value (role, company type, situation)
   - the words customers used for the problem and the value
   - what they compared it to, or used before
   - what confused them, what they asked for and what they did not use
   Quote only what the handoff quotes. Keep each quote attributed to a role, never a name.
7. Mark the feedback status. If the handoff labels feedback as mock, say so at the top of that section. Beta stats and quotes are not approved proof points. Any external use is `[NEED PROOF: approval to use closed beta results or quotes]`.
8. Note beta-to-GA differences: anything in beta that may change, and anything the Slack thread leaves open.
9. List gaps: anything an asset would need that the handoff does not say. Each is `[NEED PROOF: ...]` with who could answer.
10. Compare with `context/`. If the handoff and `context/` disagree, record both versions and flag it. Do not pick.

## Output template

```
# Launch context: <release name>

## What's shipping
<one paragraph, plain>

## What's built
### Capabilities in customer terms
| Handoff capability | What the customer can do | Source in handoff | Matters most to |
|---|---|---|---|

### Limitations
1. <plain sentence> | Must say: yes/no
2. ...

### Availability
- Plans: ...
- Platforms: ...
- Date: ...
- Not committed: ...

### Dependencies
- ...

## What closed beta customers said
> Status of this feedback: <real or mock, as the handoff labels it>. Internal evidence. Not an approved proof point.

### Beta numbers
| Measure | Value | Sample and period | Source in handoff |
|---|---|---|---|

### Who got the most value
- ...

### The language customers used
- <their words for the problem and the value, with role>

### What they compared it to
- ...

### Friction and requests
- ...

## Beta to GA
- <what may change, what the Slack thread leaves open>

## Gaps (need an answer before launch)
| Gap | Why it matters | Who can answer |
|---|---|---|

## Where the closed beta handoff and context/ disagree
- <both versions, and what a human must decide>
```
