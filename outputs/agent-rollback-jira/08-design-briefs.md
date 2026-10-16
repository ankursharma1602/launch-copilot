# Design briefs: Agent Rollback for Jira (Tier 2)

**Produced for this tier:** email header, in-app banner, LinkedIn image, one-pager layout.
**Deliberately skipped:** blog hero image (Tier 1 only).
**Source copy:** 07-channel-copy.md, section "On-image text". Text is copied unchanged, nothing cut or added.
**Style note:** Brand from `context/brand.md`. Wordmark set in type, not the official logo file. [NEED PROOF: confirm brand palette and typeface with Rewind's brand team] [NEED PROOF: confirm Boomerang yellow hex and navy with Rewind's brand team] No visual leaves the team until the brand team confirms.

**Palette used:** Boomerang Yellow #FFC72C (primary, UNCONFIRMED), Blue Zodiac #16225C (secondary, navy), Link Water #F5F8FD (canvas), Ebony #0E102B (body text), White #FFFFFF (cards). Tints of navy and yellow for schematic shapes only.
**Accent rule applied:** yellow is the accent in all four visuals: the lifted blocks, the highlight bar under the wordmark, the middle lane tint, and the supporting-line pill or bar. Navy carries the headline and the "Rewind" wordmark on the light canvas. No text is set in yellow. Text on yellow fills is navy.

**Shared visual idea (all four):** a white schematic card with three lanes. The middle lane is one agent or rule (a neutral actor among others). Its yellow blocks, outlined in navy, lift out of a pale yellow lane and leave dashed outlines in place. The other two lanes, in navy tints, stay untouched. No text, counts or ticket numbers inside the card. Nothing frames the agent as a villain.

**Internal-term check on all on-image text:** no internal terms found ("actor", "blast radius", "selective rollback" do not appear). The LinkedIn headline now says "agent's changes". "Agent Rollback for Jira" is the product name and is kept as written in 07. Note for the copy owner: 07's email preview line still says "Undo one actor's changes", and the email body and release note use "actor". These are not on-image, so I did not change them, but they are internal terms in customer copy.

**Font:** Cabin loaded through a Google Fonts `@import` in each SVG, with the brand fallback stack. Confirmed by viewing every PNG: the glyphs are Cabin, not the fallback. The SVG needs internet access to show Cabin when opened elsewhere. The PNGs are fixed.

**Tool for all four:** headless Google Chrome, 1x scale. All four PNGs viewed after the final render.

## Email header
**Size:** 1200 x 400 px
**Used with:** Customer email
**On-image text** (13 words, from 07 "Email header"):
> Rewind
> Undo the one change, not the whole site.
> Agent Rollback for Jira

**Layout:** wordmark top left (44 px) with a short yellow bar below; headline two lines at 58 px; yellow pill with the supporting line (28 px, navy text) below; schematic card right (420 x 300).
**Visual direction:** Link Water canvas, one idea, generous space. Legible at half size (headline reads about 29 px).
**Brand applied:** #F5F8FD canvas, #16225C wordmark and headline, #FFC72C accent (bar, pill, lifted blocks, lane tint at 28%), #16225C text on the yellow pill, #FFFFFF card, navy tints for other shapes. Cabin 700 headline and wordmark, Cabin 600 pill text. Wordmark set in type, not the official logo file.
**Avoid:** limitations, plan names, "only" claims, alarms, robots, any vendor logo, the Boomerang mark, yellow text.
**Does not claim:** Jira Cloud only, changes after the first backup, issues and fields only, the attachment limit, plan tier. These stay in the email.

**Prompt (paste into Claude Design or Canva):**
```
Email header, 1200 x 400 px. Light background #F5F8FD. Top left, the word "Rewind" as live text in Cabin 700, #16225C, 44 px, with clear space. Not a logo. Under it a short rounded bar in #FFC72C. Headline in two lines, Cabin 700, #16225C, 58 px: "Undo the one change, not the whole site." Below it a #FFC72C pill with text in Cabin 600, #16225C, 28 px: "Agent Rollback for Jira". Right side: a white rounded card with three horizontal lanes. Outer lanes hold pale blocks (#16225C at 20%). The middle lane is a pale #FFC72C tint; its three blocks are solid #FFC72C with a thin #16225C outline, lifted above the lane and joined by thin lines to dashed outlines left in place. No text in the card. No other text, no logos, no robots, no alarms, no yellow text.
```
**Render:** `visuals/email-header.svg`, `visuals/email-header.png` | Tool: headless Chrome | Size check: 1200 x 400, match yes | Visual check: Cabin renders, nothing clipped or overlapping, margins at least 60 px, navy on yellow and navy on Link Water pass contrast.

---

## In-app banner
**Size:** 1280 x 320 px
**Used with:** In-app message
**On-image text** (13 words, from 07 "In-app banner"):
> Rewind
> Undo what one rule or AI agent changed.
> See the effect first.

**Layout:** wordmark top left (40 px) with a short yellow bar; headline two lines at 50 px; yellow pill with the supporting line (26 px) below; schematic card right (420 x 260).
**Visual direction:** same schematic, compact and calm. The pill sits where a button would, but it is text from 07, not a button label.
**Brand applied:** #F5F8FD canvas, #16225C wordmark, headline and pill text, #FFC72C accent, #FFFFFF card, navy tints. Cabin 700 / 600. Wordmark set in type, not the official logo file.
**Avoid:** limitations, attachment note, plan tier, alarms, robots, vendor logos, the Boomerang mark, yellow text.
**Does not claim:** the Jira Cloud, first-backup, 24-hour attachment and plan-tier limits in the in-app body copy.

**Prompt (paste into Claude Design or Canva):**
```
In-app banner, 1280 x 320 px. Background #F5F8FD. Top left, "Rewind" as live text, Cabin 700, #16225C, 40 px. Short rounded bar under it in #FFC72C. Headline, two lines, Cabin 700, #16225C, 50 px: "Undo what one rule or AI agent changed." Below, a #FFC72C pill with Cabin 600, #16225C, 26 px text: "See the effect first." Right: white rounded card with three lanes; outer lanes pale blocks (#16225C at 20%); middle lane a pale #FFC72C tint whose solid #FFC72C blocks (thin #16225C outline) lift out, dashed outlines left behind. No text in the card. No other text or logos.
```
**Render:** `visuals/in-app-banner.svg`, `visuals/in-app-banner.png` | Tool: headless Chrome | Size check: 1280 x 320, match yes | Visual check: Cabin renders, nothing clipped, pill clear of headline descenders.

---

## LinkedIn image
**Size:** 1200 x 627 px
**Used with:** LinkedIn post (the post carries the limits)
**On-image text** (17 words, from 07 "LinkedIn image"):
> Rewind
> Undo one agent's changes, not the whole site.
> See what will change back before you restore.

**Layout:** 60 px safe margin. Wordmark top left (44 px) with a yellow bar; headline three lines at 62 px; supporting line two lines at 30 px with a yellow vertical bar to its left; schematic card right (420 x 400).
**Visual direction:** same schematic, larger card. Does not repeat the post text.
**Brand applied:** #F5F8FD canvas, #16225C wordmark and headline, #0E102B supporting line, #FFC72C accent, #FFFFFF card, navy tints. Cabin 700 / 500. Wordmark set in type, not the official logo file.
**Avoid:** limitations, disclaimers, plan names, alarms, robots, people at screens, vendor logos, the Boomerang mark, yellow text.
**Does not claim:** Jira Cloud, first-backup, issues and fields, attachment 24-hour and plan-tier limits stated in the post.

**Prompt (paste into Claude Design or Canva):**
```
LinkedIn image, 1200 x 627 px, 60 px safe margin. Background #F5F8FD. Top left "Rewind" as live text, Cabin 700, #16225C, 44 px, with a short #FFC72C bar below. Headline, three lines, Cabin 700, #16225C, 62 px: "Undo one agent's changes, not the whole site." Supporting line, Cabin 500, #0E102B, 30 px, with a #FFC72C vertical bar to its left: "See what will change back before you restore." Right: white rounded card, three lanes, outer lanes pale (#16225C at 20%), middle lane a pale #FFC72C tint with solid #FFC72C blocks (thin #16225C outline) lifted out and dashed outlines left behind. No text in the card, no other text, no logos.
```
**Render:** `visuals/linkedin-image.svg`, `visuals/linkedin-image.png` | Tool: headless Chrome | Size check: 1200 x 627, match yes | Visual check: Cabin renders, apostrophe renders, inside safe margin, nothing clipped.

---

## One-pager layout
**Size:** 2550 x 3300 px
**Used with:** One-pager in 09-sales-enablement.md
**On-image text** (28 words including the wordmark, from 07 "One-pager layout"):
> Rewind
> Undo what one rule or AI agent changed.
> See what changes back first.
> Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier.

**Layout:** wordmark top left (84 px) with a yellow bar; headline two lines at 150 px; yellow pill with the supporting line (64 px); wide schematic card (2250 x 620); four empty white body blocks in a 2 x 2 grid, each with one short yellow bar and no text, to be filled from 09; yellow footer rule and one small limits line (40 px).
**Visual direction:** structure over decoration. The empty blocks stay empty.
**Brand applied:** #F5F8FD canvas, #16225C wordmark and headline and pill text, #0E102B limits line, #FFC72C accent, #FFFFFF cards, navy tints. Cabin 700 / 600 / 400. Wordmark set in type, not the official logo file.
**Avoid:** extra text, lorem ipsum, beta numbers, quotes, customer names, alarms, robots, vendor logos, the Boomerang mark, yellow text.
**Does not claim:** the attachment limit does not fit the one small line. It must be carried in the body blocks from 09. The image must not imply attachments are covered without it. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]

**Prompt (paste into Claude Design or Canva):**
```
One-pager layout, US Letter 2550 x 3300 px. Background #F5F8FD. Top left "Rewind" as live text, Cabin 700, #16225C, 84 px, with a short #FFC72C bar below. Headline, two lines, Cabin 700, #16225C, 150 px: "Undo what one rule or AI agent changed." Subhead on a #FFC72C pill, Cabin 600, #16225C, 64 px: "See what changes back first." Wide white card with the lifted-lane schematic (outer lanes #16225C at 20%, middle lane a pale #FFC72C tint with solid #FFC72C blocks, thin #16225C outline, lifted out, dashed outlines left behind), no text. Below, four empty white rounded blocks in a 2 x 2 grid with a thin outline and a short #FFC72C bar at top left, no text. Footer: a #FFC72C rule and one small line, Cabin 400, #0E102B, 40 px: "Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier." Nothing else.
```
**Render:** `visuals/one-pager-layout.svg`, `visuals/one-pager-layout.png` | Tool: headless Chrome | Size check: 2550 x 3300, match yes | Visual check: Cabin renders, lifted blocks clear of the top lane, nothing clipped, body blocks empty.
