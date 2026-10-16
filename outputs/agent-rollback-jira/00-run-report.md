# Launch CoPilot run report: Agent Rollback for Jira

**Tier:** Tier 2 (weighted score 3.95), no override
**Run time:** about 7 minutes (as measured by the orchestrator)
**Assets produced:** 11 | **Passed review first time:** 6 | **Revised:** 5 | **Needs a human:** 0 failing review (open proof items below)

## The launch in three lines
Agent Rollback lets Jira Cloud admins find and undo every change made by one AI agent, automation rule or integration, preview the blast radius first, and keep the work people did since.
It is for Jira Cloud admins running AI agents or heavy automation, and for the IT and security leaders who must approve those rollouts.
Why now: the CEO named AI agents acting on SaaS data as a growth driver in Aug 2026, and Jira Cloud first also serves the Atlassian migration driver.

## Decisions the system made
- **Tier 2 at 3.95.** Scores: reach 3, commercial 4, strategic fit 5, competitive 4, story 4. No override: none of the permitted reasons (competitive event, regulatory deadline, launch dependency) is documented.
- **Rubric gap.** `context/tiering.md` puts Tier 1 at "4.0 and above" and Tier 2 at "2.8 to 3.9", so 3.95 falls in neither band. The Strategy agent treated 4.0 as the floor. A human should confirm this and fix the boundary in the rubric.
- **Deliberately not produced (Tier 2):** blog post outline, external announcement.
- **No "first" or "only" claims anywhere.** The competitor capability check is unverified.
- **Recovery-point wording.** Context says "under 24 hours"; the input says attachments may come from a backup "up to 24 hours old". Assets use only the input's attachment wording and leave out "under 24 hours" until confirmed.
- **Three limitations stated in every asset:** rollback only covers changes after the first Rewind backup; deleted attachments may come from a backup up to 24 hours old; Jira Cloud only, no committed Confluence date.
- **Positioning worth a human's eye:** the AI or automation owner is framed as the person who gets to say yes to AI, never as the risk. One reviewer note: the in-app body says "may be 24 hours old" where the source says "up to 24 hours", with no room to change it.

## Needs a human
Review: nothing failed twice. All five revised assets passed the second pass. Advisory items from the second pass, not failures:
- One-pager "Do not say" line should read "Do not claim Rewind is the first or only tool", since its own limitation line uses the word "Only" (`04-sales-enablement.md`).
- Talk track runs about 183 words, long for 60 seconds. Trim one sentence or the final question (`04-sales-enablement.md`).

Open `[NEED PROOF]` items (deduplicated):
- **GA date**: `02-launch-brief.md`, `03-channel-copy.md`, `04-sales-enablement.md`
- **Plan names and pricing**: `03-channel-copy.md`, `04-sales-enablement.md`, `05-launch-checklist.csv`
- **Competitor capability check** (other third-party backup tools): `01-tier-decision.md`, `02-launch-brief.md`, `04-sales-enablement.md`
- **How an agent is told apart from a person** (including agents under a user account or shared API token): `02-launch-brief.md`, `03-channel-copy.md`, `04-sales-enablement.md`, `05-launch-checklist.csv`
- **Same-field conflict handling** when a person edits after the agent: `02-launch-brief.md`, `03-channel-copy.md`, `04-sales-enablement.md`, `05-launch-checklist.csv`
- **Customer or design-partner example** of an AI rollout approved with Agent Rollback in place: `02-launch-brief.md`, `03-channel-copy.md`, `04-sales-enablement.md`
- **Metric baselines and targets**: `02-launch-brief.md`, `05-launch-checklist.csv`
- **Sales Ops can track "AI governance" as a buying reason**: `02-launch-brief.md`
- **Exact UI navigation labels** for the release note getting-started steps: `03-channel-copy.md`
- **Restore time benchmarks**: none approved, so none used. The one-pager and FAQ tell reps not to quote any.

## Files
- `00-run-report.md`: this report
- `01-tier-decision.md`: five-criterion scoring and the Tier 2 decision
- `02-launch-brief.md`: problem, audience, positioning, messages, proof, goals, open questions
- `03-channel-copy.md`: customer email (two subject options), in-app message, release note, LinkedIn post
- `04-sales-enablement.md`: one-pager, talk track, discovery questions, objections, FAQ, competitive quick take
- `05-launch-checklist.csv`: 38 tasks, dated relative to launch day (L-offsets), ready for Jira or monday.com import. Validated: 7 columns on every row, all dependencies match a task name.
- `05-launch-checklist.md`: the same checklist, readable
- `06-review.md`: brand review, first pass and second pass

## Lessons added this run
- 2026-10-16 | sales talk track | Do not state customer patterns as fact ("rarely", "usually", "often") without proof. Describe the scenario ("can run to thousands of issues") or turn it into a question to the buyer.
- 2026-10-16 | checklist CSV | Quote every Task field that has commas or quotes, and make each Depends On entry match a Task name exactly. Keep Task names short and put detail in Definition of Done. Re-validate: same column count on every row.
- 2026-10-16 | in-app, LinkedIn, one-pager | Short assets drop the must-say limitations first. Write the limitations into the draft before any other copy, then cut other words to fit the length limit.

**Update, 2026-10-16:** The tiering gap in `context/tiering.md` has since been fixed (Tier 2 is now 2.8 up to, but not including, 4.0), and `07-design-briefs.md` was added (4 Tier 2 visual briefs, email header revised once, all passed review).
