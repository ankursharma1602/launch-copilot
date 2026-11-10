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
4. Define best-fit segments with signals a salesperson or marketer could actually observe (for example, a firm size, a tool in use or a behaviour named in the handoff). Use only criteria from the closed beta handoff (including the beta feedback) and `context/`. Beta feedback is a small sample: say "in closed beta", never present it as a market pattern. Sizes, shares and counts need a source or `[NEED PROOF: ...]`.
5. Map the buying group: who uses it, who approves it, who influences it.
6. Never frame the AI or automation owner as the problem. They are the person who gets to say yes to AI.

## Showcase output: Illustrative personas
Write one table, labelled "Illustrative personas". The first column is headed "Target Audience" and holds the row names. Then one column per persona (2 or 3), each with an alliterative role name such as "Solo Sam" (a label for an archetype, not a person). Rows, in this order: Age, Location, Job title(s), Role/Influence (User, Auditor, Implementation, Approver), Responsibilities, Firm size/revenue, Practice area, Tech stack, Time spent on the task per day, JTBD, Challenge(s), Current solution, Preferred channels, Content types.

Rules:
- The personas are archetypes from `context/personas.md`, the research and the mock handoff. No real people or firms.
- Every cell gets a specific, realistic value, the way a PMM writes a persona: for example "41", "Austin, TX", "6 people ($1.2M revenue)", "Family law", "45 minutes a day", "LinkedIn, Clio blog, state bar newsletters". These are illustrative archetype details, covered by the "Illustrative personas" label. Ground them in the handoff, `context/` and how small and mid-size law firms actually work. Never write [NEED PROOF] or "no data" in this table.
- One short idea per cell. No sources, caveats or parentheses inside cells.
- Style it like a clean presentation table: light background, persona header cells in brand colours, generous spacing, no more text than fits comfortably at 1920x1080.
- Render the same table as a PNG at `visuals/audience-personas.png` (and `.svg`) using only the colours in `context/brand.md`. Each persona's header uses its own brand colour (three different brand colours from that file), with text that passes contrast. Follow the render method in `.claude/skills/design-brief/SKILL.md` and open the PNG to check it is not clipped. If you show a wordmark, set it as live text per `context/brand.md`, never a logo.
- Label the PNG "Illustrative personas".

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

## Illustrative personas
| Target Audience | <Persona 1 name> | <Persona 2 name> | <Persona 3 name, optional> |
|---|---|---|---|
| Age | | | |
| Location | | | |
| Job title(s) | | | |
| Role/Influence | | | |
| Responsibilities | | | |
| Firm size/revenue | | | |
| Practice area | | | |
| Tech stack | | | |
| Time spent on the task per day | | | |
| JTBD | | | |
| Challenge(s) | | | |
| Current solution | | | |
| Preferred channels | | | |
| Content types | | | |

![Illustrative personas](visuals/audience-personas.png)
```
