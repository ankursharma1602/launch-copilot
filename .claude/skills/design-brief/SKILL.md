---
name: design-brief
description: Write ready-to-paste design prompts for Claude Design or Canva for each visual asset a launch tier needs, with size, exact on-image text from the channel copy, layout, visual direction and things to avoid. Use when turning final channel copy into briefs for visuals.
---

# Design brief

## Method
1. Check the "Visual assets" rows in the asset matrix in `context/tiering.md`. Produce only the assets this tier gets. List the skipped ones at the top so a reader knows it was deliberate.
2. For each asset, pick the on-image text from `03-channel-copy.md`. Copy it exactly. You may cut words. You may not rewrite or add. Name the source section next to the text.
3. Keep on-image text under 30 words per asset, counting every visible word.
4. Lead with the primary persona's moment or the outcome they get back. The image supports the headline. It does not repeat the whole message.
5. Write each prompt so it works pasted into Claude Design or Canva with no other context.
6. Check `learnings/lessons.md` and apply every relevant lesson.

## Asset specs
| Asset | Size (px) | Notes |
|---|---|---|
| Email header | 1200 x 400 | Shows at 600 px wide in the inbox. Text must stay legible at half size. Keep key text away from the edges. |
| In-app banner | 1280 x 320 | Sits above or beside the in-app message. The message text carries the detail, the banner carries the headline only. |
| LinkedIn image | 1200 x 627 | Must work next to the post text without repeating it. Leave a safe margin of 60 px. |
| One-pager layout | 2550 x 3300 (US Letter at 300 dpi) | A layout brief. The headline and subhead are the on-image text (under 30 words). Body sections are slots, filled by pasting from the sales one-pager in `04-sales-enablement.md`. Do not rewrite them. |
| Blog hero image | 1600 x 900 | Tier 1 only. Text-light. A short title or none. |

## Rules for on-image text
- Headlines say what the customer gets, not what the feature is called.
- Limits the brief says every asset must state stay in the asset's body copy. If an image sits with copy that carries them (in-app message, email, LinkedIn post), the image does not need to repeat them, but it must not contradict them. State this in the prompt, for example "does not claim support beyond Jira Cloud".
- No em dashes, no exclamation marks, no banned words from `context/voice.md`.
- No numbers, customer names, quotes or dates unless they are in the copy and approved. Anything missing is `[NEED PROOF: ...]`.

## Visual direction rules
- Calm and clear. Light backgrounds, generous space, one idea per image.
- Show the mechanism, not the fear: for example one actor's changes lifted out of a timeline while everyone else's stay put. Use abstract shapes, simple timelines and schematic issue cards with placeholder text.
- Product UI is allowed only as a schematic with blurred or placeholder content. Never invent real-looking screenshots, ticket numbers, counts or user names.
- Use the brand palette, fonts and logo from the company. They are not in `context/`, so write `[NEED PROOF: brand palette, fonts and logo files]` in the prompt until supplied.

## What to avoid (include in every prompt, adjusted per asset)
- Red alarms, warning triangles, skulls, glitch effects, anything that sells fear.
- Robots, glowing brains, sci-fi AI imagery.
- Stock photos of people pointing at screens.
- Any logo or mark of Atlassian, Jira or another vendor, unless brand rules for using it are supplied.
- Text on image beyond the approved lines. No lorem ipsum in a final image.
- Words on the banned list in `context/voice.md`.

## Output template

````
# Design briefs: <release name> (Tier <x>)

**Produced for this tier:** <list>
**Deliberately skipped:** <list>
**Source copy:** 03-channel-copy.md
**Open inputs:** <each [NEED PROOF: ...] collected here>

## <Asset name>
**Size:** <width> x <height> px
**Used with:** <the copy asset it sits beside>
**On-image text** (<n> words, from <section of 03-channel-copy.md>):
> <exact text>

**Prompt (paste into Claude Design or Canva):**
```
<Complete prompt. Start with the asset name and size. Then the exact on-image text in quotes, the layout (where each element sits, text size order), the visual direction, the brand note, and the avoid list.>
```

**Layout:** <one line per zone, for a human reading the brief>
**Visual direction:** <one or two lines>
**Avoid:** <the list for this asset>

---
(one section per asset)
````
