# Review: Agent Rollback for Jira (Tier 2)

Review date: 2026-10-16. First pass. Assets reviewed: 01 through 05 (including `05-launch-checklist.csv`).
Sources read first: CLAUDE.md, all of `context/`, `learnings/lessons.md`, the input PRD, the brand-review and channel-copy skills.

## Mechanical checks
- **Em dashes (—) and en dashes (–):** 0 across the output folder (Grep).
- **Exclamation marks:** 0 across the output folder (Grep).
- **Banned words** (all 16 in `voice.md`, case-insensitive, including "leverag" for the verb): 0 matches (Grep).
- **Email subject length (limit 50, lessons.md and channel-copy spec):** Subject A "Undo one agent's changes in Jira" = 32. Subject B "Roll back the agent, keep your team's work" = 42. Both pass.
- **Email preview (limit 90):** "Find every change one agent or rule made, and undo only those." = 62. Pass.
- **Email body (limit 150 words):** about 126 words. Pass. One CTA. Pass.
- **In-app (headline under 8 words, body under 25, button under 4):** headline 6, body 18, button 3. Pass.
- **LinkedIn (under 120 words, max 2 hashtags, no emojis):** about 110 words including hashtags, 2 hashtags, no emojis. Pass, but only 10 words of headroom (matters for the fix below).
- **Unapproved numbers and claims:**
  - "4,000 issues" and "30 projects" appear in `02-launch-brief.md` and the LinkedIn post. Both are from the PRD and labeled as examples. Pass.
  - "16 cloud applications" and "more than 25,000 organizations" are in `proof-points.md`. Pass.
  - "up to 24 hours" is used only for attachments, as in the input. "Under 24 hours" is not used. Pass.
  - No "first" or "only" market claims (Grep of 03 shows only the limitation wording and the reviewer notes). Pass.
  - No customer names, quotes, prices, dates or benchmarks. Pass.
  - Two soft generalizations in the talk track, see Fixes.
- **Three known limitations coverage** (first-backup only / attachments up to 24 hours old / Jira Cloud only, Confluence undated). The brief says these are "must-say ... for every asset."

| Asset | First backup | Attachments up to 24h | Jira Cloud only | Result |
|---|---|---|---|---|
| 02 Brief | Yes | Yes | Yes | OK |
| 03 Email | Yes | Yes | Yes (no Confluence promise) | OK |
| 03 In-app | **No** | **No** | Yes ("Jira Cloud.") | **Missing 2** |
| 03 Release note | Yes | Yes | Yes (Confluence undated) | OK |
| 03 LinkedIn | Yes | **No** | Yes | **Missing 1** |
| 04 One-pager | **No** | **No** | Partial ("Do not say ... Confluence" only, no statement of Jira Cloud only) | **Missing 3** |
| 04 Talk track | Yes | **No** | Yes | **Missing 1** |
| 04 Objections | Yes | n/a | n/a | OK |
| 04 FAQ | Yes | Yes | Yes | OK |

- **CSV validity** (`05-launch-checklist.csv`, 39 lines, header plus 38 tasks, 7 columns expected). A strict RFC 4180 pattern matched 36 of 39 lines. Three lines do not parse cleanly:
  - Line 4: unquoted field containing `""` characters.
  - Line 9: unquoted field containing `""` characters.
  - Line 23: unquoted field containing commas, so a parser reads **9 columns instead of 7** and shifts every later field (Phase, Owner, Due, Depends On, Definition of Done and Status land in the wrong columns).
  - Result: **fail**.

## Scores
| Asset | Positioning | Proof | Persona | Voice | Channel | Avg | Result |
|---|---|---|---|---|---|---|---|
| 01 Tier decision | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| 02 Launch brief | 5 | 4 | 5 | 5 | 5 | 4.8 | **Pass** |
| 03 Channel copy: email | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| 03 Channel copy: release note | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| 03 Channel copy: in-app | 4 | 5 | 4 | 5 | 2 | 4.0 | **Fail** (missing required limitations) |
| 03 Channel copy: LinkedIn | 5 | 5 | 4 | 5 | 3 | 4.4 | **Fail** (missing required limitation) |
| 04 Sales enablement | 4 | 3 | 5 | 5 | 3 | 4.0 | **Fail** (missing required limitations, unsupported generalization) |
| 05 Checklist (.md) | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| 05 Checklist (.csv) | 5 | 5 | 5 | 5 | 1 | 4.2 | **Fail** (does not parse cleanly) |

Note: in-app, LinkedIn and sales fail on the "missing required parts" and "unsupported claim" conditions, not on average score. A pass needs both no fail condition and an average of 4.0 or higher.

## Fixes required

### 03-channel-copy.md: In-app message
- Quote: "**Body:** Find every change an agent, rule or integration made, preview it, and roll back only that. Jira Cloud."
- Problem: The brief requires all three limitations in every asset. This body states only Jira Cloud. It does not say rollback covers only changes after the first backup, or that attachments restore from a backup up to 24 hours old.
- Fix: Replace the body with a version that fits under 25 words. Suggested (24 words): "Roll back one agent's changes, keep human work. Only changes after your first backup. Deleted attachments may be 24 hours old. Jira Cloud only." If the team wants "preview" kept in the body, the attachment line cannot also fit. In that case the PMM must record a decision on the brief that the in-app message links to the release note for the attachment limitation, and still carry the first-backup line. Headline and button are fine.

### 03-channel-copy.md: LinkedIn post
- Quote: "Only changes after your first Rewind backup can be rolled back. Jira Cloud only for now."
- Problem: The attachments limitation (deleted attachments restore from a backup up to 24 hours old) is missing. It is a must-say limitation for every asset.
- Fix: Add one sentence after the quoted line: "Attachments an agent deleted come back from the latest backup, which may be up to 24 hours old." That is 17 words. To stay under 120, delete the line "That is an example, but admins know the feeling." (9 words) and change the hook to "An AI agent reclassifies thousands of Jira issues. Now what?" so no unlabeled specific number remains. Result is about 118 words including hashtags. Also update the matching reviewer note about the "4,000 issues" example, which would no longer apply.

### 04-sales-enablement.md: One-pager
- Quote: "**Do not say:** "first," "only," or that it works on Confluence. Do not quote price, plan or GA date."
- Problem: The one-pager contains none of the three limitations as statements. "Do not say Confluence" is an instruction to reps, not the must-say limitation, and the page never says Jira Cloud only, after-first-backup only, or the 24-hour attachment age. A rep working from this page alone could oversell.
- Fix: Add a "Limits to state up front" line to the one-pager: "Only changes made after the customer's first Rewind backup can be rolled back. Attachments an agent deleted come back from the most recent backup, which may be up to 24 hours old. Jira Cloud only. Confluence is on the roadmap with no committed date." Keep the "Do not say" line.

### 04-sales-enablement.md: Talk track
- Quote: "It covers changes made after your first Rewind backup, and it's Jira Cloud today."
- Problem: The attachments limitation is missing from the talk track.
- Fix: Add after the quoted sentence: "One thing to know: attachments an agent deleted come back from the most recent backup, which can be up to 24 hours old."

### 04-sales-enablement.md: Talk track, unsupported generalizations
- Quote 1: "it rarely gets one thing wrong. It's hundreds or thousands of issues."
- Problem: A frequency claim about customer incidents stated as fact. The PRD gives two example scenarios, not a pattern or a number. Unsupported claim under proof integrity.
- Fix: Replace with "When an agent or rule gets something wrong in Jira, the damage can run to thousands of issues, because that is the scale they work at."
- Quote 2: "That's usually what IT wants to see before they approve more agents."
- Problem: "Usually" asserts a pattern across customers with no proof. The PRD says only that IT and security leaders "want a recovery plan before they say yes."
- Fix: Replace with "IT and security teams often want a recovery plan before they approve an agent. Is that true for you?" or cut the sentence.

### 05-launch-checklist.csv
- Problem: Three rows break CSV parsing. Line 23 gets 9 columns, shifting Phase, Owner, Due, Depends On, Definition of Done and Status.
- Fix: Wrap the Task field in double quotes on these three lines.
  - Line 4: `"Confirm recovery point wording (""under 24 hours"" vs ""up to 24 hours"")",Prepare,...`
  - Line 9: `"Decide feature name vs headline (does ""Agent Rollback"" undersell automation rules and integrations)",Prepare,...`
  - Line 23: `"Run Sales enablement session (one-pager, talk track, FAQ)",Enable,...`
- Related, same file: the Depends On column refers to tasks by name, and two names do not match the Task column exactly. "Confirm recovery point wording" (rows 13, 14, 15, 19) does not match line 4, and "Decide feature name vs headline" (rows 13, 14, 16) does not match line 9, because the Task fields carry parentheticals. Fix: shorten the Task names on lines 4 and 9 to "Confirm recovery point wording" and "Decide feature name vs headline", and move the parenthetical text into Definition of Done. That also removes the need for escaped quotes on those two lines. Minor: line 13's Definition of Done says "Draft in 03 asset folder", but the email lives in `03-channel-copy.md`. Change to "Draft in 03-channel-copy.md".
- After the fix, re-validate: 39 lines, 7 columns each.

## Advisory (not fails)
- `04-sales-enablement.md`, objection row: "Agents will make mistakes at scale, like any fast system." It does not blame the AI owner, so it passes `voice.md`. Consider "Fast systems fail at scale, including agents" so the framing stays on the system and not the agents.
- `02-launch-brief.md`: "Agent Rollback is the most direct answer to that driver so far." "So far" implies a comparison with other Rewind work that nothing in context supports. Internal doc, so not a fail. Cut "so far".
- `02-launch-brief.md` and `05-launch-checklist.md` correctly flag the 3.95 rubric gap. `01-tier-decision.md` arithmetic checks out: 0.75 + 1.00 + 1.00 + 0.60 + 0.60 = 3.95, and the reach-2 sensitivity of 3.70 is correct.
- Release note step list is customer-facing but carries a `[NEED PROOF: exact navigation labels and UI path]`. Correctly flagged. It must be resolved before the release note ships (the checklist already covers this at L-7).

## Open proof requests (not fails)
- `02-launch-brief.md` and `01-tier-decision.md`: GA date.
- `02-launch-brief.md`: how conflicts are handled when a person edited the same field after the agent did.
- `02-launch-brief.md`: customer or design-partner example of an AI rollout approved with Agent Rollback in place.
- `02-launch-brief.md`: baseline and target (leading metric); baseline and target (lagging metric); confirm sales ops can track AI governance as a buying reason.
- `02-launch-brief.md`: product confirmation of attribution method (agents under a user account or shared API token).
- `02-launch-brief.md`: competitor capability check (other third-party backup tools) and plan names and pricing (in Open questions).
- `03-channel-copy.md`: exact navigation labels and UI path for the release note steps.
- `03-channel-copy.md`: plan names and pricing; GA date (release note availability line).
- `03-channel-copy.md` (reviewer notes): same-field conflicts, attribution method, customer example.
- `04-sales-enablement.md`: same-field conflict handling (objections and FAQ); attribution method (objections and FAQ); plan names and pricing (objections and FAQ); GA date (FAQ); customer or design-partner example (FAQ); competitor capability check (competitive table).
- `05-launch-checklist.csv`: placeholders are referenced as tasks, not used as claims.

## Summary
- Pass: 01, 02, 03 email, 03 release note, 05 checklist .md.
- Fail, one revision pass needed: 03 in-app, 03 LinkedIn, 04 (one-pager, talk track), 05 CSV.
- Items for a human regardless of revision: all open proof requests above, the 3.95 tier boundary, and the in-app space decision for the attachments limitation.

## Second pass

Review date: 2026-10-16. Scope: only the revised assets (in-app, LinkedIn, one-pager, talk track, CSV). Also confirmed the "so far" cut in `02-launch-brief.md`.

### Mechanical checks
- Em dashes and en dashes: 0 in the output folder (Grep). Exclamation marks: 0. Banned words (all 16, case-insensitive): 0. The only hits are the check descriptions inside this file.
- In-app: headline "Undo one agent, keep human work" = 6 words (limit under 8). Body = 24 words (limit under 25). Button "See Actor view" = 3 words (limit under 4). Pass.
- LinkedIn: about 116 words of text plus 2 hashtags = about 118 (limit under 120). 2 hashtags, no emojis. First line works as a standalone hook. Pass.
- Talk track: about 183 words, which is a little over 60 seconds at a normal speaking pace. No word limit exists in the spec, so advisory only.
- Unapproved claims: none. No "first" or "only" market claims, no customer names, prices, dates or benchmarks. The two talk-track generalizations from the first pass are gone ("the damage can run to thousands of issues" describes a scenario, and the IT line is now a question to the buyer). Pass.
- CSV (independent check): 39 lines, header plus 38 tasks. A strict RFC 4180 pattern for exactly 7 fields matched 39 of 39 lines. Lines 4, 9 and 23 now parse cleanly. Every Depends On entry (semicolon-separated) matches a Task name exactly, including rows 13 to 19, 21, 28, 29, 37 and 38. Line 13 now says "Draft in 03-channel-copy.md". Pass.

### Three known limitations coverage
| Asset | First backup | Attachments up to 24h | Jira Cloud only | Result |
|---|---|---|---|---|
| 03 In-app | Yes ("Only changes after your first backup.") | Yes ("Deleted attachments may be 24 hours old.") | Yes | OK |
| 03 LinkedIn | Yes | Yes ("may be up to 24 hours old") | Yes | OK |
| 04 One-pager | Yes ("Limits to state up front" 1) | Yes (2) | Yes (3), Confluence has no committed date | OK |
| 04 Talk track | Yes | Yes ("can be up to 24 hours old") | Yes ("Jira Cloud today") | OK |

### Scores and results
| Asset | Positioning | Proof | Persona | Voice | Channel | Avg | Result |
|---|---|---|---|---|---|---|---|
| 03 In-app | 5 | 5 | 4 | 5 | 5 | 4.8 | **Pass** |
| 03 LinkedIn | 5 | 5 | 4 | 5 | 5 | 4.8 | **Pass** |
| 04 One-pager | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| 04 Talk track | 5 | 5 | 5 | 5 | 4 | 4.8 | **Pass** |
| 05 Checklist (.csv) | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |

No fails remain in the revised assets.

### Advisory (not fails)
- In-app body: "Deleted attachments may be 24 hours old." The source says "up to 24 hours old". "May be 24" reads as exactly 24 and there is no word of headroom to add "up to". Acceptable. If the in-app tool allows 26 words, use "up to".
- One-pager: "**Do not say:** "first," "only," or that it works on Confluence." The same page tells reps to say "Only changes ... after the customer's first Rewind backup". Make the intent clear: "Do not claim Rewind is the first or only tool." Not a fail because the intent is market claims.
- Talk track: about 183 words. Trim the last question or one sentence in paragraph 2 to land near 60 seconds.
- `02-launch-brief.md`: "so far" removed from "most direct answer to that driver." Resolved.

### Second pass summary
- Pass: in-app, LinkedIn, one-pager, talk track, 05 CSV.
- Still needs a human: the open proof requests listed above, the 3.95 tier boundary. No new items.

## Design briefs review

Review date: 2026-10-16. Scope: `07-design-briefs.md` only, against `03-channel-copy.md`, the brand-review "Design briefs" checks and the design-brief skill. No other asset reviewed.

### Mechanical checks (Grep on 07-design-briefs.md)
- Em dashes and en dashes: 0.
- Exclamation marks: 0. The word "exclamation marks" appears only inside avoid lists, as an instruction.
- Banned words (all 16 in `voice.md`, case-insensitive, including "leverag"): 0 matches.
- Tier scope: email header, in-app banner, LinkedIn image, one-pager layout produced. Blog hero skipped and the skip is stated. Matches the skill.
- Sizes: 1200 x 400, 1280 x 320, 1200 x 627, 2550 x 3300. All match the spec table.
- Each prompt has asset name and size, on-image text, layout, visual direction, brand note and avoid list. Pass.
- Invented brand colors, logos, screenshots, numbers or names: none. Brand items are `[NEED PROOF: brand palette, fonts and logo files]`. Pass.
- Fear imagery or framing AI owners as the problem: none. The LinkedIn prompt treats the AI agent lane "neutrally, as one actor among four". Pass.

### On-image text, word for word against 03-channel-copy.md
| Asset | On-image text | Source found in 03 | Words | Result |
|---|---|---|---|---|
| Email header | "Roll back the agent, keep your team's work" | Customer email, Subject B, exact | 8 | Match |
| In-app banner | "Undo one agent, keep human work" | In-app Headline, exact | 6 | Match |
| LinkedIn headline | "Undo one agent's changes in Jira Cloud, without a full-site restore" | Release note Title, exact | 11 | Match |
| LinkedIn lane labels | "Person", "Automation rule", "Integration", "AI agent" | Release note, Actor view bullet: "a person, an automation rule, an integration or an AI agent". Articles cut, first letter capitalised. | 1+2+1+2 = 6 | Match (cut only) |
| One-pager headline | same as LinkedIn headline | Release note Title, exact | 11 | Match |
| One-pager subhead | "People's work stays in place. You see what will change before you restore." | Release note Summary, last two sentences, exact | 13 | Match |

Totals: email header 8, in-app 6, LinkedIn 17, one-pager 24. All match the stated counts and all are under 30.

### Limitation check
The skill requires each prompt to state that the image does not contradict the limitations (for example "does not claim support beyond Jira Cloud").
- In-app prompt: states it. Pass.
- LinkedIn prompt: states it, also first-backup and restore time. Pass.
- One-pager prompt: limitations slot is specified and sized, and the headline names Jira Cloud. Pass.
- Email header prompt: **does not state it.** The only statement is in the file-level "Limitations note", which does not travel with a prompt pasted alone. Fail.

### Scores
| Asset | Positioning | Proof | Persona | Voice | Channel | Avg | Result |
|---|---|---|---|---|---|---|---|
| Email header | 5 | 5 | 4 | 5 | 3 | 4.4 | **Fail** (missing required prompt statement) |
| In-app banner | 5 | 5 | 4 | 5 | 5 | 4.8 | **Pass** |
| LinkedIn image | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| One-pager layout | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |

### Fixes required

#### Email header
- Quote: the Prompt block for the email header ends with "Avoid: red alarms, warning triangles, skulls, glitch effects, robots, glowing brains, sci-fi AI imagery, stock photos of people pointing at screens, any Atlassian or Jira logo or mark, lorem ipsum, any text beyond the line above, exclamation marks, fake screenshots, ticket numbers or counts."
- Problem: Design-brief skill, "Rules for on-image text": the prompt must state that the image does not claim support beyond Jira Cloud. This prompt says nothing about limits, so a designer pasting it alone could add imagery implying Confluence or retroactive recovery. The headline also does not name Jira Cloud, so the prompt is the only guard.
- Fix: Insert this paragraph in the prompt, directly above the "Avoid:" line, copied from the pattern used in the in-app prompt: "The header must not claim anything beyond what the email says. It does not imply support beyond Jira Cloud or recovery of changes made before the first backup." No change to the on-image text, layout or size.

### Advisory (not fails)
- One-pager prompt, footer strip: `a "Hypothetical, not a real product" or legal note`. The quoted string is not in `03-channel-copy.md`, and the prompt also says "No words in the template". A design tool may render the quoted string as text. Suggested change: "plus a small empty slot for a legal or disclaimer note, left blank." Not a fail because it is described as an empty slot.
- Email header prompt says "one line or two". At half size (600 px) a two-line headline of 42 characters is fine, but pin it to "two lines" if the designer needs a fixed layout.

### Open proof requests (not fails)
- `07-design-briefs.md`: brand palette, fonts and logo files (all four assets).
- `07-design-briefs.md`: brand rules for showing the Jira or Atlassian name.
- `07-design-briefs.md`: `04-sales-enablement.md` one-pager body text, to be pasted into the empty slots later.
- `07-design-briefs.md`: plan names, pricing and GA date, inherited from `03-channel-copy.md`. No visual shows them.

### Design briefs summary
- Pass: in-app banner, LinkedIn image, one-pager layout.
- Fail, one revision pass needed: email header (add the no-overclaim statement to the prompt).

## Design briefs review, second pass

Review date: 2026-10-16. Scope: `07-design-briefs.md` after revision. Re-checked the email header and one-pager layout. Mechanical checks run on the whole file.

### Mechanical checks (Grep on 07-design-briefs.md)
- Em dashes and en dashes: 0.
- Exclamation marks: 0 literal "!" characters. The word "exclamation marks" appears only in the four Avoid lines (lines 41, 71, 104, 142), as an instruction.
- Banned words (all 16 in `voice.md`, case-insensitive, including "leverag"): 0 matches.

### On-image text
| Asset | On-image text | Source in 03-channel-copy.md | Words | Result |
|---|---|---|---|---|
| Email header | "Roll back the agent, keep your team's work" | Customer email, Subject B, exact | 8 | Match |
| In-app banner | "Undo one agent, keep human work" | In-app Headline, exact | 6 | Match |
| LinkedIn image | Release note Title (11) plus four lane labels (6, cut only) | Exact / cut only | 17 | Match |
| One-pager | Release note Title (11) plus Summary last two sentences (13) | Exact | 24 | Match |

All still word for word and all under 30. The stated counts in the file header (8, 6, 17, 24) are correct.

### Email header (re-check)
- Fix applied: the prompt now contains "The header must not claim anything beyond what the email says. It does not imply support beyond Jira Cloud or recovery of changes made before the first backup." It sits directly above the Avoid line, inside the pasteable block. Pass.
- Advisory applied: "one line or two" is now "two lines". Pass.
- On-image text, layout and size unchanged. No new claims.

### One-pager layout (re-check)
- Footer strip now reads "a small empty slot for a legal or disclaimer note, left blank. No words in the template." The unsourced quoted string is gone, so a design tool has no text to render. Pass.
- Limitations slot is still sized to hold three bullets and cannot be dropped. Headline names Jira Cloud. Rest of the prompt unchanged.

### Scores
| Asset | Positioning | Proof | Persona | Voice | Channel | Avg | Result |
|---|---|---|---|---|---|---|---|
| Email header | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |
| One-pager layout | 5 | 5 | 5 | 5 | 5 | 5.0 | **Pass** |

The in-app banner and LinkedIn image were not edited and keep their first-pass Pass.

### Second pass summary
- Pass: email header, in-app banner, LinkedIn image, one-pager layout.
- No fails remain. Open proof requests from the first design review stand (brand palette, fonts and logo files; Jira or Atlassian name rules; one-pager body text from `04-sales-enablement.md`; plan names, pricing and GA date). No new items.
