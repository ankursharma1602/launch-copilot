# Channel copy: Agent Rollback for Jira (Tier 2)

> Based on a HYPOTHETICAL PRD. Not a real Rewind product.

**Produced for this tier:** Customer email, in-app message, release note, LinkedIn post
**Deliberately skipped:** Blog post outline (Tier 1 only). Sales one-pager, talk track, sales FAQ and checklist belong to other agents.

## Customer email
**Subject A:** Undo one agent's changes in Jira
**Subject B:** Roll back the agent, keep your team's work
**Preview:** Find every change one agent or rule made, and undo only those.

An agent reclassifies thousands of issues. An automation rule overwrites a field across projects. You can restore the whole site and lose your team's work, or fix it by hand.

Agent Rollback gives you a third way. Actor view groups every change by who or what made it. Pick one agent, rule or integration and a time window. The blast radius preview shows what will change back and what stays. Changes people made after the bad event are kept. Every rollback is logged and exportable for auditors.

Good to know: only changes made after your first Rewind backup can be rolled back. Attachments deleted by an agent come back from the latest backup, which may be up to 24 hours old. Jira Cloud only for now.

**CTA:** See how Agent Rollback works

## In-app message
**Headline:** Undo one agent, keep human work
**Body:** Roll back one agent's changes, keep human work. Only changes after your first backup. Deleted attachments may be 24 hours old. Jira Cloud only.
**Button:** See Actor view

## Release note
**Title:** Undo one agent's changes in Jira Cloud, without a full-site restore

**Summary:** Agent Rollback lets Jira Cloud admins find and undo every change made by one AI agent, automation rule or integration, in any time window. People's work stays in place. You see what will change before you restore.

**What's new**
- **Actor view:** see every change grouped by who or what made it: a person, an automation rule, an integration or an AI agent.
- **Blast radius preview:** before restoring, see which issues, fields and projects will change back and what will stay as is.
- **Selective rollback:** undo all changes by one actor in a time window, or pick specific issues or fields.
- **Keep human work:** changes made by people after the bad event are preserved.
- **Audit log:** every rollback records who ran it, what changed and when. Export it for auditors.

**How to get started**
1. Open your Jira Cloud site in Rewind.
2. Open Actor view and choose the agent, rule or integration.
3. Set a time window, or select specific issues or fields.
4. Review the blast radius preview.
5. Run the rollback. Find the record in the audit log.

[NEED PROOF: exact navigation labels and UI path for the steps above]

**Limitations**
- Only changes made after your first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- Jira Cloud only. Confluence is on the roadmap, with no date committed.

**Availability:** Included in Rewind's Jira Cloud backup plans at the [NEED PROOF: plan names and pricing] tier. Generally available [NEED PROOF: GA date].

## LinkedIn post
An AI agent reclassifies thousands of Jira issues. Now what?

Restore the whole site and lose every good change since the backup, or fix it by hand.

Agent Rollback for Jira Cloud is a third option. See changes grouped by agent, rule or integration. Preview what will change back. Undo one actor's changes and keep the work people did.

Atlassian protects the platform. Rewind helps you recover from your own automations and agents. Backups live outside Atlassian, and every rollback is logged for auditors.

Only changes after your first Rewind backup can be rolled back. Attachments an agent deleted come back from the latest backup, which may be up to 24 hours old. Jira Cloud only.

#Jira #Atlassian

## Notes for reviewer
- Same-field conflicts (person edits after agent, then rollback) are unresolved. Copy says only "changes people made after the bad event are preserved," per the input. [NEED PROOF: how conflicts are handled when a person edited the same field after the agent did]
- Actor attribution for agents running under user accounts or shared tokens is unconfirmed. [NEED PROOF: product confirmation of attribution method]
- No "first" or "only" claims used. Competitor check is pending.
- No customer example of an AI rollout approved with Agent Rollback. [NEED PROOF: customer or design-partner example]
- The "up to 24 hours" wording is used only for attachments, as in the input. The recovery point wording ("under 24 hours") is not used pending confirmation.
- Company-level proof (16 apps, 25,000+ organizations) was left out for length. It can be added to the LinkedIn post if wanted.
