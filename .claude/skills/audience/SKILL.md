---
name: audience
description: Define the best-fit segments and personas for a launch from the personas in context/ and the launch context. Use when deciding who a launch is for and who it is not for.
---

# Audience

## Method
1. Start from `context/personas.md`. Do not add personas. Sharpen the ones that matter for this launch.
   Then read the closed beta feedback in `02-launch-context.md`: who got the most value, the language customers used, and what they compared it to. Treat it as a primary input. Where it confirms a persona, say so. Where it differs, say so and follow the evidence.
2. Choose one primary persona and at most one secondary. Say why, using the launch context. Name who is deliberately out of focus.
3. For the primary persona, write the trigger: the moment this launch becomes relevant to them. Use the words closed beta customers used, then the persona file.
4. Define best-fit segments with signals a salesperson or marketer could actually observe (for example, rolling out AI agents in Jira Cloud). Use only criteria from the closed beta handoff (including the beta feedback) and `context/`. Beta feedback is a small sample: say "in closed beta", never present it as a market pattern. Sizes, shares and counts need a source or `[NEED PROOF: ...]`.
5. Map the buying group: who uses it, who approves it, who influences it.
6. Never frame the AI or automation owner as the problem. They are the person who gets to say yes to AI.

## Output template

```
# Audience: <release name>

## Primary persona: <persona>
- **Why primary:** ...
- **What closed beta showed:** <who got the most value, and how that supports or changes the persona>
- **Trigger moment:** ...
- **What they own / fear / want:** ...
- **Their words:** <from closed beta customers, attributed to a role, then the persona file>
- **What turns them off:** ...

## Secondary persona: <persona or none>
- **Why:** ...

## Best-fit segments
| Segment | Signals to look for | Why they fit | Evidence |
|---|---|---|---|

## Buying group
| Role | Persona | Part in the decision |
|---|---|---|

## Out of focus for this launch
- <who, and why>

## Open questions
- ...
```
