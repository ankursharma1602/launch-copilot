# Design briefs: Clio Timekeeping GA (Tier 2)

Produced: email header, in-app banner, LinkedIn image, one-pager layout.

Font for all four: Inter (stand-in for Facility); labels in system monospace. The three launch visuals carry the official logo file (assets/clio-logo.png), unaltered.

## Email header
**Size:** 1200 x 560 px
**On-image text** (from 08-channel-copy.md, "On-image text"):
> NOW AVAILABLE
> Your time, drafted / while you work
> Clio Timekeeping turns your emails, documents and calls into time entries you check and bill.
> Chips: Email to client · 9:12 a.m. / Lease draft in Word · 10:05 a.m. / Call with opposing counsel · 11:30 a.m.
> Card: My time entries; Commercial lease review · 24 min; Commercial lease review · 52 min; Supplier contract dispute · 18 min; Bill-ready; Review

**Logo:** `assets/clio-logo.png` embedded byte for byte as a base64 data URI in an SVG `<image>`, top left, native 655:240 ratio, 40 px clear space from left and top, unaltered, drawn first. No live "Clio" text beside it.
**Layout:** Logo top left, white pill top centre, two-line thin headline, grey subline (2 lines), then the flow centred below at 16 px text. Height raised from 400 so the flow stays legible.
**Flow:** three outlined chips (1px white at 25%, no fill) on the left, one thin 2px arrow (white at 60%), one flat #191919 card on the right. The first two toggles are on (#1A56FF), the third is off (#404040) with a "Review" label. Reads as: emails, documents and calls in, drafted entries out, you check and bill.
**Brand applied:** #000000 canvas, #FFFFFF, #0A0A0A pill text, #191919 card, #404040 off toggle, #1A56FF. Inter 200 headline (stand-in for Facility), Inter 400/500 elsewhere, mono capital label. No shadow, gradient, icon or screenshot. No limits text on the image.
**Does not claim:** anything about plans, regions or capture beyond the copy. Details stay in the post, email and in-app copy.
**Files:** `visuals/email-header.svg`, `visuals/email-header.png` (rendered with headless Chrome, 1200 x 560 checked with sips)

## In-app banner
**Size:** 1280 x 420 px
**On-image text** (from 08-channel-copy.md, "On-image text" and Button):
> NOW AVAILABLE
> Your time, drafted / while you work
> Clio Timekeeping turns your emails, documents and calls into time entries you check and bill.
> Chips: Email to client · 9:12 a.m. / Lease draft in Word · 10:05 a.m. / Call with opposing counsel · 11:30 a.m.
> Card: My time entries; Commercial lease review · 24 min; Commercial lease review · 52 min; Supplier contract dispute · 18 min; Bill-ready; Review
> Button: Try Clio Timekeeping

**Logo:** `assets/clio-logo.png` embedded byte for byte as a base64 data URI in an SVG `<image>`, top left, native 655:240 ratio, 40 px clear space from left and top, unaltered, drawn first. No live "Clio" text beside it.
**Layout:** Left column: 36 px logo, pill, headline (40 px), grey subline (3 lines), one #1A56FF button (white Inter 600, 6 px radius). Right: the compact flow at 15 px text. Height raised from 320 so nothing is below 15 px.
**Flow:** three outlined chips (1px white at 25%, no fill) on the left, one thin 2px arrow (white at 60%), one flat #191919 card on the right. The first two toggles are on (#1A56FF), the third is off (#404040) with a "Review" label. Reads as: emails, documents and calls in, drafted entries out, you check and bill.
**Brand applied:** #000000 canvas, #FFFFFF, #0A0A0A pill text, #191919 card, #404040 off toggle, #1A56FF. Inter 200 headline (stand-in for Facility), Inter 400/500 elsewhere, mono capital label. No shadow, gradient, icon or screenshot. No limits text on the image.
**Does not claim:** anything about plans, regions or capture beyond the copy. Details stay in the post, email and in-app copy.
**Files:** `visuals/in-app-banner.svg`, `visuals/in-app-banner.png` (rendered with headless Chrome, 1280 x 420 checked with sips)

## LinkedIn image
**Size:** 1200 x 627 px
**On-image text** (from 08-channel-copy.md, "On-image text"):
> CLIO TIMEKEEPING
> Your time, drafted / while you work
> Clio Timekeeping turns your emails, documents and calls into time entries you check and bill.
> Chips: Email to client · 9:12 a.m. / Lease draft in Word · 10:05 a.m. / Call with opposing counsel · 11:30 a.m.
> Card: My time entries; Commercial lease review · 24 min; Commercial lease review · 52 min; Supplier contract dispute · 18 min; Bill-ready; Review

**Logo:** `assets/clio-logo.png` embedded byte for byte as a base64 data URI in an SVG `<image>`, top left, native 655:240 ratio, 40 px clear space from left and top, unaltered, drawn first. No live "Clio" text beside it.
**Layout:** Logo top left, pill top centre, two-line thin headline (56 px, largest text), grey subline (2 lines), full flow at 17 px text below.
**Flow:** three outlined chips (1px white at 25%, no fill) on the left, one thin 2px arrow (white at 60%), one flat #191919 card on the right. The first two toggles are on (#1A56FF), the third is off (#404040) with a "Review" label. Reads as: emails, documents and calls in, drafted entries out, you check and bill.
**Brand applied:** #000000 canvas, #FFFFFF, #0A0A0A pill text, #191919 card, #404040 off toggle, #1A56FF. Inter 200 headline (stand-in for Facility), Inter 400/500 elsewhere, mono capital label. No shadow, gradient, icon or screenshot. No limits text on the image.
**Does not claim:** anything about plans, regions or capture beyond the copy. Details stay in the post, email and in-app copy.
**Files:** `visuals/linkedin-image.svg`, `visuals/linkedin-image.png` (rendered with headless Chrome, 1200 x 627 checked with sips)

## One-pager layout
**Size:** 2550 x 3300 px
**On-image text:**
> Clio (wordmark) | CLIO TIMEKEEPING
> Stop rebuilding your week
> Now available on every Clio Manage plan.
> 1. Time is drafted while you work, so Friday is for checking.
> 2. You review every entry and decide what is billed.
> 3. Entries land on your matters, ready for your next bill.
> Activities > "My time entries" / Edit with the pencil icon / Switch on "Bill-ready" to add it to the matter's unpaid bills

**Layout:** Black header band with "Clio" in white type at left and the label at right. Very large thin headline, grey supporting line, and an abstract entry card top right. Three pillar cards in a row, then one wide card with three numbered steps.
**Colours:** #FFFFFF canvas, #000000 band, #0A0A0A, #404040, #F5F5F5, pillar cards #D9E2FB, #CCC4BA, #DBCCFF, numerals and toggle #1A56FF.
**Files:** `visuals/one-pager-layout.svg`, `visuals/one-pager-layout.png`
