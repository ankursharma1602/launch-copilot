# Sales enablement: Agent Rollback for Jira (Tier 2)

> Based on a HYPOTHETICAL PRD. Not a real Rewind product. GA date, plan names and pricing are not confirmed. Do not quote them.

## One-pager

**Headline:** Undo one agent's changes. Keep your team's work.

**The problem:** An AI agent reclassifies thousands of issues, or an automation rule overwrites a custom field across dozens of projects. The admin has two bad options: restore the whole site and lose every good change since the backup, or fix it by hand. (Scenarios are illustrations, not customer data.)

**What it does:**
- **Actor view and selective rollback:** see every change grouped by who or what made it (person, automation rule, integration or AI agent). Undo all of one actor's changes in a time window, or pick specific issues or fields.
- **Blast radius preview:** before you restore, see which issues, fields and projects will change back and what will stay as is.
- **Keep human work and audit log:** changes people made after the bad event are preserved. Every rollback is logged with who ran it, what changed and when, and can be exported for auditors.

**Why Rewind:**
- Rewind already restores a single ticket, page, file or configuration without a full-site restore. Agent Rollback extends that to "everything one actor did."
- Backups are stored independently of the vendor platform. Rewind protects 16 cloud applications for more than 25,000 organizations.

**Who to call about it:** Jira Cloud admins at companies using AI agents or heavy automation. Also IT and security leads who have to approve AI rollouts and want a recovery plan first. Good triggers: an AI agent pilot going live in Jira, a recent bulk-change or automation mishap, an IT review blocking an agent rollout.

**Limits to state up front:** (1) Covers changes only after the customer's first Rewind backup. (2) Attachments an agent deleted come back from the most recent backup, which may be up to 24 hours old. (3) Jira Cloud only. Confluence has no committed date.

**Do not say:** "first," "only," or that it works on Confluence. Do not quote price, plan or GA date.

## Talk track (60 seconds)

"When an AI agent or an automation rule gets something wrong in Jira, the damage can run to thousands of issues. Today your choices are to restore the whole site and lose everything your team did since the backup, or fix it by hand.

Agent Rollback gives you a third option. You pick the agent, rule or integration, and the time window. You see every change it made. Before you restore, a preview shows you which issues, fields and projects will change back and what will stay. Then you undo that one actor's changes. What your people did after the bad event is kept.

Every rollback is logged, with who ran it and what changed, and you can export it for auditors. Is that something your IT team often asks to see before approving more agents?

It covers changes made after your first Rewind backup, and it's Jira Cloud today. Attachments an agent deleted come back from the most recent backup, which can be up to 24 hours old. Can I ask how you handle it now when an automation goes wrong?"

## Discovery questions
1. Which AI agents, automation rules or integrations can edit issues in your Jira today? Who owns them?
2. Last time one of them made a wrong bulk change, how did you fix it? How long did it take, and how did you know you got everything?
3. Does IT or security need a recovery plan before approving a new agent? What would they want to see?
4. If you restored the whole site tomorrow, what would your team lose?

## Objection handling
| They say | You say | Proof |
|---|---|---|
| "Atlassian already has Backup and Restore." | "Keep it. We sit on top of it, not in place of it. Atlassian's tool works at the site level. Agent Rollback works at the actor level, so you undo one agent's changes without restoring the site." | company.md (Rewind sits on top of the native tool); input (native tool restores at site level, no actor-based rollback) |
| "We'll just restore the site." | "That also removes every good change since the backup. Preview first: you see what changes back and what stays." | Input: Blast radius preview, Keep human work |
| "Will it touch my team's edits?" | "Changes people made after the bad event are kept. The preview shows what will and won't change. If someone edited the same field the agent changed, I'll confirm how that is handled and get back to you." | Input: Keep human work. [NEED PROOF: how same-field conflicts are handled] |
| "How do you know it was the agent and not a person?" | "Actor view groups changes by person, automation rule, integration or AI agent. I'll confirm how it attributes changes when an agent runs under a user account or shared token." | Input: Actor view. [NEED PROOF: product confirmation of attribution method] |
| "Our auditors need evidence." | "Every rollback is logged with who ran it, what changed and when. The log exports for auditors." | Input: Audit log |
| "This sounds like it blames our AI team." | "No. Any fast system can make mistakes at scale, so the question is how you recover. A safety net is what lets you roll agents out with IT's approval." | personas.md #3 |
| "Can it undo what happened last month, before we signed up?" | "No. Only changes made after your first Rewind backup can be rolled back." | Input: Known limitations |
| "What does it cost? Which plan?" | "It's part of Rewind's Jira Cloud backup plans. I'll get you exact plan and pricing." Do not guess. | [NEED PROOF: plan names and pricing] |
| "Do other backup tools do this?" | "I can speak to Atlassian's native tool, which works at site level. I haven't verified other vendors, so I won't compare." | Input: competitor check not done |

## FAQ

**Q: What does Agent Rollback do?**
A: It finds and undoes every change made by one AI agent, automation rule or integration, in any time window, without restoring the whole site or touching changes made by people.

**Q: Can I roll back things that happened before we started using Rewind?**
A: No. Only changes made after the customer's first Rewind backup can be rolled back.

**Q: If an agent deleted attachments, do they come back current?**
A: They come back from the most recent backup, which may be up to 24 hours old. Attachments added in that gap may not be there. Say this before the customer finds it.

**Q: Does it work for Confluence?**
A: Not today. It is Jira Cloud first. Confluence is on the roadmap with no committed date. Do not promise one.

**Q: Can I undo only some changes?**
A: Yes. Undo all of one actor's changes in a time window, or pick specific issues or fields.

**Q: Can I see what will change before I restore?**
A: Yes. The blast radius preview lists which issues, fields and projects will change back, and what will stay as is.

**Q: Is there a record of rollbacks?**
A: Yes. Each rollback is logged with who ran it, what changed and when. The log is exportable.

**Q: What if a person edited a field after the agent changed it?**
A: Human changes after the bad event are preserved. For the same-field case, [NEED PROOF: how conflicts are handled]. Tell the customer you will confirm.

**Q: How does Rewind tell an agent from a person?**
A: [NEED PROOF: product confirmation of attribution method, including agents running under a user account or shared API token]. Do not guess on a call.

**Q: Which plan includes it, and what does it cost?**
A: It is included in Rewind's Jira Cloud backup plans at a tier that is [NEED PROOF: plan names and pricing].

**Q: When is it available?**
A: [NEED PROOF: GA date]. Do not give a date.

**Q: Do customers use it today?**
A: [NEED PROOF: customer or design-partner example]. No names, logos or quotes are approved.

**Q: How fast is a rollback?**
A: No restore time benchmarks are approved. Do not quote one.

## Competitive quick take
| Alternative | Where they stop | Where we go further |
|---|---|---|
| Atlassian native Backup and Restore | Works at the site level. No actor-based rollback. It is built for full-site recovery, and we sit on top of it. | Undo one actor's changes and keep everyone else's. Preview before restore. Also restores a single ticket, page, file or configuration. |
| Fixing it by hand | Slow, and no clean record of what the agent touched. | Actor view shows everything the actor changed. Audit log records the rollback. |
| Other third-party backup tools | [NEED PROOF: competitor capability check] | Do not compare until the check is done. |
