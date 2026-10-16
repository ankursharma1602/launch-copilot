---
name: prd-context
description: Turn a PRD into launch-ready context: what is shipping, capabilities in customer terms, limitations, availability, dependencies and gaps. Use when later agents need a trustworthy, customer-language source of facts.
---

# PRD to launch context

Everything written later builds on this file. If a fact is not here, downstream agents should not state it.

## Method
1. Read the PRD end to end. List every capability, constraint, plan, platform and date it states.
2. Rewrite each capability in customer terms: what can the customer do now that they could not do before? Name the real objects (issues, fields, projects, automation rules).
3. Pull out every limitation. State each plainly, in one sentence, as the PRD states it. Mark which ones copy must always repeat ("must say").
4. Record availability: plans, platforms, date, and anything promised "later" with no commitment. Do not turn a roadmap hint into a promise.
5. List dependencies: other teams, other launches, data or permissions the customer needs.
6. List gaps: anything an asset would need that the PRD does not say. Each is `[NEED PROOF: ...]` with who could answer.
7. Compare with `context/`. If the PRD and `context/` disagree, record both versions and flag it. Do not pick.

## Output template

```
# Launch context: <release name>

## What's shipping
<one paragraph, plain>

## Capabilities in customer terms
| PRD capability | What the customer can do | Matters most to |
|---|---|---|

## Limitations
1. <plain sentence> | Must say: yes/no
2. ...

## Availability
- Plans: ...
- Platforms: ...
- Date: ...
- Not committed: ...

## Dependencies
- ...

## Gaps (need an answer before launch)
| Gap | Why it matters | Who can answer |
|---|---|---|

## Where the PRD and context/ disagree
- <both versions, and what a human must decide>
```
