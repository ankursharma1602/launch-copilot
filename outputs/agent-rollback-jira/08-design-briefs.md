# Design briefs: Agent Rollback for Jira (Tier 2)

**Produced for this tier:** email header, in-app banner, LinkedIn image, one-pager layout.
**Deliberately skipped:** blog hero image (Tier 1 only).
**Source copy:** 07-channel-copy.md, section "On-image text". Text is copied unchanged, nothing cut or added.
**Style note:** Brand from `context/brand.md`. Wordmark set in type, not the official logo file. [NEED PROOF: confirm brand palette and typeface with Rewind's brand team] The Boomerang yellow is not used because its hex is unknown. No visual leaves the team until the brand team confirms.

**Shared visual idea (all four):** a white schematic card with three lanes. The middle lane is the one actor. Its solid Blue Zodiac blocks lift out of the lane, leaving dashed outlines in place. The other lanes, in 20% tints of Blue Zodiac, stay untouched. No text, counts or ticket numbers inside the card. The actor is neutral, not a villain.

**Font:** Cabin loaded through a Google Fonts `@import` in each SVG, with the brand fallback stack. Confirmed by viewing every PNG: the glyphs are Cabin, not the fallback. The SVG needs internet access to show Cabin when opened elsewhere. The PNGs are fixed.

**Tool for all four:** headless Google Chrome, 1x scale.

## Email header
**Size:** 1200 x 400 px
**Used with:** Customer email
**On-image text** (13 words, from 07 "Email header"):
> Rewind
> Undo the one change, not the whole site.
> Agent Rollback for Jira

**Layout:** wordmark top left (44 px); headline two lines at 58 px, left; supporting line 28 px below; schematic card right (420 x 300).
**Visual direction:** Link Water canvas, one idea, generous space. Legible at half size (headline reads about 29 px).
**Brand applied:** #F5F8FD canvas, #16225C wordmark and headline, #0E102B supporting line, #FFFFFF card, Blue Zodiac tints for shapes. Cabin 700 headline and wordmark, Cabin 500 supporting line. Wordmark set in type, not the official logo file.
**Avoid:** limitations, plan names, "only" claims, alarms, robots, any vendor logo, the Boomerang mark.
**Does not claim:** Jira Cloud only, changes after the first backup, issues and fields only, the attachment limit, plan tier. These stay in the email.

**Prompt (paste into Claude Design or Canva):**
```
Email header, 1200 x 400 px. Light background #F5F8FD. Top left, the word "Rewind" as live text in Cabin 700, #16225C, 44 px, with clear space. Not a logo. Headline in two lines, Cabin 700, #16225C, 58 px: "Undo the one change, not the whole site." Below it, Cabin 500, #0E102B, 28 px: "Agent Rollback for Jira". Right side: a white rounded card with three horizontal lanes. Outer lanes hold pale blocks (#16225C at 20%). The middle lane's three blocks are solid #16225C and lifted above the lane, joined by thin lines to dashed outlines left in place. No text in the card. No other text, no logos, no robots, no alarms, no yellow.
```
**Render:** `visuals/email-header.svg`, `visuals/email-header.png` | Tool: headless Chrome | Size check: 1200 x 400, match yes | Visual check: Cabin renders, nothing clipped or overlapping, margins at least 60 px.

---

## In-app banner
**Size:** 1280 x 320 px
**Used with:** In-app message
**On-image text** (13 words, from 07 "In-app banner"):
> Rewind
> Undo what one rule or AI agent changed.
> See the effect first.

**Layout:** wordmark top left (40 px); headline two lines at 50 px; supporting line 26 px; schematic card right (420 x 260).
**Visual direction:** same schematic, headline only, calm and compact.
**Brand applied:** #F5F8FD canvas, #16225C wordmark and headline, #0E102B supporting line, #FFFFFF card, tints of #16225C. Cabin 700 / 500. Wordmark set in type, not the official logo file.
**Avoid:** limitations, attachment note, plan tier, alarms, robots, vendor logos, the Boomerang mark.
**Does not claim:** the Jira Cloud, first-backup, 24-hour attachment and plan-tier limits in the in-app body copy.

**Prompt (paste into Claude Design or Canva):**
```
In-app banner, 1280 x 320 px. Background #F5F8FD. Top left, "Rewind" as live text, Cabin 700, #16225C, 40 px. Headline, two lines, Cabin 700, #16225C, 50 px: "Undo what one rule or AI agent changed." Below, Cabin 500, #0E102B, 26 px: "See the effect first." Right: white rounded card with three lanes; outer lanes pale blocks (#16225C at 20%); middle lane's solid #16225C blocks lifted out, dashed outlines left behind. No text in the card. No other text or logos.
```
**Render:** `visuals/in-app-banner.svg`, `visuals/in-app-banner.png` | Tool: headless Chrome | Size check: 1280 x 320, match yes | Visual check: Cabin renders, nothing clipped.

---

## LinkedIn image
**Size:** 1200 x 627 px
**Used with:** LinkedIn post (the post carries the limits)
**On-image text** (17 words, from 07 "LinkedIn image"):
> Rewind
> Undo the one actor, not the whole site.
> See what will change back before you restore.

**Layout:** 60 px safe margin. Wordmark top left (44 px); headline two lines at 64 px; supporting line two lines at 30 px; schematic card right (420 x 400).
**Visual direction:** same schematic, larger card. Does not repeat the post text.
**Brand applied:** #F5F8FD, #16225C, #0E102B, #FFFFFF, tints of #16225C. Cabin 700 / 500. Wordmark set in type, not the official logo file.
**Avoid:** limitations, disclaimers, plan names, alarms, robots, people at screens, vendor logos, the Boomerang mark.
**Does not claim:** Jira Cloud, first-backup, issues and fields, attachment 24-hour and plan-tier limits stated in the post.

**Prompt (paste into Claude Design or Canva):**
```
LinkedIn image, 1200 x 627 px, 60 px safe margin. Background #F5F8FD. Top left "Rewind" as live text, Cabin 700, #16225C, 44 px. Headline, two lines, Cabin 700, #16225C, 64 px: "Undo the one actor, not the whole site." Supporting line, Cabin 500, #0E102B, 30 px: "See what will change back before you restore." Right: white rounded card, three lanes, outer lanes pale (#16225C at 20%), middle lane's solid #16225C blocks lifted out with dashed outlines left behind. No text in the card, no other text, no logos.
```
**Render:** `visuals/linkedin-image.svg`, `visuals/linkedin-image.png` | Tool: headless Chrome | Size check: 1200 x 627, match yes | Visual check: Cabin renders, inside safe margin, nothing clipped.

---

## One-pager layout
**Size:** 2550 x 3300 px
**Used with:** One-pager in 09-sales-enablement.md
**On-image text** (about 29 words including the wordmark, from 07 "One-pager layout"):
> Rewind
> Undo what one rule or AI agent changed.
> See what changes back first.
> Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier.

**Layout:** wordmark top left (84 px); headline two lines at 150 px; supporting line 64 px; wide schematic card (2250 x 620); four empty white body blocks in a 2 x 2 grid, each with one short tint bar and no text, to be filled from 09; thin rule and one small limits line (40 px) in the footer.
**Visual direction:** structure over decoration. The empty blocks stay empty.
**Brand applied:** #F5F8FD, #16225C, #0E102B, #FFFFFF, tints of #16225C. Cabin 700 / 500 / 400. Wordmark set in type, not the official logo file.
**Avoid:** extra text, lorem ipsum, beta numbers, quotes, customer names, alarms, robots, vendor logos, the Boomerang mark.
**Does not claim:** the attachment limit does not fit the one small line. It must be carried in the body blocks from 09. The image must not imply attachments are covered without it. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]

**Prompt (paste into Claude Design or Canva):**
```
One-pager layout, US Letter 2550 x 3300 px. Background #F5F8FD. Top left "Rewind" as live text, Cabin 700, #16225C, 84 px. Headline, two lines, Cabin 700, #16225C, 150 px: "Undo what one rule or AI agent changed." Subhead Cabin 500, #0E102B, 64 px: "See what changes back first." Wide white card with the lifted-lane schematic (outer lanes #16225C at 20%, middle lane solid #16225C blocks lifted out, dashed outlines left behind), no text. Below, four empty white rounded blocks in a 2 x 2 grid with a thin outline, no text. Footer rule and one small line, Cabin 400, #0E102B, 40 px: "Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier." Nothing else.
```
**Render:** `visuals/one-pager-layout.svg`, `visuals/one-pager-layout.png` | Tool: headless Chrome | Size check: 2550 x 3300, match yes | Visual check: Cabin renders, lifted blocks no longer touch the top lane after one fix, nothing clipped.
