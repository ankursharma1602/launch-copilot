---
name: audience
description: Define the best-fit segments and personas for a launch from the personas in context/ and the launch context. Use when deciding who a launch is for and who it is not for.
---

# Audience

## Method
1. Start from `context/personas.md`. Do not add personas. Sharpen the ones that matter for this launch.
2. Choose one primary persona and at most one secondary. Say why, using the launch context. Name who is deliberately out of focus.
3. For the primary persona, write the trigger: the moment this launch becomes relevant to them. Use their language from the persona file.
4. Define best-fit segments with signals a salesperson or marketer could actually observe (for example, rolling out AI agents in Jira Cloud). Use only criteria from the PRD and `context/`. Sizes, shares and counts need a source or `[NEED PROOF: ...]`.
5. Map the buying group: who uses it, who approves it, who influences it.
6. Never frame the AI or automation owner as the problem. They are the person who gets to say yes to AI.

## Output template

```
# Audience: <release name>

## Primary persona: <persona>
- **Why primary:** ...
- **Trigger moment:** ...
- **What they own / fear / want:** ...
- **Their words:** ...
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
