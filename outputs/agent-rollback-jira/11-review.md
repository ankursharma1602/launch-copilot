# Review: Agent Rollback for Jira (Tier 2)

First pass. Reviewed files 01 to 10 and all four SVG and PNG pairs in `visuals/`.

## Mechanical checks
- Em dashes and en dashes: 0 across the folder (text, entity forms and SVG checked).
- Banned words: 0 in customer-facing or rep-facing copy. "peace of mind" appears twice only as a rule being quoted (`03-audience.md` line 14, `05-messaging.md` line 58). Not a fail.
- Exclamation marks: 0 in copy. The only "!" hits are the XML comment openers in the SVG files.
- "Under 24 hours" near Agent Rollback: 0 in 07, 08, 09, 09b, 09c. It appears only as a "never say" rule in 02, 04, 06 and 10. Attachment wording is the PRD wording everywhere it is used.
- Native "has no actor-based rollback": never stated as fact. It appears only in "do not say" rules (09, 09b, 09c).
- Third-party claims: none. Customer names, quotes, speeds, ROI: none. No plan name, price or date in any asset.
- Tier scope: no blog outline, blog hero or Sales FYI produced. Four visuals only. Matches the Tier 2 matrix.
- Length limits (counted by hand, no shell available):
  - Email subjects: A is 44 characters (07 says 45), B is 32. Both under 50. Preview is 71 characters (07 says 76). Under 90. Body is about 135 words with placeholders. Under 150. One CTA.
  - In-app: headline 7 words, body 23, button 3. All within spec.
  - LinkedIn: about 105 words. Under 120. No hashtags.
  - Talk track: 146 words. Under 150.
  - On-image words: email header 24, banner 22, LinkedIn image 28 (08 says 27), one-pager 26. All under 30.
- On-image text versus SVG: all four SVGs match the on-image text in 08 word for word. PNGs viewed. No clipping or overlap. Sizes match the spec table (1200x400, 1280x320, 1200x627, 2550x3300). Placeholder palette is marked in the SVG comments and in 08. No logo, invented screenshot or number. No fear imagery.
- CSV: 7 columns on all 41 rows, all fields quoted, every "Depends On" entry matches a Task name exactly.
- Must-say limitations: all four present in the email, release note, LinkedIn post, 09 one-pager and FAQ, and tested in the quiz. The in-app message and banner carry first backup, platform and plan. Attachments are in the in-app message only. Confluence roadmap is left out of the in-app message and banner on purpose, because it has no sign-off. See the advisory notes below.

## Scores
| Asset | Positioning and messaging | Proof | Persona | Voice | Spec | Avg | Result |
|---|---|---|---|---|---|---|---|
| 01 Launch brief | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 02 Launch context | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 03 Audience | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 04 Positioning | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 05 Messaging | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 06 Campaign strategy | 5 | 3 | 5 | 5 | 3 | 4.2 | Fail (score math error, timing conflict with 10) |
| 07 Channel copy | 5 | 3 | 5 | 5 | 4 | 4.4 | Fail (misleading in-app attachment line) |
| 08 Design briefs | 5 | 5 | 5 | 5 | 3 | 4.6 | Fail (one-pager visual carries 1 of 4 limits) |
| Visual: email header | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: in-app banner | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: LinkedIn image | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| Visual: one-pager layout | 4 | 4 | 5 | 5 | 2 | 4.0 | Fail (limits missing, see 08) |
| 09 Sales enablement | 5 | 3 | 5 | 5 | 5 | 4.6 | Fail (invented attachment mechanism) |
| 09b Enablement session | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 09c Readiness quiz | 5 | 5 | 5 | 5 | 5 | 5.0 | Pass |
| 10 Launch checklist (CSV and md) | 4 | 5 | 5 | 5 | 3 | 4.4 | Fail (timing conflicts with 06) |

## Fixes required

### 06 Campaign strategy (writer: campaign-strategy-agent)
1. Quote: "**Down to Tier 3 (below 2.8):** the including tier turns out to be a small add-on and commercial impact drops to 2 and competitive weight to 2. Score would be 2.70."
   - Problem: The math is wrong. Moving commercial from 4 to 2 takes off 0.50 and competitive from 3 to 2 takes off 0.15. 3.55 minus 0.65 is 2.90, which is still Tier 2.
   - Fix: Make the scenario land under 2.8. For example: "commercial impact drops to 2, competitive weight to 2 and story value to 3. Score would be 0.50 + 0.50 + 1.00 + 0.30 + 0.45 = 2.75." The Tier 1 line (4.05) is correct.
2. Quote: "Session at L-5 to L-3. Quiz by L-2." and "Go or no-go at L-1." (also "Reps get the one-pager, talk track and FAQ by L-5").
   - Problem: `10-launch-checklist.csv` has go/no-go at L-2, quiz at L-3 and sales kit at L-6. Final review is at L-8 in 10, while 06 says "Build L-21 to L-10 ... built and reviewed."
   - Fix: Keep 06 as the authority on go/no-go (L-1) and the sales kit (by L-5). Change the Build row to "L-21 to L-8" so the L-8 Final review sits inside it. Keep "Quiz by L-2" as written, since a quiz at L-3 meets "by L-2". Then 10 conforms (see 10 below).
3. Quote: "All three come from the PRD, which labels them proposed." followed by a four-row table.
   - Problem: The table has four rows, and the first two overlap.
   - Fix: Say "Three come from the PRD. The first row is a working measure." Or drop the first row.

### 07 Channel copy (writer: copywriter-agent)
1. Quote (in-app body): "Deleted attachments: up to 24 hours old."
   - Problem: It reads as if the deleted attachments are up to 24 hours old. Must say 2 is that attachments are restored from the most recent backup, which may be up to 24 hours old. A customer-facing line must not blur this.
   - Fix: "Deleted attachments restore from a backup up to 24 hours old." That is 10 words in that sentence, so the body is still 24 words or fewer. Check it stays under 25 words. If it does not fit, cut "Not on every plan" from the body only, since the banner carries it.
2. Quote: "Headline: Undo one agent's changes, not the whole site. / Sub-line: Find it. Preview it. Restore only that. / Footer strip: ..." (email header) and "Sub-line: Keep your team's work. Preview before you restore." (LinkedIn image).
   - Problem: These blocks are 31 and 32 words, over the 30-word on-image cap. The one-pager block is far over. 08 had to cut them, so 07 no longer matches what is on the images. 10's Refresh visuals task says "Text matches 07-channel-copy.md", which would re-introduce the mismatch.
   - Fix: Replace the three on-image blocks with the text that is actually rendered: email header (headline plus the two-line footer, 24 words), LinkedIn image (sub-line "Keep your team's work.", 28 words), one-pager (headline, sub-head, "What to know", "Jira Cloud only at launch.", 26 words). Move the longer one-pager block text into a separate "body for the sales one-pager" section that points to 09.
3. Minor, no fail: character counts are off. Subject A is 44 (says 45). Preview is 71 (says 76). Fix the numbers in the copy and in the self-check.

### 08 Design briefs and one-pager layout (writer: design-director-agent)
1. Quote: "Jira Cloud only at launch." (the only text on the one-pager footer), with the box "What to know" left empty.
   - Problem: The one-pager visual says "Undo one agent's changes" but carries only 1 of the 4 must-say limitations. The first-backup limit is not on it at all. Its status is documented, but the PNG could be forwarded as it is.
   - Fix: Drop the sub-head to make room, or shorten it. Put the first-backup limit in the footer, word for word: "Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back." (headline 8 + "What to know" 3 + footer 16 = 27 words). Re-render the SVG and PNG. Keep the empty box for all four lines at fill time. Alternatively mark the file name or an on-canvas label as a template, not for distribution. The first option is preferred.
2. Minor: word counts in 08 are off by one for the LinkedIn image (28, not 27). Correct them.

### 09 Sales enablement (writer: sales-enablement-agent)
1. Quote (objection row "What about attachments an agent deleted?"): "So the restored file can be older than the deletion by up to that much."
   - Problem: Unsupported claim. The PRD says only that deleted attachments come from the most recent backup, which may be up to 24 hours old. It does not describe how the restored file relates to the deletion time. Stating a mechanism is invented detail.
   - Fix: Delete that sentence. End the answer at "...which may be up to 24 hours old." Add the proof tag `[NEED PROOF: what is and is not recoverable for attachments created or changed since the last backup]`.

### 10 Launch checklist, CSV and md (writer: launch-ops-agent)
1. Quote: `"Go or no-go","Enable",...,"L-2"` and "Go or no-go (L-2)" in the md.
   - Problem: 06 says go or no-go at L-1.
   - Fix: Change Due to L-1 in the CSV and md. The four Launch tasks at L depend on it, which still holds.
2. Quote: `"Send sales kit to reps",...,"L-6"`, `"Run readiness quiz",...,"L-3"`.
   - Problem: Not a strict conflict ("by L-5", "by L-2"), but 10 is a day earlier than 06 and 09b ("Session L-5 to L-3, quiz by L-2"). Two sets of dates will confuse the owners.
   - Fix: Set the sales kit to L-5, the session to L-5, and the quiz to L-2. Keep the dependency chain (kit, then session, then quiz, then go/no-go). Update the md in the same way.
3. Quote: `"Final review",...,"L-8"` with 06's "Build L-21 to L-10 ... built and reviewed".
   - Problem: Resolved by the 06 fix above (Build window to L-8). Check the final dates against it after 06 is revised.

## Advisory, not fails
- 05 requires the Confluence roadmap line wherever platform coverage is mentioned. The in-app message and banner say "Jira Cloud only." and omit Confluence. 07 explains this (no sign-off, length cap). It is a defensible deviation. A human should confirm it, or `05-messaging.md` should record the exception.
- `06-campaign-strategy.md` says Confluence date or roadmap needs sign-off. 02, 05, 07 and 09 all flag it. Consistent.
- Upstream chain check: 01 to 05 are consistent with each other and with `context/`. All four limitations from 02 appear where 05 says they must, except the in-app Confluence note above. 06 asset list matches the Tier 2 matrix exactly. 06 weighted score 3.55 is correct and lands in one band.
- Release note line "Keep using native for a full-site recovery" goes slightly past `context/company.md` ("built for full-site recovery") but matches 04's "right tool" wording. Acceptable.

## Open proof requests
These are the system working. None is a fail.
- GA date: 01, 02, 03 to 07, 09, 10 (task "Confirm GA date").
- Plan names and pricing: 01, 02, 03, 04, 05, 06, 07, 09, 10.
- Competitor capability check on other third-party backup tools: 01, 02, 04, 09, 10.
- Source or approval for the PRD claim that native "has no actor-based rollback": 01, 02, 04, 09, 10. The claim is not used anywhere.
- Sign-off to mention the Confluence roadmap publicly: 02, 03, 05, 07, 09, 10.
- Actor-type detection: 02, 03, 04, 05, 07, 09.
- Data types and fields that can be rolled back: 02, 04, 05, 09.
- Conflict handling when a person later edited the same issue or field: 02, 04, 05, 07, 09.
- Audit log retention, export format and any named standard: 02, 03, 04, 05, 09. Legal review pending (task in 10).
- Roles and permissions needed to run a rollback: 02, 03, 07, 09.
- Limits on time window and issue count, and rollback speed: 02, 04, 05, 09.
- Large sites above Atlassian's size limits for Agent Rollback: 02, 03, 09.
- Customer name, quote or benchmark: 01, 02, 04, 05, 09.
- Segment sizes and plan mix: 01, 03, 04, 06, 09, 10.
- Baselines and targets for the three success metrics, and channel baselines: 01, 06, 10.
- Brand palette, fonts, logo files, email CTA destination link, LinkedIn destination link, Actor view navigation path: 07, 08, 10.
- Migration-led fit and any market data: 03, 04.
- New, from this review: what is and is not recoverable for attachments created or changed since the last backup (to be added to 09 by the fix above).

## Second pass
Re-reviewed 06, 07, 08, the one-pager PNG and SVG (PNG viewed), 09 and 10 (CSV and md).

### Mechanical checks
- Em and en dashes (text and entity forms): 0 in the folder.
- Banned words: only the same quoted-rule hits as first pass (03, 05). Exclamation marks in 06 to 09: 0.
- "Under 24 hours" and "older than the deletion": 0 in 07, 08, 09.
- CSV: 40 tasks plus header, all 41 lines match 7 quoted fields. Every Depends On entry matches a Task name. The md lists the same 40 tasks.
- Dates agree across 06, 09b and 10: go/no-go L-1, sales kit L-5, session L-5, quiz L-2 (09b "by L-2"), final review L-8 inside 06's Build window "L-21 to L-8". QA, email test and approvals at L-3 match 06 "Ready L-3 to L-1".
- Counts verified by hand. Subject A 44, B 32, preview 71. In-app body 24 words. On-image: email header 24, banner 22, LinkedIn image 28, one-pager 42 (approved exception).

### First-pass fixes, checked
- 06 fix 1 (tier-down math): applied. 0.50 + 0.50 + 1.00 + 0.30 + 0.45 = 2.75, and the 2.90 note is correct.
- 06 fix 2 (timing): applied. Build L-21 to L-8, go/no-go L-1, kit by L-5.
- 06 fix 3 (metrics table): applied. The note now says the first row is a working measure.
- 07 fix 1 (in-app attachment line): applied. "Deleted attachments restore from a backup up to 24 hours old." The body is 24 words.
- 07 fix 2 (on-image blocks): applied. 07 now holds the exact rendered text for all four visuals. Longer one-pager block text moved to a separate "Body for the sales one-pager" section that points to 09.
- 07 fix 3 (character counts): applied.
- 08 fix 1 (one-pager limits): applied in a different way than first suggested, and acceptable. The footer carries limits 1 and 3 in full, and the "What to know" box carries 2, 3 and 4 in short form. All four limits are on the PNG.
- 08 fix 2 (LinkedIn word count): applied, 28.
- 09 fix (attachment mechanism): applied. The invented sentence is gone. The answer ends at "up to 24 hours old", with the requested NEED PROOF tag added.
- 10 fixes: applied. Go/no-go L-1, kit L-5, session L-5, quiz L-2.

### Text match, 07 versus 08 versus visuals
07 on-image text equals 08 on-image text equals the SVG text for all four visuals. The one-pager SVG matches 08 word for word (headline, box title, three box lines, two-line footer). The PNG shows no clipping or overlap, three empty cards, an empty logo area, and the footer and box inside margins. No logo, number or invented screenshot.

### Results
| Asset | Result |
|---|---|
| 06 Campaign strategy | Pass |
| 07 Channel copy | Pass |
| 08 Design briefs | Pass |
| Visual: one-pager layout | Pass (42 words is an approved exception, all four limits present) |
| 09 Sales enablement | Pass |
| 10 Launch checklist (CSV and md) | Pass |

No fails remain. Nothing needs a human beyond the open proof requests above.

### Advisory notes, not fails
- 08 line on the one-pager says the box short forms "are not word for word from 07, which only says filled from 09". This is stale, since 07 now lists the box lines verbatim. Edit 08 to say they match 07.
- The box line "Attachments: backup up to 24 hours old." is terse. It reads correctly beside the footer, but at fill time the card text from 09 must carry the full wording "restored from the most recent backup, which may be up to 24 hours old."
- Task "Fill one-pager from 09" in 10 says the What to know box carries all four limits "in full". The rendered layout splits them between box and footer. Reword to "all four limits appear on the page, in full where space allows, with the full attachment wording in the cards."
- In the 10 md, the L-2 quiz line sits before the L-3 items in the Enable list. Cosmetic.
- The in-app and banner Confluence omission advisory from the first pass still stands for a human to confirm.
