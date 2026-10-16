---
name: design-brief
description: Write a design brief for each visual a launch tier needs, then render each as an SVG and convert it to PNG, using the exact on-image text from the channel copy. Use when turning final copy into finished visuals.
---

# Design brief and render

## Method
1. Check the "Visual assets" rows in the asset matrix in `context/tiering.md`. Produce only what this tier gets. List the skipped ones at the top.
2. Choose the on-image text from `07-channel-copy.md`. Copy it exactly. You may cut words. You may not rewrite or add. Name the source section.
3. Keep on-image text under 30 words per visual, counting every visible word.
4. Write the brief (template below), then render the visual from it.
5. Check `learnings/lessons.md` and apply every relevant lesson.

## Asset specs
| Asset | Size (px) | Notes |
|---|---|---|
| Email header | 1200 x 400 | Shows at 600 px wide in the inbox. Text must stay legible at half size. |
| In-app banner | 1280 x 320 | Sits above or beside the in-app message. The headline only. |
| LinkedIn image | 1200 x 627 | Works next to the post text without repeating it. 60 px safe margin. |
| One-pager layout | 2550 x 3300 | US Letter at 300 dpi. Headline and subhead are the on-image text. Body sections are empty blocks with no text, to be filled from `09-sales-enablement.md`. |
| Blog hero image | 1600 x 900 | Tier 1 only. Text-light. A short title or none. |

## Style
- Clean and modern. Light background, generous space, one idea per image, strong type hierarchy (headline clearly largest).
- Fonts: a system sans stack, `Helvetica Neue, Helvetica, Arial, sans-serif`. No web fonts, so the render works offline.
- Brand colors, fonts and logo are not in `context/`. Use a neutral placeholder palette: dark slate for text, light grey background, one accent. Mark it as a placeholder in the brief and in an SVG comment (`<!-- PLACEHOLDER BRAND COLORS: replace with brand palette -->`). Add `[NEED PROOF: brand palette, fonts and logo files]` to the brief. Do not draw a logo. Leave a clearly empty logo area only if the layout needs one.
- Show the mechanism, not the fear: one actor's changes lift out of a timeline while everyone else's work stays in place. Use abstract shapes and schematic cards with no real-looking text, counts or ticket numbers.
- The AI agent is one neutral actor among others, never a villain.

## What to avoid
- Red alarms, warning triangles, skulls, glitch effects, anything that sells fear.
- Robots, glowing brains, sci-fi AI imagery, stock photos of people at screens.
- Any logo or mark of Atlassian, Jira or another vendor.
- Text on the image beyond the approved lines. No lorem ipsum.
- Words from the banned list in `context/voice.md`.
- Implying support beyond what `02-launch-context.md` says. The limitations stay in the body copy the image sits beside. The image must not contradict them.

## Render method
1. Write `visuals/<asset-name>.svg` in the output folder. Set `width`, `height` and `viewBox` to the exact pixel size. Wrap long text by hand with `<tspan>` lines. Estimate about 0.55 x font size per character and keep every line inside the safe margin.
2. Convert to PNG at the same pixel size. Use the first tool that works:
   - Headless Chrome:
     `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --hide-scrollbars --force-device-scale-factor=1 --window-size=<W>,<H> --screenshot=<abs path>.png "file://<abs path>.svg"`
   - macOS `qlmanage -t -s <longest side> -o <folder> <file>.svg`, which writes `<file>.svg.png`. Rename it.
3. Check the result: run `sips -g pixelWidth -g pixelHeight <png>` and confirm it matches the spec. If a headless window adds browser chrome and the size is off, adjust the window size or crop with `sips`.
4. Open the PNG with the Read tool and look at it. Text must not be clipped, overlap or fall outside the margin. Fix the SVG and re-render if it does.
5. If no tool works, keep the SVG, say so in the brief, and do not claim a PNG exists.
6. Keep any helper script in the scratchpad, not the project folder.

## Output template

````
# Design briefs: <release name> (Tier <x>)

**Produced for this tier:** <list>
**Deliberately skipped:** <list>
**Source copy:** 07-channel-copy.md
**Style note:** Placeholder brand colors in use. [NEED PROOF: brand palette, fonts and logo files]

## <Asset name>
**Size:** <width> x <height> px
**Used with:** <the copy asset it sits beside>
**On-image text** (<n> words, from <section of 07-channel-copy.md>):
> <exact text>

**Layout:** <one line per zone>
**Visual direction:** <one or two lines>
**Palette (placeholder):** <hex values, labelled placeholder>
**Avoid:** <the list for this asset>
**Does not claim:** <the limitation the image must not contradict>

**Prompt (paste into Claude Design or Canva):**
```
<Complete prompt: asset name and size, the exact on-image text in quotes, layout, visual direction, placeholder palette note, avoid list.>
```

**Render:** `visuals/<name>.svg`, `visuals/<name>.png` | Tool: <tool> | Size check: <w x h, match yes/no> | Visual check: <what was checked>

---
(one section per visual)
````
