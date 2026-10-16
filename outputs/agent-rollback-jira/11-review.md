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
  - Hex codes used are only #F5F8FD, #16225C, #0E102B and #FFFFFF, plus Blue Zodiac opacity tints. No yellow.
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
