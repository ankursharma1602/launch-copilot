# Design briefs: Agent Rollback for Jira (Tier 2)

**Produced for this tier:** email header, in-app banner, LinkedIn image, one-pager layout.
**Deliberately skipped:** blog hero image (Tier 1 only).
**Source copy:** 07-channel-copy.md
**Style note:** Placeholder brand colors in use. [NEED PROOF: brand palette, fonts and logo files]

**Shared visual idea (all four):** a schematic timeline. Three grey lanes of neutral blocks stay in place. In the top lane, three accent blocks lift out and leave dashed empty slots behind, joined by dotted lines. One actor's changes come out, everyone else's work stays. No text, counts or ticket numbers inside the shapes. The actor is not named or drawn as a character. No logo is drawn.

**Palette (placeholder, all assets):** text #1F2933, background #F3F5F7, footer strip #E4E9EE, neutral blocks #C3CCD6, rails #D5DCE3, accent #2F6FED. Font stack: Helvetica Neue, Helvetica, Arial, sans-serif.

**Cuts from the copy (cutting allowed, no rewriting):**
- Email header: sub-line dropped so the full limits footer stays word for word at 24 words.
- LinkedIn image: sub-line cut to "Keep your team's work." to stay under 30 words and keep all limits.
- One-pager: the three body blocks stay empty, to be filled from `09-sales-enablement.md`. The footer is word for word from 07. The "What to know" box carries short forms of limits 2, 3 and 4 from 09. Limits 1 and 3 are in the footer in full, so all four limits are on the visual. The sub-head from the earlier render is removed because it is not in 07. Word count is 42, over the 30-word cap. This is accepted on purpose so the PNG cannot be forwarded without the limits. The box short forms are not word for word from 07, which only says "filled from 09". The Confluence roadmap line still needs sign-off. [NEED PROOF: sign-off to mention Confluence roadmap publicly]

---

## Email header
**Size:** 1200 x 400 px
**Used with:** Customer email (shows at 600 px wide in the inbox)
**On-image text** (24 words, from "Customer email" > Email header on-image text):
> Undo one agent's changes, not the whole site.
> Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back.

**Layout:** Left: headline, two lines, 46 px bold. Right: timeline motif. Bottom: grey strip with the limits in two lines at 22 px, full width inside 60 px margins. Thin accent bar on the left edge.
**Visual direction:** Calm and spacious. The headline is clearly the largest element. Limits are readable at half size.
**Palette (placeholder):** see shared palette. Placeholders, replace with brand palette.
**Avoid:** red alarms, warning icons, robots, glitch effects, any vendor logo, extra text.
**Does not claim:** support beyond Jira Cloud, rollback of anything before the first Rewind backup.

**Prompt (paste into Claude Design or Canva):**
```
Email header, 1200 x 400 px, light grey background. Headline, bold, largest: "Undo one agent's changes, not the whole site." Bottom strip, small but legible: "Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back." Right side: abstract timeline with three lanes of grey rounded blocks. In the top lane three accent blocks lift out above it, leaving dashed empty slots, joined by dotted lines. No text in the shapes. Placeholder palette: dark slate text, light grey background, one blue accent. Avoid red, warning icons, robots, logos, stock photos.
```

**Render:** `visuals/email-header.svg`, `visuals/email-header.png` | Tool: headless Chrome | Size check: 1200 x 400, match yes | Visual check: viewed, no clipping or overlap, text inside margin.

---

## In-app banner
**Size:** 1280 x 320 px
**Used with:** In-app message
**On-image text** (22 words, from "In-app message" > In-app banner on-image text):
> Undo one agent, not the whole site.
> Jira Cloud only. Changes after your first backup. Not on every plan.
> See Actor view

**Layout:** Left: headline 42 px bold, limits line 22 px, then a pill button with the label. Right: small timeline motif.
**Visual direction:** Quiet, one idea, sits above the message without crowding it.
**Palette (placeholder):** see shared palette. Placeholders, replace with brand palette.
**Avoid:** alarm colors, warning icons, robots, vendor logos, extra text.
**Does not claim:** Confluence support (left out on purpose, no sign-off), any plan name, rollback before the first backup.

**Prompt (paste into Claude Design or Canva):**
```
In-app banner, 1280 x 320 px, light grey background. Headline bold: "Undo one agent, not the whole site." Below it, regular weight: "Jira Cloud only. Changes after your first backup. Not on every plan." Blue pill button with white text: "See Actor view". Right side: small abstract timeline of grey blocks, with three accent blocks lifted out of the top lane and dashed empty slots left behind. Placeholder palette. Avoid red, warning icons, robots, logos.
```

**Render:** `visuals/in-app-banner.svg`, `visuals/in-app-banner.png` | Tool: headless Chrome | Size check: 1280 x 320, match yes | Visual check: viewed, no clipping or overlap.

---

## LinkedIn image
**Size:** 1200 x 627 px, 60 px safe margin
**Used with:** LinkedIn post
**On-image text** (28 words, from "LinkedIn post" > LinkedIn image on-image text):
> Undo one agent's changes, not the whole site.
> Keep your team's work.
> Jira Cloud only at launch. Only changes after your first Rewind backup. Not on every plan.

**Layout:** Top left: short accent rule, headline 56 px bold, sub-line 30 px. Right: timeline motif, kept clear of the footer. Bottom: grey strip with the limits in two lines at 23 px.
**Visual direction:** Works beside the post without repeating its body. Mechanism only, no people, no fear imagery.
**Palette (placeholder):** see shared palette. Placeholders, replace with brand palette.
**Avoid:** alarm colors, warning icons, robots, stock photos, vendor logos, extra text.
**Does not claim:** support beyond Jira Cloud, any plan name, rollback before the first Rewind backup.

**Prompt (paste into Claude Design or Canva):**
```
LinkedIn image, 1200 x 627 px, 60 px margins, light grey background. Headline bold: "Undo one agent's changes, not the whole site." Sub-line: "Keep your team's work." Footer strip: "Jira Cloud only at launch. Only changes after your first Rewind backup. Not on every plan." Right: abstract timeline, three lanes of grey blocks, three accent blocks lifted from the top lane with dashed empty slots left behind. No text in shapes. Placeholder palette. Avoid red, warning icons, robots, people at screens, logos.
```

**Render:** `visuals/linkedin-image.svg`, `visuals/linkedin-image.png` | Tool: headless Chrome | Size check: 1200 x 627, match yes | Visual check: viewed. First render had the motif running under the footer strip. Moved up and re-rendered. Now clear, no clipping.

---

## One-pager layout
**Size:** 2550 x 3300 px (US Letter, 300 dpi)
**Used with:** Sales one-pager (`09-sales-enablement.md`)
**On-image text** (42 words as rendered: headline 8, box title 3, box lines 15, footer 16. From "One-pager layout, on-image text"):
> Undo one agent's changes, not the whole site.
> What to know
> Attachments: backup up to 24 hours old.
> Confluence: roadmap, no date.
> Not on every plan.
> Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back.

**Layout:** Headline 150 px bold at the top. Large timeline motif. Three empty white cards in a row for the three body blocks. Full-width "What to know" box, titled, with three lines at 52 px. Footer in two lines at 44 px at the bottom, full text. Empty logo area top right, intentionally blank. [NEED PROOF: brand palette, fonts and logo files]
**Visual direction:** The same motif at large scale. Generous space so the filled body text has room.
**Palette (placeholder):** see shared palette. Placeholders, replace with brand palette.
**Avoid:** lorem ipsum, fake data, alarm colors, robots, vendor logos.
**Does not claim:** support beyond Jira Cloud, a Confluence date, a plan name, rollback before the first Rewind backup.

**Prompt (paste into Claude Design or Canva):**
```
Sales one-pager layout, US Letter 2550 x 3300 px, light grey background. Headline bold: "Undo one agent's changes, not the whole site." Large abstract timeline: three lanes of grey rounded blocks, three accent blocks lifted from the top lane with dashed empty slots left behind. Below, three empty white cards in a row, then a grey box titled "What to know" with three lines: "Attachments: backup up to 24 hours old." "Confluence: roadmap, no date." "Not on every plan." Footer text: "Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back." Leave the three cards empty, no placeholder text. Leave an empty logo area top right. Placeholder palette. Avoid red, warning icons, robots, logos.
```

**Render:** `visuals/one-pager-layout.svg`, `visuals/one-pager-layout.png` | Tool: headless Chrome | Size check: 2550 x 3300, match yes | Visual check: viewed after re-render, no clipping, cards empty, limits box and footer fully inside margins.
