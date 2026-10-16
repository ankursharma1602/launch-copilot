# Launch CoPilot run report: Agent Rollback for Jira

**Tier:** 2 (weighted score 3.95), no override. It sits 0.05 below the Tier 1 line.
**Run time:** about 14 minutes (this run only, after the brand setup)
**Assets produced:** 16 | **Passed review first time:** 13 | **Revised:** 3 | **Needs a human:** 0 failed twice, but open items below block launch

The 16 assets: files 01 to 09c (11), the launch checklist (1), and four visuals. The three first-pass failures were 09, 09b and 09c, each a small wording fix. All passed the second review.

## The launch in three lines
Agent Rollback lets a Jira Cloud admin find and undo every change made by one rule, integration or AI agent, without restoring the whole site or touching people's work.
It is for Jira admins first, and for the IT or security leaders who approve AI rollouts and want a recovery plan.
It matters now because rules and agents edit Jira at a scale no person does, and the feature is heading from closed beta to GA.

Input is a hypothetical closed beta handoff. The beta stats and customer feedback are mock, not from real customers.

## Decisions the system made
- **Tier 2, score 3.95.** Reach 3, commercial impact 4, strategic fit 5, competitive weight 3, story value 5. Reach is the swing score: one more point gives 4.20 and Tier 1. It scored 3 because the eligible base is unknown (Jira Cloud only, needs Rewind backup, plan tier unnamed). The earlier run, from a thinner PRD, scored 3.55.
- **Not produced on purpose:** blog post outline, blog hero image, Sales FYI, and any press, event or paid push.
- **Market category:** backup and recovery for Jira Cloud, specifically selective recovery by actor. "AI agent governance" and "Jira change management" were rejected because the sources do not support them.
- **Beta feedback shaped the story, not the proof.** In the mock beta, more rollbacks were on automation rules (12 of 23) than on AI agents (8 of 23), and an admin said most bad changes come from rules. So the messaging says "one rule, integration or AI agent", and treats agents as the growing case, not the only one. This is a small mock sample. No beta number or quote appears in any customer-facing asset.
- **Visuals follow the new rules.** The email header, in-app banner and LinkedIn image carry no limitations or caveats; those sit in the email, in-app message and post beside them. Only the one-pager layout carries one small limits line. Every visual uses `context/brand.md` colours, Cabin, and the word "Rewind" set as live text. No logo file or Boomerang mark is used.
- **Claims held back:** no statement that Atlassian native "has no actor-based rollback" (unsourced; copy says native works at the site level). No claims about other third-party tools. No "only", "first" or "unique" wording.
- **Attachment wording:** every asset uses the handoff wording and never pairs Agent Rollback with "under 24 hours".

## Needs a human
Blockers. The go/no-go at L-3 needs these (see 06 and 10):
- GA date: `[NEED PROOF: GA date]` (01, 02, 06, 07, 10)
- Plan names and pricing: `[NEED PROOF: plan names and pricing]` (all customer-facing assets, which say "a specific plan tier")
- **Brand palette and typeface are unconfirmed.** `context/brand.md` uses a third-party listing (Blue Zodiac `#16225C`, Link Water `#F5F8FD`, Ebony `#0E102B`, Cabin). rewind.com blocked scripted readers and its brand page needs a login. No visual should leave the team until Rewind's brand team confirms them: `[NEED PROOF: confirm brand palette and typeface with Rewind's brand team]` (context/brand.md, 08, visuals/)
- Decide the attachment wording: handoff "up to 24 hours old" vs `context/` "under 24 hours" (01, 02, 05, 07, 09)
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
- Boomerang yellow hex, if the brand team wants it used

Advisory items from review (not fails):
- 07 Subject A is 39 characters (stated as 38); the LinkedIn post is about 101 words (stated as 112). Both are within spec.
- 08 says the one-pager is "about 29" words; it is 28.
- The 07 in-app body shortens the attachment wording to fit 24 words. Go/no-go gate 4 must confirm the short form, or the copy needs trimming to carry the full wording.
- The 09 FAQ says "Two closed beta accounts did not get this at first" (mock). The reviewer suggests deleting that clause, since it is a beta number. Not changed in this run.
- The SVGs load Cabin from Google Fonts, so they need internet to show Cabin when opened elsewhere. The PNGs are fixed.
- `learnings/field-feedback.md` has no entries, so the Sales Enablement Lead had nothing to support or flag.

## Files
- `01-launch-brief.md`: what is launching, business case, goals, timeline, stakeholders, open questions
- `02-launch-context.md`: what's built, what closed beta customers said (kept separate), limitations, gaps, conflicts with context/
- `03-audience.md`: personas tested against closed beta feedback, segments, buying group, out of focus
- `04-positioning.md`: positioning in order, starting from what beta customers compared it to; category choice
- `05-messaging.md`: core message, three pillars, persona angles, must-say list, vocabulary
- `06-campaign-strategy.md`: tier score and decision, channels, assets in scope, one timeline, go/no-go gates, metrics
- `07-channel-copy.md`: customer email, in-app message, release note, LinkedIn post, on-image text
- `08-design-briefs.md`: a design brief for each of the four visuals
- `09-sales-enablement.md`: one-pager, talk track, discovery questions, objections, FAQ, competitive take
- `09b-enablement-session.md`: 30-minute rep session plan with role-plays
- `09c-readiness-quiz.md`: 8-question quiz with answer key (pass mark proposed)
- `10-launch-checklist.csv`: 40 owned, dated tasks for monday.com or Jira
- `10-launch-checklist.md`: the same checklist, readable, with go/no-go gates mapped to tasks
- `11-review.md`: first-pass and second-pass review results
- `visuals/email-header.svg` and `.png`: email header (1200x400)
- `visuals/in-app-banner.svg` and `.png`: in-app banner (1280x320)
- `visuals/linkedin-image.svg` and `.png`: LinkedIn image (1200x627)
- `visuals/one-pager-layout.svg` and `.png`: sales one-pager layout (2550x3300), body blocks empty to fill from 09

## Lessons added this run
- 2026-10-16 | sales talk track, session plan | A shortened limitation loses words like "by an agent" or "restored" and broadens the limit. Copy the Must say wording from 05-messaging.md exactly, and cut other words instead.
- 2026-10-16 | all assets | Hand-counted character and word counts come out off by one or more. Recount with a tool, or write "about N". Never state an exact count you did not verify.
- 2026-10-16 | quiz, checklist | A proposed value (such as the quiz pass mark) is written as fact while 06 and 10 treat it as open. Label it "proposed, to confirm" or add a [NEED PROOF: ...] tag until a source sets it.
