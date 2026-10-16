# Launch brief: Agent Rollback for Jira

> Based on a HYPOTHETICAL PRD (`inputs/rewind-agent-rollback-jira.md`) and demo context. Not a real Rewind product.

**Tier:** 2 (weighted score 3.95, no override) | **Launch date:** [NEED PROOF: GA date] | **Primary persona:** The Atlassian admin (Jira Cloud)

## In one sentence
Agent Rollback lets Jira Cloud admins find and undo every change one AI agent, automation rule or integration made, without restoring the whole site or losing work people did.

## The problem
An AI agent reclassifies 4,000 issues. Or an automation rule overwrites a custom field across 30 projects. The admin is the person everyone looks at, and they have two bad options: restore the whole site and lose every legitimate change since the backup, or fix it by hand. Native tools restore at the site level, not by who or what made the change.

(The 4,000 issues and 30 projects are example scenarios from the PRD, not customer data. Use them only as illustrations.)

## Who it's for
- **Primary:** The Atlassian admin, specifically Jira Cloud admins at companies using AI agents or heavy automation. They own automations and, more and more, the AI tools wired into Jira. They are the one who has to undo the damage, and they want "fast, surgical restores" (personas.md #1; input, Who it's for).
- **Secondary:** The IT or security leader. They must approve AI rollouts and want a recovery plan before they say yes. The audit log speaks to their need for "evidence for auditors" (personas.md #2; input, Who it's for).

The AI or automation owner (personas.md #3) is an influencer, not a target, for this launch. Assets can show that Agent Rollback lets them say yes to AI. Never frame them or their agents as the problem (voice.md).

## Today's alternative
1. **Full-site restore** with Atlassian's native Backup and Restore, or a site-level restore. This rolls back the bad changes but also wipes every legitimate change made since the backup.
2. **Fix it by hand.** Admins find and correct thousands of issues one by one, with no clean record of what the agent touched.
3. **Do nothing and hope.** This shows up as slower AI rollouts, because IT won't approve agents without a recovery plan.

## Positioning statement
For Jira Cloud admins who need to undo what an AI agent or automation got wrong, Agent Rollback is the Rewind recovery capability that rolls back every change by one actor, in any time window, while keeping the work people did. Unlike a full-site restore, it undoes the one actor's changes, not the whole site.

## Key messages
1. **Undo the agent, not the whole site.** See every change grouped by who or what made it, then roll back one actor's changes in a time window, or pick specific issues or fields. Proof: Actor view and Selective rollback (input, What it does #1 and #3). Rewind already restores a single ticket, page, file or configuration without a full-site restore (proof-points.md).
2. **Know exactly what will change before you click restore.** The blast radius preview shows which issues, fields and projects will change back and what will stay as is. Changes people made after the bad event are kept. Proof: Blast radius preview and Keep human work (input, What it does #2 and #4). [NEED PROOF: how conflicts are handled when a person edited the same field after the agent did]
3. **Give IT the recovery plan they need to approve AI.** Every rollback is logged with who ran it, what changed and when, and the log can be exported for auditors. Backups live outside Atlassian's platform. Proof: Audit log (input, What it does #5); backups stored independently of the vendor platform (proof-points.md). [NEED PROOF: customer or design-partner example of AI rollout approved with Agent Rollback in place]

Company-level proof that can support any asset: protects 16 cloud applications, trusted by more than 25,000 organizations (proof-points.md).

## Why now
The CEO named AI usage as one of Rewind's three growth drivers: "AI agents now act directly on SaaS data, which creates new rollback and recovery needs" (company.md, Aug 2026). Agent Rollback is the most direct answer to that driver. It also serves a second named driver, the Atlassian cloud migration, because it ships for Jira Cloud first. It fits the core idea in company.md: SaaS vendors protect their infrastructure, not you from your own automations or AI agents. Frame this as shared responsibility. Never imply Atlassian is unreliable (voice.md).

## Success metrics
- **Leading:** % of active Jira customers who open Actor view within 30 days of GA (input). Target: [NEED PROOF: baseline and target]
- **Lagging:** Upgrades to the plan that includes Agent Rollback within 90 days of GA (input). Target: [NEED PROOF: baseline and target]
- **Lagging (pipeline):** New opportunities where AI governance is cited as a buying reason, within 90 days (input). This requires a CRM field or reason code. [NEED PROOF: confirm sales ops can track this]

## Must-say limitations (for every asset)
- Only changes made after the customer's first Rewind backup can be rolled back. Don't imply it works retroactively.
- Attachments deleted by an agent come back from the most recent backup, which may be up to 24 hours old.
- Jira Cloud only. Confluence is on the roadmap with no committed date. Don't name Confluence as covered.

## Open questions
- **Rubric gap.** The score is 3.95. `context/tiering.md` defines Tier 1 as 4.0 and above and Tier 2 as 2.8 to 3.9, so 3.95 falls in neither band. I treated it as Tier 2. A human should confirm this and fix the rubric's boundary.
- **Recovery point wording (input vs context).** Context and proof points say "recovery points under 24 hours." The input says restored attachments "may be up to 24 hours old." These are close, but "under" and "up to" are not the same claim. Confirm the exact RPO wording before any asset uses either one.
- **Plan and pricing.** The plan names and pricing tier are `[NEED PROOF]` in the input. The IT or security leader is "turned off by unclear pricing" (personas.md #2), and the upgrade metric depends on this. Sales assets need it before GA.
- **GA date.** `[NEED PROOF: GA date]`. The checklist and in-app timing depend on it.
- **Competitor check.** `[NEED PROOF: competitor capability check]` for other third-party backup tools. Until it's done, no asset may claim "first" or "only." We can only make the comparison to Atlassian's native tool, and only as "site-level vs actor-level," not as a weakness.
- **Feature name vs headline.** "Agent Rollback" covers automation rules and integrations as well as AI agents. Per lessons.md, headlines should lead with what the admin gets back ("undo one agent's changes, keep your team's work"), not the feature name. Product should also confirm whether the name undersells the automation use case.
- **Actor attribution.** How does Rewind tell an AI agent from a person when an agent runs under a user account or a shared API token? This decides whether "keep human work" holds in practice. [NEED PROOF: product confirmation of attribution method]
- **Same-field conflicts.** What happens when a person edits a field after the agent changed it, and the admin then rolls back the agent? Needed for the FAQ and the talk track.
