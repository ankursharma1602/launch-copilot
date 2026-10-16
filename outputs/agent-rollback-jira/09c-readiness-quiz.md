# Readiness quiz: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product.

8 questions. Pass mark: 7 of 8. Covers positioning, the top objections, and the limitations. All four Must say limits are tested: first backup, attachments, platform, plan.

1. A Jira admin says an automation rule just changed a custom field across many projects. What are the two options they have today, and what is the cost of each? (positioning)
2. Name the four things Agent Rollback lets an admin do, in the order they happen. (positioning)
3. Rewind and Atlassian's native Backup and Restore: how do you describe the relationship, and what do you never say about native? (positioning)
4. A buyer says, "Atlassian already has native backup and restore." What do you say? (objection)
5. An IT leader asks, "Is the audit log compliant with our audit standard?" What do you say, and what do you avoid? (objection)
6. A buyer asks, "Which plan is it in and what does it cost?" What do you say? (objection)
7. A buyer asks, "Can it roll back what the agent did last month?" What is the limit, and how do you state it? Also: what do you say about attachments an agent deleted? (limitations)
8. A buyer asks about platform coverage and then asks whether it is in every plan. What do you say on each? (limitations)

## Answer key

1. Restore the whole site, which also takes back legitimate changes made since the backup. Or fix it by hand, which is slow when an agent or rule has touched thousands of issues or many projects. No time or error benchmark is approved, so do not quote one. Agent Rollback is the third option: undo the one actor, not the whole site. | Source: `04-positioning.md`, section 1; `05-messaging.md`, core message.
2. See every change grouped by who or what made it (person, automation rule, integration or AI agent) and pick a time window. Preview which issues, fields and projects change back and what stays. Restore only that actor's changes, or pick specific issues or fields. Keep changes people made afterward. Full marks also mention that each rollback is recorded and the record is exportable for auditors. | Source: `02-launch-context.md`, Capabilities; `05-messaging.md`, pillars 1 to 3.
3. Rewind sits on top of native. It does not replace it. Native works at the site level and is the right tool for a full-site loss. Recovering your own data is a shared responsibility. Never say native lacks actor-based rollback, never imply Atlassian is unreliable, and never say anything about other third-party tools. | Source: `05-messaging.md`, supporting message and Vocabulary; `04-positioning.md`, section 1.
4. "It does, and Rewind sits on top of it. Native works at the site level. Agent Rollback is for when one agent or rule did the damage and you want to undo just that, and keep your people's work." | Source: `09-sales-enablement.md`, Objection handling; `context/company.md`.
5. Say each rollback is recorded with who ran it, what changed and when, and the record is exportable for auditors. Offer to get export details. Avoid naming any standard and avoid "audit-ready" or "compliant." Retention, export format and standards are not confirmed, and legal review is pending. | Source: `05-messaging.md`, pillar 3 and Vocabulary; `02-launch-context.md`, Gaps.
6. It is included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. Plan names and pricing are not set, so you will confirm. Do not name a plan or a price. | Source: `05-messaging.md`, Must say 4; `02-launch-context.md`, Availability.
7. Only changes made after your first Rewind backup can be rolled back, so state it up front and say that older changes cannot be undone. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Use that wording as written. | Source: `05-messaging.md`, Must say 1 and 2.
8. Jira Cloud only at launch. Confluence is on the roadmap, no date committed, and do not give a timeframe. On plans: included at a specific tier, not every plan has it, and the tier and price are still to be confirmed. | Source: `05-messaging.md`, Must say 3 and 4.

## Scoring notes for the trainer

- Question 3, 5, 7 and 8 answers lose the point if the rep claims native lacks actor-based rollback, names a standard, pairs Agent Rollback with any recovery point claim from the company materials, or gives a date or plan name.
- Any rep who scores below 7 repeats the limits block of the session and retakes the quiz.
