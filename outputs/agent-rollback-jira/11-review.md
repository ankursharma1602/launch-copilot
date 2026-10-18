# Review: Agent Rollback for Jira (Tier 2)

Reviewed: 01 to 10 and the four SVG and PNG pairs in `visuals/`. Every PNG was opened and viewed. Checked against `.claude/skills/brand-review/SKILL.md`, `context/` (including `brand.md`) and `learnings/lessons.md`.

## Mechanical checks
- Em dashes and en dashes: 0 (Grep for the characters and for HTML entities across the folder).
- Banned words: 0 in assets. The only hit is `05-messaging.md` line 54, which lists the banned words as an avoid list. Not a breach.
- Exclamation marks: 0 across the folder.
- "Under 24 hours" near Agent Rollback: appears only in "do not say" lists (09, 09c). Not used in any customer copy, SVG or on-image text.
- "No actor-based rollback" or "native lacks": appears only in "never say" guidance (09, 09b, 09c). No asset claims it.
- Third-party, "only", "first" or "no other tool" claims: none in customer copy.
- Closed beta numbers or quotes in customer-facing assets (07, visuals, one-pager): none.
- Confluence mention: absent from every customer asset. It appears only in the rep-only lines in 09 and the quiz, with the Legal tag.
- Tier scope: no blog outline, blog hero image or Sales FYI exists. The folder holds exactly the Tier 2 matrix.
- Length limits, counted by hand:
  - Email Subject A, "Undo the one change, not the whole site": **39 characters**. 07 says 38. Under 50, so no breach, but the stated count is wrong.
  - Email Subject B, "Undo what one rule or AI agent changed in Jira": 46. Correct, under 50.
  - Email preview: 61. Correct, under 90.
  - Email body: about 139 words plus a 4-word CTA, so about 143. Under 150.
  - In-app headline: 7 words (limit under 8). Body: 24 words (limit under 25). Button: 2 words. All pass.
  - LinkedIn post: about 101 words. 07 says 112. Under 120, no hashtags or emojis. Count is mis-stated, not a breach.
  - Talk track: 130 words (09 says about 128). Under 150.
  - On-image text: email header 13, in-app banner 13, LinkedIn image 17, one-pager 28. All under 30. 08 says the one-pager is "about 29", 07 says 28. Counting gives 28.
- Timing offsets in 06, 09b, 09c and 10:
  - 06 gives build L-28 to L-18, final review L-17 to L-14, kit L-10, session L-7, quiz L-5, go/no-go L-3, launch L, LinkedIn L+1, adoption L+30 and expansion L+90.
  - 09 (kit L-10), 09b (L-7, quiz L-5), 09c (L-5), 10 CSV and 10 MD all match. Reviewer pass is L-17 and re-review is L-14, matching the final review window. Draft checklist is L-18, the end of the build window.
  - No drift.
- 06 math: (3 x 0.25) + (4 x 0.25) + (5 x 0.20) + (3 x 0.15) + (5 x 0.15) = 0.75 + 1.00 + 1.00 + 0.45 + 0.75 = 3.95. Correct. The tier is exactly one band, Tier 2. The sensitivity figures check out (reach 4 gives 4.20, story 4 gives 3.80, story 3 gives 3.65). Weights sum to 100%.
- CSV: 7 columns on all 41 data rows. Every field is quoted, and embedded quotes use single quotes. Every "Depends On" entry matches a Task name exactly (checked rows 19, 31 and 37 in full).
- Visuals, checked in the SVG source and the PNGs:
  - Hex codes used are only #F5F8FD, #16225C, #0E102B and #FFFFFF, plus Blue Zodiac opacity tints. No yellow. (First-pass note on the old palette. Superseded: the visuals were re-rendered in Rewind yellow #FFC72C and navy #16225C, see the visuals revision review below.)
  - The "Rewind" wordmark is a live `<text>` element in Cabin 700. There is no logo file, no `<image>` and no Boomerang.
  - PNG glyphs are Cabin. The distinctive single-storey "a" and the "g" are visible in all four.
  - Wordmark sizes are 44, 40, 44 and 84 px, all at or above the 32 px floor.
  - Pixel sizes match the spec: 1200x400, 1280x320, 1200x627 and 2550x3300.
  - Nothing is clipped or overlapping.
  - The email header, in-app banner and LinkedIn image carry no limits, disclaimers, plan caveats, numbers or quotes.
  - Only the one-pager carries one limits line: "Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier."
  - On-image text matches 07 word for word in all four SVGs.
  - No fear imagery, and the actor is shown neutrally.
  - 08 flags the unconfirmed palette and typeface, and says the wordmark is set in type.

## Scores
| Asset | Positioning and messaging | Proof | Persona | Voice | Spec | Avg | Result |
|---|---|---|---|---|---|---|---|
| 01 Launch brief (launch-brief-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 02 Launch context (product-context-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 03 Audience (audience-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 04 Positioning (positioning-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 05 Messaging (messaging-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 06 Campaign strategy (campaign-strategy-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 07 Channel copy (copywriter-agent) | 5 | 5 | 5 | 5 | 4 | 4.8 | Pass (two non-blocking corrections) |
| 08 Design briefs (design-director-agent) | 5 | 5 | 5 | 5 | 4 | 4.8 | Pass (one non-blocking correction) |
| Visual: email-header | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: in-app-banner | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: linkedin-image | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: one-pager-layout | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 09 Sales enablement (sales-enablement-agent) | 4 | 3 | 5 | 5 | 5 | 4.4 | **Fail** (proof fail condition) |
| 09b Enablement session (sales-enablement-agent) | 4 | 3 | 5 | 5 | 5 | 4.4 | **Fail** (same drift as 09) |
| 09c Readiness quiz (sales-enablement-agent) | 5 | 3 | 5 | 5 | 5 | 4.6 | **Fail** (invented pass mark) |
| 10 Checklist CSV and MD (launch-ops-agent) | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |

## Fixes required

### 09-sales-enablement.md (sales-enablement-agent) FAIL
- Quote: "Deleted attachments come from the most recent backup, which may be up to 24 hours old." (Talk track, last limits sentences)
- Problem: Must say 2 in 05 is "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old." The talk track drops "by an agent" and "restored". That broadens the limit to every deleted attachment and changes what the limit says. It rewrites a must-say limit that has an open wording item. The rep says this line out loud.
- Fix: Replace with "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old." The track becomes about 133 words, still under 150. Update the word count line. The one-pager, FAQ and objection table already use the right wording.

### 09b-enablement-session.md (sales-enablement-agent) FAIL
- Quote: "Deleted attachments come from the most recent backup, which may be up to 24 hours old." (Talking point 7)
- Problem: The same drift from 05 Must say 2 as in 09.
- Fix: Use "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old."

### 09c-readiness-quiz.md (sales-enablement-agent) FAIL
- Quote: "Pass mark: 7 of 8."
- Problem: 06 success metrics and task "Set quiz pass mark and target" in 10 both say the pass mark is not set: [NEED PROOF: pass mark and target share of reps]. 09c states 7 of 8 as fact with no tag. It also contradicts the chain, because 10 has a task to set it at L-12.
- Fix: Change to "Pass mark: 7 of 8 (proposed). [NEED PROOF: pass mark and target share of reps]". In 09b, change "Pass mark is 7 of 8." to "Proposed pass mark is 7 of 8." The tag is already there.

### 07-channel-copy.md (copywriter-agent) PASS, correct two stated counts
- Quote: "Subject A: Undo the one change, not the whole site (38 characters)"
- Problem: The count is 39, not 38. Still under 50.
- Fix: Change to "(39 characters)".
- Quote: "(Count: 112 words, under 120. No hashtags, no emojis.)"
- Problem: The post is about 101 words. The stated figure is wrong, though the limit is met.
- Fix: Change to "(Count: about 101 words, under 120. ...)".
- Advisory, no change required before the human check: the in-app body says "Agent-deleted attachments come from the latest backup, which may be up to 24 hours old" and "after your first backup". These shorten the handoff wording ("restored from the most recent backup", "first Rewind backup"). 07 admits this. At 24 of 24 allowed words there is no room to restore it. The attachment-wording decision (go/no-go gate 4) must confirm this short form, or the copywriter must trim the body to fit the approved wording.

### 08-design-briefs.md (design-director-agent) PASS, correct one count
- Quote: "On-image text (about 29 words including the wordmark, from 07 "One-pager layout")"
- Problem: 07 gives 28 and the text counts to 28, and the brief is meant to render 07 unchanged.
- Fix: Change to "(28 words including the wordmark)".

Everything else needs no change. Before it leaves the team, the stated rules for visuals still apply (see Open proof requests).

## Open proof requests (collected, not fails)
Upstream and context:
- 01: GA date, plan names and pricing, owner dates, pricing date, legal date, adoption and expansion baselines and targets, pipeline baseline and target, approval to use closed beta results or quotes, source for native tool capability, competitor capability check, large-site behavior, brand hex codes and typeface.
- 02: all gaps in its Gaps table, including audit log contents and export format, how a customer turns the feature on, and any outcome measure.
- 03: customer research, share of bad changes from rules versus agents, how often AI governance is a buying reason, number of Rewind Jira Cloud customers per segment, CRM capture.
- 04, 05: attachment wording including the 24-hour phrase, Legal approval of "exportable for auditors" and any Confluence mention, who can run a rollback, same-field behavior, how Actor view identifies actors, rollback-able data types, outcome measures.
- 06: baselines, targets, pass mark and target share of reps, email and in-app benchmarks, definition of "active Jira customers", budget and paid media targets, eligible base size.

Assets:
- 07: release note step 1, "[NEED PROOF: how a customer turns the feature on, and whether it needs setup]". The release note availability line also carries the attachment-wording tag. The notes section carries the brand tag.
- 08: palette and typeface confirmation, attachment-wording tag.
- 09: attachment wording, Legal for Confluence and "exportable for auditors", plan names and pricing, data types, large sites, same-field edits, who can run a rollback, Actor view detection, audit log contents, how to turn it on, competitor check, outcome measure, beta approval, GA date.
- 09b: beta approval, pass mark.
- 10: every open item above is mapped to a task in the checklist.

## Second pass
Scope: 09, 09b and 09c only, after one revision pass. Checked with Grep and a manual word count.

### Fix checks
| Check | Result |
|---|---|
| Attachment wording matches 05 Must say 2 exactly ("Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.") | Pass. Found verbatim in 09 (Limits item 2, talk track, objection table, FAQ), 09b (talking point 7) and 09c (answer 7). The old "Deleted attachments come from..." wording is gone. |
| Pass mark marked proposed with [NEED PROOF] | Pass. 09c header: "Pass mark: 7 of 8 (proposed). [NEED PROOF: quiz pass mark and target share of reps]". 09b Wrap-up: "Proposed pass mark is 7 of 8." with the tag. |
| Talk track under 150 words | Pass. Counted by hand: 17 + 17 + 6 + 10 + 13 + 5 + 11 + 12 + 7 + 8 + 20 + 8 = 134. The stated "About 134 words" is correct. |
| Em dashes and en dashes in 09, 09b, 09c | Pass. Grep found 0. |
| Exclamation marks, beta percentages or quotes in 09, 09b, 09c | Pass. 0 found. Quiz states it uses no beta numbers or quotes. |
| Nothing new broke | Pass. "Under 24 hours" appears only in Do-not-say contexts. Confluence line, plan tier line and data type caveat unchanged and still tagged. No new unsupported claims. |

### Result per asset
| Asset | Result |
|---|---|
| 09 Sales enablement | **Pass** |
| 09b Enablement session | **Pass** |
| 09c Readiness quiz | **Pass** |

### Advisory items for the run report (non-blocking, from pass one, plus one new)
1. 07 Subject A: "(38 characters)" should read "(39 characters)". Still under 50.
2. 07 LinkedIn post: "(Count: 112 words, under 120...)" should read "about 101 words". Limit is met.
3. 08 one-pager: "about 29 words including the wordmark" should read "28 words". 07 gives 28.
4. 07 in-app body shortens the Must say 2 attachment wording ("Agent-deleted attachments come from the latest backup...") and "after your first backup". It has no word room to restore it. Go/no-go gate 4 (attachment wording) must confirm the short form, or the copywriter trims the body to fit the approved wording.
5. New, minor: 09 FAQ "Does it go back before we started with Rewind?" says "Two closed beta accounts did not get this at first (mock, internal)". It is labelled internal and the page bans repeating beta figures, so it is not a fail. Safer to delete "Two closed beta accounts did not get this at first" and keep "so say it early".

No asset in this pass needs a human beyond the open [NEED PROOF] items already collected above.

## Visuals revision review
Scope: 08-design-briefs.md and the four visuals (email header, in-app banner, LinkedIn image, one-pager layout), after the brand update (yellow #FFC72C unconfirmed, navy #16225C). Checked with Grep on the SVGs and brief, and by opening all four PNGs. Word counts done by hand.

### Mechanical checks
- Em dashes, en dashes, exclamation marks in 08 and the four SVGs: 0 found.
- Internal terms ("actor", "blast radius", "selective rollback", "Actor view") in any SVG: 0 found. They appear in 08 only in the internal-term check note, not on any image.
- Colours in all four SVGs: only #F5F8FD, #16225C, #FFC72C, #FFFFFF, #0E102B, plus opacity tints of navy and yellow. No other hex.
- Text in yellow: none. Every `<text>` fill is #16225C or #0E102B. Yellow is used only for bars, pills, lane tint and lifted blocks.
- Embedded images, paths or logo files in the SVGs: none. "Rewind" is a `<text>` element in Cabin 700, navy, top left. No Boomerang mark.
- Font: each SVG imports Cabin from Google Fonts. In the PNGs the glyphs are Cabin (the single-storey "a" shapes, the "g" and "y" forms), not Helvetica or Arial.
- Pixel sizes: I could not run sips in this session (no shell tool). The images opened at 1200 x 400, 1280 x 320 and 1200 x 627 with coordinates matching the SVG viewBoxes, and the one-pager opened as 2550 x 3300. The brief states a match for all four. Treat as passed on the evidence, and re-run `sips -g pixelWidth -g pixelHeight` on the four PNGs if you want it on record.

### On-image text and word counts (matched word for word to 07 "On-image text")
| Visual | Text in SVG | Words | Matches 07 |
|---|---|---|---|
| Email header | Rewind / Undo the one change, not the whole site. / Agent Rollback for Jira | 1 + 8 + 4 = 13 | Yes |
| In-app banner | Rewind / Undo what one rule or AI agent changed. / See the effect first. | 1 + 8 + 4 = 13 | Yes |
| LinkedIn image | Rewind / Undo one agent's changes, not the whole site. / See what will change back before you restore. | 1 + 8 + 8 = 17 | Yes (curly apostrophe only) |
| One-pager | Rewind / Undo what one rule or AI agent changed. / See what changes back first. / Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier. | 1 + 8 + 5 + 14 = 28 | Yes |

All under 30. The LinkedIn headline is exactly "Undo one agent's changes, not the whole site."

### Result per visual
| Visual | Colour and accent | Cabin and wordmark | Customer words | Limits rule | Size, clipping | Result |
|---|---|---|---|---|---|---|
| Email header | Pass | Pass | Pass | Pass (no limits or plan text) | Pass | **Pass** |
| In-app banner | Pass | Pass | Pass | Pass | Pass | **Pass** |
| LinkedIn image | Pass | Pass | Pass | Pass | Pass | **Pass** |
| One-pager layout | Pass | Pass | Pass | Pass (one small limits line only, body blocks empty) | Pass | **Pass** |

Contrast: navy on Link Water and navy on yellow are readable in all four. The small limits line (Ebony, 40 px at 2550 wide) is legible. Nothing is clipped or overlapping. Lifted blocks clear the top lane in every card.

### 08-design-briefs.md
Pass. It carries [NEED PROOF: confirm brand palette and typeface with Rewind's brand team], [NEED PROOF: confirm Boomerang yellow hex and navy with Rewind's brand team], and the attachment-wording tag. It says "Wordmark set in type, not the official logo file" in the style note and in each asset. It has no beta numbers or quotes and says the limits stay in the copy.

### Advisory items (non-blocking)
1. In-app banner: the pill starts about 8 px below the descender of "agent" on the second headline line. It is clear but tight. If the banner is touched again, add 6 to 10 px between headline and pill.
2. 07 still uses internal terms in customer copy, as 08 notes: the email preview ("Undo one actor's changes in Jira Cloud...") and "actor" in the email body, release note and LinkedIn post. They are not on any image. The copywriter should swap "actor" for "agent, rule or integration" where it reads as customer copy.
3. The 08 one-pager "Does not claim" line is correct: the attachment limit is not on the one-pager's small line and must be carried by the body blocks filled from 09.
4. Palette, typeface and yellow hex stay unconfirmed. No visual leaves the team until the brand team confirms.

No visual needs a revision. No fixes required.

## Copy revision review
Scope: 07-channel-copy.md after the copywriter swapped internal terms for customer words. No shell tool was available, so I could not run `git diff`. I read the whole file and checked it against 02-launch-context.md, voice.md and the four SVGs. Because I could not see the diff, I confirmed intact items by presence and wording, not by comparing to the old text. All counts by hand.

**Result: FAIL, two small fixes (1 and 2 below). Everything else passes.**

### Mechanical checks (Grep on 07)
- Em dashes, en dashes, exclamation marks: 0.
- Banned words from voice.md: 0.
- Internal terms (actor, Actor view, blast radius, selective rollback, keep human work): 0 anywhere in the file, including the notes. Advisory item 2 above is closed.
- "under 24", "every change", "everything", beta numbers (11, 14, 23, 4,000), quotes: 0.

### Lengths
| Item | Count | Limit | Result |
|---|---|---|---|
| Subject A "Undo the one change, not the whole site" | 39 characters (file says 38) | under 50 | Pass, fix the stated count |
| Subject B "Undo what one rule or AI agent changed in Jira" | 46 | under 50 | Pass |
| Preview | 69 | under 90 | Pass |
| Email body (two paragraphs 30 + 60, Good to know 53, CTA 5) | 143 without CTA, 148 with CTA | under 150 | Pass, tight |
| In-app headline | 7 words | under 8 | Pass |
| In-app body | 24 words | under 25 | Pass |
| LinkedIn post (23 + 39 + 38 + 5) | 105 (file says about 115) | under 120 | Pass, fix the stated count |

The email has only 2 words of room. Any edit to the body must come with a recount.

### Intact items
- Limitations in the email, in-app, release note and LinkedIn: Jira Cloud, after the first Rewind backup, issues and fields, specific plan tier. Present in each.
- Attachment wording is "restored from the most recent backup, which may be up to 24 hours old" in the email, release note and LinkedIn. The in-app body shortens it to "come from the latest backup, which may be up to 24 hours old" and the notes say so. Never "under 24 hours". Pass.
- [NEED PROOF] tags present: how to turn the feature on (release note step 1 and notes), plain wording for the attachment limitation (release note and notes), brand hex and typeface (notes). Pass.
- On-image text matches the SVGs word for word: email header, in-app banner, LinkedIn image (curly apostrophe only) and one-pager, including the one-pager limits line. Word counts 13, 13, 17, 28 are correct. Pass.
- Confluence not mentioned. "Exportable for auditors" not used (copy says "can be exported"). Pass.

### Meaning and overclaim
- "Undo just its changes", "No whole-site restore" and "Separate edits people made after the bad event stay in place" match the handoff capabilities (undo all changes by one source in a window, or pick issues or fields; demo showed separate edits kept). Pass. The same-field case is not claimed anywhere. Pass.
- "Keep your team's work" (release note bullet heading) is broader than the demo, but the sentence under it limits it to "Separate edits people made after the bad event". Pass. Advisory: "Keep the work people did separately" is safer, since the heading alone could be read as covering same-field edits.
- No permission model, no detection explanation, no outcome measure. Pass.

### Fixes required
1. **Release note, How to get started, step 3: "Open Agent Rollback. Pick the rule, integration or AI agent and a time window."** This is a guess presented as a UI path. The handoff gives no place, menu or screen for the feature, and step 1 already says how to turn it on is unknown. The old wording used a handoff screen name. "Open Agent Rollback" implies a named screen that nobody has confirmed. Change to: `3. [NEED PROOF: in-product path to start a rollback] Pick the rule, integration or AI agent and a time window.` Add the same tag to the notes section next to the step 1 tag. Do not name a screen, tab or button.
2. **Release note, What's new, first bullet: "Changes in Jira are grouped by a person, an automation rule, an integration or an AI agent."** "Changes in Jira" with the bullet title "each change" reads as every change, which limitation 4 forbids. Change the title to "See who or what made changes to issues and fields" and the body to "Changes to issues and fields are grouped by a person, an automation rule, an integration or an AI agent."
3. (Count corrections, no re-review needed) Subject A is 39 characters, not 38. The LinkedIn count line should say about 105 words, not 115.

### Advisory (non-blocking)
- In-app body opens with the fragment "Jira Cloud, after your first backup." It is correct but reads as a label. If the copywriter can keep 24 words or fewer, "Works on Jira Cloud, after your first backup." is 8 words and takes the body to 26, which is over the limit. Leave as is.
- "Specific plan tier" stays awkward until pricing is confirmed. Held by the plan-name proof request above.

Re-review needed for fixes 1 and 2 only. After they are made, the file passes.

## Copy revision second pass
Scope: 07-channel-copy.md after the copywriter applied fixes 1 to 3 above. Checked with Grep and a hand count. The four SVGs were read as source text. No shell tool, so no `git diff`; unchanged items were confirmed by presence and wording.

**Result: PASS.** No fixes required.

### Fix checks
| Check | Result |
|---|---|
| Release note step 3 | Pass. Now "3. [NEED PROOF: in-product path to start a rollback] Pick the rule, integration or AI agent and a time window." No screen, tab or button is named. |
| Same tag in the notes section | Pass. Notes line 104 carries it next to the step 1 tag. |
| First What's new bullet scoped | Pass. "See who or what made changes to issues and fields: Changes to issues and fields are grouped by a person, an automation rule, an integration or an AI agent." |
| Subject A count | Pass. Says 39 characters. Hand count is 39. |
| LinkedIn count | Pass. Says about 105 words. Hand count: 23 + 39 + 38 + 5 = 105. Under 120. |
| Email body count | Pass. Hand count: paragraph one 30, paragraph two 60, Good to know 52, so 142 without the CTA. The CTA is 4 or 5 words, so 146 to 147 with it. Under 150. The note "about 143 plus 4" is within one or two words of true. No breach. |
| Preview | Pass. 69 characters, as stated. |
| "Keep the work people did separately" | Pass. The sentence under it is "Separate edits people made after the bad event stay in place." That is the demonstrated case only. It does not cover same-field edits and promises nothing broader. |

### Nothing else changed
- Must say limitations: Jira Cloud, changes after the first Rewind backup, issues and fields, specific plan tier. All present in the email, in-app, release note and LinkedIn post.
- Attachment wording: "restored from the most recent backup, which may be up to 24 hours old" in the email, release note and LinkedIn. The in-app body keeps its shortened form, with the same 24 of 24 words. Never "under 24 hours". Carried-over advisory 4 (gate 4) still stands.
- [NEED PROOF] tags: step 1 and notes (turn on), step 3 and notes (path, new), attachment wording in the release note and notes, brand hex and typeface in the notes. None removed.
- In-app message: headline 7 words, body 24, button 2. Unchanged and within limits.
- On-image text matches the SVG text word for word in all four visuals, including the one-pager limits line (the LinkedIn apostrophe is curly only). Counts 13, 13, 17, 28 hold.

### Mechanical checks (Grep on 07)
- Em dashes, en dashes, exclamation marks: 0.
- Banned words from voice.md: 0.
- Internal terms (actor, Actor view, blast radius, selective, keep human): 0.
- "under 24", beta numbers (11, 14, 23, 4,000), quotes: 0.

### Advisory (non-blocking)
- The pass-one count notes for 07 (items 1 and 2 in the second-pass advisory list) are now closed. The 08 one-pager count (28, not about 29) and the in-app short-form attachment wording remain open.

07-channel-copy.md: **Pass.** It needs no human beyond the open [NEED PROOF] items already collected.

## Full open items
Moved here from the run report. The run report lists only the five decisions that block launch.

Blockers for the go/no-go at L-3 (see 06 and 10):
- GA date: `[NEED PROOF: GA date]` (01, 02, 06, 07, 10)
- Plan names and pricing: `[NEED PROOF: plan names and pricing]` (all customer-facing assets, which say "a specific plan tier")
- Brand sign-off: Rewind yellow `#FFC72C` and navy `#16225C`, plus the light neutral `#F5F8FD`, dark neutral `#0E102B` and Cabin, are unconfirmed. `[NEED PROOF: confirm brand palette and typeface with Rewind's brand team]` (context/brand.md, 08, visuals/)
- Attachment wording: handoff "up to 24 hours old" versus `context/` "under 24 hours" (01, 02, 05, 07, 09)
- Source or approval for "Atlassian native has no actor-based rollback" (01, 02, 04)
- Legal review of "exportable for auditors", and sign-off to mention the Confluence roadmap (05, 07, 09)
- Competitor check on other third-party tools (01, 04, 09)
- Revenue operations: capture "AI governance cited as a buying reason" in the CRM; product analytics counting Actor view opens (06, 10)

Engineering and product unknowns (reps have holding lines in 09):
- How Actor view tells a person, rule, integration and AI agent apart
- What happens when a person edited the same field after the agent
- Which Jira data types beyond issues and fields can be rolled back
- Who can run a rollback; large-site behavior; audit log contents and export format
- How a customer turns the feature on (blocks the email CTA and the release note's first step)

Evidence and measurement:
- Approval to use any closed beta number or quote outside the team: `[NEED PROOF: approval to use closed beta results or quotes]`
- Baselines, targets and the definition of "active Jira customers" for the three proposed metrics
- Size of the eligible customer base; quiz pass mark (7 of 8 is proposed only)
- Brand team confirmation of the Boomerang yellow hex

Other notes:
- The SVGs load Cabin from Google Fonts, so they need internet to show Cabin when opened elsewhere. The PNGs are fixed.
- `learnings/field-feedback.md` has no entries, so the Sales Enablement Lead had nothing to support or flag.
- Input is a hypothetical closed beta handoff. The beta stats and customer feedback are mock.
