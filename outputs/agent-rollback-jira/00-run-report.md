# Launch CoPilot run report: Agent Rollback for Jira

**Tier:** 2 (weighted score 3.55), no override
**Run time:** about 15 minutes
**Assets produced:** 16 | **Passed review first time:** 10 | **Revised:** 6 | **Needs a human:** 0 failed twice, but open items below block launch

The 16 assets: files 01 to 09c (11), the launch checklist (1), and four visuals. The first-pass failures were 06, 07, 08 (with the one-pager visual), 09 and 10. All six passed the second review.

## The launch in three lines
Agent Rollback lets a Jira Cloud admin find and undo every change made by one AI agent, automation rule or integration, without restoring the whole site or touching people's work.
It is for Jira admins running agents or heavy automation, and for the IT or security leaders who must approve those rollouts.
It matters now because agents edit Jira at a scale no person does, and approvers want a recovery plan before they say yes.

This is a hypothetical PRD written to demo Launch CoPilot, not a real Rewind product.

## Decisions the system made
- **Tier 2, score 3.55.** Customer reach 2, commercial impact 4, strategic fit 5, competitive weight 3, story value 4. Reach is low because it is Jira Cloud only, one plan tier, and needs an existing Rewind Jira backup. Reaching Tier 1 would need reach to rise to 4 (4.05). Falling to Tier 3 would need commercial impact 2, competitive weight 2 and story value 3 (2.75).
- **Not produced on purpose:** blog post outline, blog hero image, Sales FYI, and any press, event or paid push.
- **Market category:** SaaS backup and recovery for Jira Cloud, with actor-based rollback as the new capability inside it. "AI governance tooling" was considered and rejected because the sources support only an exportable audit log, not compliance claims.
- **Claims held back:** no statement that Atlassian native "has no actor-based rollback" (the PRD's claim has no source; copy says native works at the site level). No claims about other third-party tools. No "only", "first" or "unique" wording.
- **Attachment wording:** every asset uses the PRD wording ("up to 24 hours old") and never pairs Agent Rollback with the company-level "under 24 hours" claim.
- **Exceptions to check:** the one-pager visual is 42 words, over the 30-word cap, because it carries a limits box (approved exception, recorded in 07 and 08). The in-app message and banner leave out the Confluence roadmap line because it has no sign-off and the length cap is tight.

## Needs a human
Blockers (nothing dated, priced or plan-named can ship until these are answered):
- GA date: `[NEED PROOF: GA date]` (01, 02, 06, 07, 10)
- Plan names, pricing and which tier includes it: `[NEED PROOF: plan names and pricing]` (all customer-facing assets)
- Decide the attachment wording: PRD "up to 24 hours old" vs `context/` "under 24 hours" (02, 07, 09)
- Source or approval for "Atlassian native has no actor-based rollback" (02, 04)
- Competitor capability check on other third-party tools (01, 04, 09)
- Legal review of "exportable for auditors", and sign-off to mention the Confluence roadmap (05, 07, 08)
- Confirm the in-app and banner Confluence omission is acceptable (07)

Engineering unknowns (rep holding lines are in 09):
- How Actor view tells people, rules, integrations and AI agents apart
- Which Jira data types and fields can be rolled back
- How a rollback handles a person's later edit to the same item
- Limits on time window, size and speed; permissions needed; large-site support
- Audit log retention and export format
- How the attachment recovery point works in Agent Rollback (tag added in 09)

Evidence and measurement:
- Any customer name, quote or benchmark (none approved)
- Baselines and targets for the three proposed success metrics; whether the CRM can capture "AI governance cited as a buying reason"
- Segment sizes and validation of the demo personas against real research
- Brand palette, fonts and logo files for the visuals (placeholders used); CTA links and the in-product path to Actor view

Field feedback: `learnings/field-feedback.md` has no entries, so there was nothing for the Sales Enablement Lead to support or flag.

Advisory items from the second review (not fails):
- 08 still says the one-pager box short forms are "not word for word from 07". That is stale, since 07 now lists them.
- The box line "Attachments: backup up to 24 hours old." is terse. The full attachment wording must carry at fill time.
- The "Fill one-pager from 09" task in 10 says the box holds all four limits "in full". The layout splits them between the box and the footer, so reword the task.

## Files
- `01-launch-brief.md`: what is launching, business case, goals, timeline, stakeholders, open questions
- `02-launch-context.md`: capabilities in customer terms, four must-say limitations, availability, gaps, PRD vs context conflicts
- `03-audience.md`: personas, best-fit segments, buying group, out of focus
- `04-positioning.md`: Dunford positioning in order, category choice, trends, messaging handoff
- `05-messaging.md`: core message, three pillars, persona angles, must-say list, vocabulary
- `06-campaign-strategy.md`: tier score and decision, channels, assets in scope, timeline, metrics, risks
- `07-channel-copy.md`: customer email, in-app message, release note, LinkedIn post, on-image text
- `08-design-briefs.md`: a design brief for each of the four visuals
- `09-sales-enablement.md`: one-pager, talk track, discovery questions, objections, FAQ, competitive take
- `09b-enablement-session.md`: 30-minute rep session plan with role-plays
- `09c-readiness-quiz.md`: 8-question quiz with answer key (pass mark 7)
- `10-launch-checklist.csv`: 40 owned, dated tasks for monday.com or Jira
- `10-launch-checklist.md`: the same checklist, readable, with open questions mapped to tasks
- `11-review.md`: first-pass and second-pass review results
- `visuals/email-header.svg` and `.png`: email header (1200x400)
- `visuals/in-app-banner.svg` and `.png`: in-app banner (1280x320)
- `visuals/linkedin-image.svg` and `.png`: LinkedIn image (1200x627)
- `visuals/one-pager-layout.svg` and `.png`: sales one-pager layout (2550x3300), body cards left empty to fill from 09

## Lessons added this run
- 2026-10-16 | checklist CSV | Timing offsets (go/no-go, kit ready, quiz dates) drift from 06-campaign-strategy.md. Copy each offset from 06 word for word, then compare every dated row against it before finishing.
- 2026-10-16 | channel copy, design briefs | On-image text over the word cap forces design to cut it, and copy and visuals drift. Write on-image text within the cap in 07 (count the limits box), so design renders it unchanged.
- 2026-10-16 | sales objection answers | Do not explain how a feature works beyond what the PRD states (for example, how restored attachments relate to deletion time). Stop at the PRD wording and add a [NEED PROOF: ...] tag for the gap.
