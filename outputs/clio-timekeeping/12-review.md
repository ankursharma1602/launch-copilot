# Review: Clio Timekeeping GA

Mechanical checks: 0 em or en dashes, 0 banned words, 0 exclamation marks, 0 "beta" or "opt in" in customer copy, 0 `[NEED PROOF]` in any body. Subjects are 33 and 36 characters. 4Cs maths is right (3.50, Tier 2) and 07 takes the tier from 03. Dates in the CSV match 07 and the run calendar. All plans for GA, none for the beta.

## Quality scorecard
| Asset | Result after fixes | Score (first review) | Note |
|---|---|---|---|
| 01 launch brief | Pass | 3 | |
| 02 launch context | Pass | 3 | |
| 03 tiering | Pass | 4 | |
| 04 audience and persona PNG | Pass | 3 | |
| 05 positioning | Pass | 3 | |
| 06 messaging | Pass | 4 | |
| 07 campaign strategy | Pass | 4 | |
| 08 channel copy | Pass | 4 | |
| 09 design briefs | Pass | 4 | |
| Email header | Pass | 4 | |
| In-app banner | Pass | 4 | |
| LinkedIn image | Pass | 4 | |
| One-pager layout | Pass | 4 | |
| 10 sales enablement | Pass | 3 | |
| 10b enablement session | Pass | 4 | |
| 10c readiness quiz | Fail | 3 | source reference to fix |
| 11 launch checklist | Pass | 4 | |

Legend: scores are from the first review (1 to 5 on the quality bar). The second review gave pass or fail only, so a Pass with a score under 4 means it failed first and passed after its fixes.

Remark: 07: new showcase tables added after review, not re-reviewed.

## Fixes required

### 04-audience.md and visuals/audience-personas.svg and .png
- Quote: "Clio Manage, Outlook, OneDrive, Clio Insights" (Tech stack, Partner Priya). Problem: "Clio Insights" is not in context/. The source says "Benchmarking and Insights". Fix: "Clio Manage, Outlook, OneDrive, Benchmarking and Insights". Change it in the table, the SVG (line 59) and re-render the PNG.
- Quote: row dividers `#E5E5E5` in the SVG. Problem: not in the brand table. Fix: use `#F5F5F5` bands only, or `#CCC4BA`, and re-render. Everything else on the PNG passes: black band, live "Clio" text, Inter renders, four tint headers in brand colours, nothing clipped, no blank cells.

### 05-positioning.md and 10-sales-enablement.md and 10c-readiness-quiz.md: the timer claim
Judgement: no source supports it. The handoff says only that firms "used timers". Nothing says a timer must be started each time. It is also a claim about an alternative that 06 "Avoid saying" tells writers not to frame ("Timer" framing). Benchmark: the help article says what Timekeeping does ("automatically captures billable activity and drafts time entries"), it never describes another tool.
- 05, Alternatives table. Quote: "Has to be remembered and started each time". Fix: "Records only the time you chose to track".
- 10, Objection 1. Quote: "A timer has to be started each time. This drafts entries while you work. You check each one." Fix: "Keep using it if it works for you. Timekeeping drafts entries from your activity while you work, and you check each one."
- 10, Competitive quick take. Quote: "Timer | Must be started each time | Entries are drafted for you and land in Clio Manage". Fix: "Timer | Records only what you chose to time | Entries are drafted from your activity and land in Clio Manage".
- 10c, answer 4. Quote: "A timer has to be started each time. Timekeeping drafts entries while you work, and you check each one." Fix: "Timekeeping drafts entries from your activity while you work, and you check each one."

### 08-channel-copy.md
- LinkedIn post omits the own-entries limit that 06 "Must say" 2 requires. Quote: "Matter suggestions can be wrong, so you review every entry. Timekeeping drafts. You approve." Fix: "Matter suggestions can be wrong, so you review every entry. You see only your own entries. Timekeeping drafts. You approve."
- Quality bar. Weak: "On Friday afternoon, you rebuild the week from sent mail." Benchmark: "Entries usually appear about 15 minutes after the activity." Fix: "Lawyers often rebuild the week from sent mail on Friday afternoon." Adds no claim and stops telling the reader what they do.
- Advisory: the in-app message has only limits 1 and 4. Acceptable at that length.

### 11-launch-checklist.md (Mermaid)
- Quote: "Email 9:00 a.m. - Lifecycle marketing (L-0) :l1, 2027-02-02, 1d". Problem: Mermaid splits the task at the first colon, so "9:00" breaks the line and the chart will fail or misread. Fix: "Email at 9 a.m. - Lifecycle marketing (L-0) :l1, 2027-02-02, 1d". The rest of the syntax reads valid. The CSV is well formed, quoted, and every Depends On entry matches a Task name.

### 01-launch-brief.md (about 980 words, cut to about 600)
- Cut the "Goals" table. It repeats the KPIs in "Launch at a glance" row 4.
- Cut the "Timeline" table. It repeats the Key dates row, 07 and the 11 checklist.
- Cut "Why it matters to the business". Its own text says it picks no driver.
- Quote: "Revenue operations cannot yet track opt-ins by firm size in the CRM." Fix: "Revenue operations cannot yet track setup by firm size in the CRM." This is beta wording in a GA plan.

### 02-launch-context.md (about 1,170 words, cut to about 650)
- Cut "What closed beta customers said" to a two-line internal note. The numbers table, "Who got the most value", the four quotes and "Friction and requests" are unused internal evidence. 04 already carries the persona signal.
- Cut "Beta to GA", which repeats earlier sections, and "Dependencies", which repeats Setup and the open questions.
- Quote: "Status of this feedback: invented for the demo and marked illustrative in the handoff." Fix: "Internal evidence, illustrative, not for outside use." Drop "Must say: yes" fragments from the limitations list.

### 03-tiering.md
- Cut "Out of scope on purpose" and "What would change the tier". CLAUDE.md rule 10: do not explain omissions. Keep the scorecard, maths, tier, override line and in-scope table.

### 05-positioning.md
- Cut "What Clio Timekeeping does", "Alternatives, in short" and "Trends". Each repeats a canvas row. Keep the canvas, "Market category" and "What this means for messaging".

## Checks that passed, one line each
- GA plan: pre-launch, launch day Tue Feb 2, 2027, post-launch to May 3. CTA is "Try Clio Timekeeping".
- Visuals: email header, banner and LinkedIn image follow the minimal black pattern with the white pill, thin Inter headline and one warm object. The banner adds one Clio blue button. The one-pager is white with a black band and one UI card. Text matches 08 word for word. Sizes match. Only palette breach is the `#E5E5E5` above.
- Advisory 09: the one-pager has no limits line. The skill asks for one small limits line, and the brief says 08 gives none. Add "Setup comes first. You see only your own entries." to 08 and the layout, or accept the exception.

## Second pass (2026-11-09)

Mechanical re-check: 0 em or en dashes in outputs, 0 banned words, 0 exclamation marks, 0 "beta" or "opt in" in 08, `[NEED PROOF]` only in this review file. Every SVG colour is in `context/brand.md` (no `#E5E5E5` left). The personas PNG was opened: "Benchmarking and Insights" shows, nothing clipped, no blank cells. 09 on-image text matches 08 word for word. The 11 Mermaid gantt block was read line by line and is valid: no stray colons, every task has an id and dates.

| File | Result |
|---|---|
| 01 launch brief | PASS |
| 02 launch context | PASS |
| 03 tiering | PASS |
| 04 audience, SVG, PNG | PASS |
| 05 positioning | PASS |
| 08 channel copy | PASS (own-entries line in LinkedIn post, new email sentence reads plain) |
| 09 design briefs | PASS |
| 10 sales enablement | PASS |
| 10c readiness quiz | FAIL (minor) |
| 11 checklist md | PASS |

### Needs a human
- 10c, answer key row 4. Quote: "Timekeeping drafts entries from your activity while you work, and you check each one. | 05, Alternatives". Problem: the "Alternatives" section was cut from 05, so the source reference points at nothing. Fix: change it to "05, Competitive alternatives" (the canvas row) or "10, Objection 1".

## Full open items
- Desktop capture and data handling: Legal and Product.
- Admin and biller visibility of others' entries: Customer success and Product.
- "About 15 minutes", with or without "usually": Support lead and Product. Copy says "shortly after".
- Beta numbers and quotes outside Clio: Product marketing, Legal and the beta firms.
- Growth driver and any competitor claim: Product marketing leadership and Sales Engineering. Competitive score 2 and Commercial score 3 are judgements.
- "AI" wording in public copy: Legal.
- Matter suggestion ranking and error rate: Engineering lead.
- Date, plans, regions final; brand palette and rolled-paper object: Product manager and Brand team.
- Per-user billable time baseline and CRM tracking by firm size: Revenue operations.
- 10c answer key source reference (above): Sales enablement lead.
- Accepted: the one-pager has no limits line, because customer-facing copy carries no caveats.
