---
name: design-brief
description: Write a design brief for each visual a launch tier needs, then render each as an SVG and convert it to PNG, using the exact on-image text from the channel copy. Use when turning final copy into finished visuals.
---

# Design brief and render

## Method
1. Check the "Visual assets" rows in the asset matrix in `context/tiering.md`. Produce only what this tier gets. List the skipped ones at the top.
2. Choose the on-image text from `08-channel-copy.md`. Copy it exactly. You may cut words. You may not rewrite or add. Name the source section.
3. Keep on-image text under 30 words per visual, counting every visible word, including the wordmark. The one-pager layout is a page, not a banner: it may carry up to about 90 words, with real content in every card, no empty placeholder shapes.
   Limitations and disclaimers never go on email header, in-app banner or LinkedIn images. They stay in the accompanying copy (the email, in-app message and post). Only the one-pager layout may carry a small limits line (one short line, in a footer or small box).
4. Read `context/brand.md`. Apply its colours, typeface, wordmark rule and visual style to every visual.
5. Write the brief (template below), then render the visual from it.
6. Check `learnings/lessons.md` and apply every relevant lesson.

## Asset specs
| Asset | Size (px) | Notes |
|---|---|---|
| Email header | 1200 x 560 | Shows at 600 px wide in the inbox. Carries the compact flow, so it is taller than a plain banner. Text must stay as legible as the canvas allows at half size. |
| In-app banner | 1280 x 420 | Sits above or beside the in-app message. Headline, subline, button and the compact flow. |
| LinkedIn image | 1200 x 627 | Works next to the post text without repeating it. 60 px safe margin. |
| One-pager layout | 2550 x 3300 | US Letter at 300 dpi. Headline and subhead are the on-image text, plus one small limits line. Body sections are empty blocks with no text, to be filled from `10-sales-enablement.md`. |
| Blog hero image | 1600 x 900 | Tier 1 only. Text-light. A short title or none. |

## Style
Follow `context/brand.md`. In every visual:
- **Colours:** only the hex codes in `context/brand.md` (primary, secondary, neutrals), and tints of those for schematic shapes. Follow the accent, type and contrast rules in that file.
- **Typeface:** the brand typeface and stand-in rule in `context/brand.md`. Inter is installed as the family "Inter Variable", so set `font-family="'Inter Variable', Inter, sans-serif"` and weights as brand.md says (headlines 200 or 300). Check the PNG shows real thin Inter, not a fallback: test by temporarily using a monospace fallback, which turns monospace if Inter is missing. The brief says the typeface is a stand-in for Facility.
- **Headlines use the customer's words**, never internal jargon. If the on-image text in `08-channel-copy.md` uses an internal term, flag it in the brief and ask for a fix; do not rewrite it yourself.
- **Wordmark:** the company name set as live text in the brand typeface, in the wordmark colour `context/brand.md` gives for the background, top left, with clear space. Do not download or embed the company's logo file, and do not draw or trace the logo or any brand mark. Say in the brief: "Wordmark set in type, not the official logo file."
- **Style:** follow `context/brand.md` exactly. Launch and social images (email header, LinkedIn image, in-app banner) use the black minimal pattern in its "Launch and social assets" section: a white mono pill label at the top centre and a thin centred white headline of at most two short lines. Instead of an abstract object, show ONE clean product card in the lower half: a drafted time entry on a #191919 card (matter name, a short activity line, a duration) with a Clio blue #1A56FF Bill-ready toggle switched on; flat, crisp, generous padding, small radius, no shadow and no cartoon shapes. The wordmark goes top left: if `assets/clio-logo.svg` or `.png` exists, place it unaltered with clear space; otherwise set "Clio" as live text per brand.md. The in-app banner may add its one Clio blue button. Long-read visuals (persona table, one-pager) use a white canvas with a black header band, ink text and tint header fills. Open every PNG and compare it with brand.md before you finish.
- Product visuals are one clean UI card, as brand.md says. The card text is illustrative and generic: no real person or firm names, no ticket numbers.
- The typeface is a stand-in for Facility (see `context/brand.md`). Say so in the brief. No flags or caveats appear on the image.

## What to avoid
- Red alarms, warning triangles, skulls, glitch effects, anything that sells fear.
- Robots, glowing brains, sci-fi AI imagery, stock photos of people at screens.
- Any logo or mark of another vendor or partner.
- Text on the image beyond the approved lines. No lorem ipsum.
- Words from the banned list in `context/voice.md`.
- Limitations, disclaimers, plan names and "only X" caveats on email header, in-app banner or LinkedIn images. They stay in the accompanying copy. The image must not contradict them.
- Implying support beyond what `02-launch-context.md` says.
- The company's logo file, a traced or redrawn logo, or any brand mark.

## Render method
1. Write `visuals/<asset-name>.svg` in the output folder. Set `width`, `height` and `viewBox` to the exact pixel size. Wrap long text by hand with `<tspan>` lines. Estimate about 0.55 x font size per character and keep every line inside the safe margin.
2. Convert to PNG at the same pixel size. Use the first tool that works:
   - Headless Chrome:
     `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --hide-scrollbars --force-device-scale-factor=1 --window-size=<W>,<H> --screenshot=<abs path>.png "file://<abs path>.svg"`
   - macOS `qlmanage -t -s <longest side> -o <folder> <file>.svg`, which writes `<file>.svg.png`. Rename it.
3. Check the result: confirm the text renders in the brand typeface and not the fallback font, then run `sips -g pixelWidth -g pixelHeight <png>` and confirm it matches the spec. If a headless window adds browser chrome and the size is off, adjust the window size or crop with `sips`.
4. Open the PNG with the Read tool and look at it. Text must not be clipped, overlap or fall outside the margin. Fix the SVG and re-render if it does.
5. If no tool works, keep the SVG, say so in the brief, and do not claim a PNG exists.
6. Keep any helper script in the scratchpad, not the project folder.

## Output template

````
# Design briefs: <release name> (Tier <x>)

**Produced for this tier:** <list>
**Deliberately skipped:** <list>
**Source copy:** 08-channel-copy.md
**Style note:** Brand from `context/brand.md`. Wordmark set in type, not the official logo file. Typeface is a stand-in for Facility.

## <Asset name>
**Size:** <width> x <height> px
**Used with:** <the copy asset it sits beside>
**On-image text** (<n> words, from <section of 08-channel-copy.md>):
> <exact text>

**Layout:** <one line per zone>
**Visual direction:** <one or two lines>
**Brand applied:** <colours as hex from context/brand.md, typeface, wordmark colour and position>
**Avoid:** <the list for this asset>
**Does not claim:** <the limitation the image must not contradict>

**Prompt (paste into Claude Design or Canva):**
```
<Complete prompt: asset name and size, the exact on-image text in quotes, layout, visual direction, brand hex codes and typeface, wordmark rule, avoid list.>
```

**Render:** `visuals/<name>.svg`, `visuals/<name>.png` | Tool: <tool> | Size check: <w x h, match yes/no> | Visual check: <what was checked>

---
(one section per visual)
````
