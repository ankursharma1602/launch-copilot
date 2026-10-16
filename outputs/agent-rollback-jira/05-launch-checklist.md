# Launch checklist: Agent Rollback for Jira

> Based on a HYPOTHETICAL PRD. Tier 2. Same plan as `05-launch-checklist.csv`.

**Flag: GA date is unknown.** All dates are offsets from launch day (L). The first task is to confirm the GA date. Prepare tasks start at L-21, so if the date lands inside 21 days, compress Prepare and keep the order of dependencies.

**Tier 2 assets in scope:** customer email, in-app message, release note, LinkedIn post, sales one-pager, talk track and objections, sales FAQ. Not in scope: blog post outline, press or external announcement (Tier 1 only).

## Prepare (L-21 to L-8)
- [ ] L-21 | Product Manager | Confirm GA date
- [ ] L-21 | Head of Product Marketing | Confirm tier boundary (score 3.95 sits between Tier 1 and Tier 2 bands) and fix the rubric
- [ ] L-18 | Product Manager | Confirm recovery point wording ("under 24 hours" vs "up to 24 hours")
- [ ] L-14 | Product Manager | Confirm plan names and pricing tier (after GA date)
- [ ] L-14 | Product Marketing Manager | Run competitor capability check on other third-party backup tools
- [ ] L-14 | Engineering Lead | Confirm how Rewind attributes changes to an AI agent vs a person
- [ ] L-14 | Engineering Lead | Document what happens when a person edits a field after the agent and the admin rolls back the agent
- [ ] L-14 | Product Marketing Manager | Decide feature name vs headline
- [ ] L-12 | Customer Success Manager | Find a customer or design-partner example of an AI rollout approved with Agent Rollback in place
- [ ] L-12 | Product Analytics Lead | Set baseline and targets for the three success metrics
- [ ] L-10 | Sales Operations | Confirm Sales Ops can track AI governance as a buying reason (CRM field or reason code)
- [ ] L-10 | Lifecycle Marketing Manager | Draft customer email
- [ ] L-10 | Product Marketing Manager | Draft in-app message
- [ ] L-10 | Product Marketing Manager | Draft release note
- [ ] L-10 | Social Media Manager | Draft LinkedIn post
- [ ] L-10 | Product Marketing Manager | Draft sales one-pager
- [ ] L-10 | Product Marketing Manager | Draft talk track and objections
- [ ] L-10 | Product Marketing Manager | Draft sales FAQ
- [ ] L-8 | Brand Reviewer | Brand review of all drafts (first pass)

## Enable (L-7 to L-1)
- [ ] L-7 | Product Marketing Manager | Resolve or formally carry every remaining [NEED PROOF] placeholder in all assets
- [ ] L-6 | Product Marketing Manager | Confirm must-say limitations appear in every asset
- [ ] L-5 | Sales Enablement Manager | Run Sales enablement session (one-pager, talk track, FAQ)
- [ ] L-5 | Customer Success Manager | Brief Support and Customer Success on the feature and limitations
- [ ] L-4 | Lifecycle Marketing Manager | Build and QA customer email in the email tool
- [ ] L-4 | Product Manager | Configure and QA in-app message
- [ ] L-3 | Social Media Manager | Stage release note and schedule LinkedIn post
- [ ] L-3 | Brand Reviewer | Final brand review of finished assets
- [ ] L-2 | Head of Product Marketing | Go/no-go check

## Launch (L)
- [ ] L | Product Manager | Publish release note and turn on in-app message
- [ ] L | Lifecycle Marketing Manager | Send customer email
- [ ] L | Social Media Manager | Publish LinkedIn post
- [ ] L | Sales Enablement Manager | Announce launch to Sales and Support with links to assets
- [ ] L | Product Manager | Monitor launch day issues and questions

## Measure (L+1 to L+90)
- [ ] L+7 | Product Analytics Lead | First adoption read and Sales question log review
- [ ] L+14 | Product Marketing Manager | Update learnings/lessons.md with recurring review issues
- [ ] L+30 | Product Analytics Lead | Checkpoint: % of active Jira customers who open Actor view (leading metric)
- [ ] L+60 | Product Marketing Manager | Checkpoint: upgrades and AI governance pipeline
- [ ] L+90 | Head of Product Marketing | Final review of all three success metrics and launch retrospective

## Open questions mapped to tasks
| Open question or [NEED PROOF] | Task | Due |
|---|---|---|
| GA date | Confirm GA date | L-21 |
| Rubric gap (3.95) | Confirm tier boundary | L-21 |
| RPO wording | Confirm recovery point wording | L-18 |
| Plan names and pricing | Confirm plan names and pricing tier | L-14 |
| Competitor check | Run competitor capability check | L-14 |
| Actor attribution | Confirm attribution method | L-14 |
| Same-field conflicts | Document conflict behaviour | L-14 |
| Feature name vs headline | Decide feature name vs headline | L-14 |
| Customer example for AI rollout | Find customer or design-partner example | L-12 |
| Metric baselines and targets | Set baseline and targets | L-12 |
| Pipeline tracking | Confirm Sales Ops can track AI governance | L-10 |
