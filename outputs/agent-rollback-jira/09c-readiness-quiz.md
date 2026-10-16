# Readiness quiz: Agent Rollback for Jira

**Due:** L-5 (from 06-campaign-strategy.md) | 8 questions. Pass mark: 7 of 8 (proposed). [NEED PROOF: quiz pass mark and target share of reps] Covers positioning, the top objections, and the limitations. Gaps feed `learnings/field-feedback.md`.

> Agent Rollback is a hypothetical product from a mock handoff. The quiz uses no closed beta numbers or quotes.

1. (positioning) In one breath, what does Agent Rollback let a Jira Cloud admin do, and what are the two bad options it replaces?
2. (positioning) Name the three kinds of actor in the lead message, and say why you should not lead with AI alone.
3. (positioning) What is the line about Atlassian's native Backup and Restore, and what must you never say about it?
4. (objection) A prospect says, "Atlassian already has native backup." What do you say?
5. (objection) An IT leader asks, "Who can run a rollback?" What do you say?
6. (objection) A prospect asks, "Can you undo every change the agent made?" What do you say?
7. (limitations) State the two limits on what can be restored, in the approved wording.
8. (limitations) A prospect asks about Confluence and about price. What is the only thing you can say on each?

## Answer key

1. It lets an admin undo what one rule, integration or AI agent changed in a time window, see the effect first, and leave people's work alone. The two bad options are restoring the whole site and losing the team's work since the backup, or fixing it by hand. | Source: 05-messaging.md, Core message and Angles by persona (admin)
2. Rule, integration and AI agent. AI is why the safety net matters, never the problem, and rules and integrations are actors too. Leading with AI alone misses admins whose problems come from rules. | Source: 05-messaging.md, Angles by persona; 04-positioning.md section 4
3. "Native works at the site level and Rewind sits on top of it. It does not replace it." Never say native lacks actor-based rollback or anything else, and never imply Atlassian is unreliable. No source exists for the lack claim. | Source: context/company.md; 05-messaging.md, Vocabulary (Avoid); 02-launch-context.md disagreement 2
4. "Yes, and Rewind sits on top of it. Native is built for full-site recovery. Agent Rollback is for undoing only what one actor changed." No claim that native lacks anything. | Source: 09-sales-enablement.md, Objection handling; context/company.md
5. "That is still being decided. I will come back to you." Do not guess a role or permission model. | Source: 05-messaging.md, Must say 7; 02-launch-context.md limitation 7
6. "Up to the limits." Only changes after your first Rewind backup. Issues and fields are confirmed. Other Jira data types are not confirmed. Do not say "every change" or "everything". | Source: 05-messaging.md, Must say 1 and 5; 02-launch-context.md limitations 1 and 4
7. Agent Rollback can undo changes made after your first Rewind backup. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Stop there, do not explain it and do not use "under 24 hours" or any recovery point claim. | Source: 05-messaging.md, Must say 1 and 2
8. Confluence: "Confluence is on the roadmap. No date is committed." No date, quarter or "coming soon". Price: "It is included in Rewind's Jira Cloud backup plans at a specific plan tier." No name, no price. | Source: 05-messaging.md, Must say 3 and 4
