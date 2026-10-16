# PRD: Agent Rollback for Jira

> HYPOTHETICAL. A mock release written to demo Launch CoPilot. Not a real or announced Rewind product.

## Summary
Agent Rollback lets Jira admins find and undo every change made by a specific AI agent, automation rule or integration, across any time window, without restoring the whole site or touching changes made by people.

## Problem
AI agents and automation rules now edit Jira issues at a scale no human does. When one goes wrong, for example an agent reclassifies 4,000 issues or an automation overwrites a custom field across 30 projects, admins today have two bad options: restore the whole site and lose every legitimate change since the backup, or fix things by hand. Native tools restore at the site level, not by actor.

## Who it's for
- Primary: Jira Cloud admins at companies using AI agents or heavy automation.
- Secondary: IT and security leaders who must approve AI rollouts and want a recovery plan before they say yes.

## What it does
1. **Actor view:** see every change grouped by who or what made it: a person, an automation rule, an integration or an AI agent.
2. **Blast radius preview:** before restoring, see exactly which issues, fields and projects will change back, and what will stay as is.
3. **Selective rollback:** undo all changes by one actor in a time window, or pick specific issues or fields.
4. **Keep human work:** changes made by people after the bad event are preserved.
5. **Audit log:** every rollback is recorded with who ran it, what changed and when, exportable for auditors.

## Availability
- Plans: included in Rewind's Jira Cloud backup plans at the [NEED PROOF: plan names and pricing] tier.
- Platforms: Jira Cloud first. Confluence on the roadmap, no date committed.
- Launch date: [NEED PROOF: GA date]

## Success metrics (proposed)
- Adoption: % of active Jira customers who open Actor view within 30 days
- Expansion: upgrades to the plan that includes Agent Rollback within 90 days
- Pipeline: new opportunities where AI governance is cited as a buying reason

## Competitive notes
- Atlassian's native Backup and Restore works at the site level and has no actor-based rollback.
- Other third-party backup tools: [NEED PROOF: competitor capability check]

## Known limitations
- Only changes made after the customer's first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
