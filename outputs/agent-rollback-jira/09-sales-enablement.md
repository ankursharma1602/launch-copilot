# Sales enablement: Agent Rollback for Jira (Tier 2)

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. Built from `05-messaging.md`, `04-positioning.md` and `02-launch-context.md`. If it is not in those files, do not say it. GA date: [NEED PROOF: GA date]. Plan names and pricing: [NEED PROOF: plan names and pricing].

## One-pager

**Headline:** Undo one agent's changes, not the whole site.

**The problem:** An AI agent, automation rule or integration changes a lot of Jira issues the wrong way. Today the admin restores the whole site and loses legitimate changes made since the backup, or fixes it by hand. The PRD's illustrations: an agent reclassifies 4,000 issues, or an automation overwrites a custom field across 30 projects. These are illustrations of the problem, not customer data.

**What it does:**
- Shows every change in Jira grouped by who or what made it: a person, an automation rule, an integration or an AI agent. Pick a time window.
- Previews what will change back (issues, fields, projects) and what will stay, before anything is restored. Undo all of one actor's changes, or pick specific issues or fields.
- Keeps changes people made after the bad event. Each rollback is recorded (who ran it, what changed, when), and the record is exportable for auditors.

**Why Rewind:**
- Rewind sits on top of Atlassian's native Backup and Restore, which works at the site level. Native is the right tool for a full-site loss. Agent Rollback covers the actor-level need on top of it.
- Rewind protects 16 cloud applications for more than 25,000 organizations, including companies in financial services, healthcare and manufacturing. This is trust context, not proof that this feature works. Customer proof for this feature: [NEED PROOF: no customer name, quote or benchmark is approved].

**Who to call about it:**
- Jira Cloud admins with AI agents, heavy automation or integrations that write to issues or custom fields across projects.
- Existing Rewind Jira Cloud backup customers.
- IT or security leaders who must approve an AI rollout and want a recovery plan first.
- Segment sizes: [NEED PROOF: segment sizes].

**Limits to state up front (all four, every time):**
1. Only changes made after your first Rewind backup can be rolled back.
2. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
3. Jira Cloud only at launch. Confluence is on the roadmap, no date committed.
4. Included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. [NEED PROOF: plan names and pricing]

**Do not say:**
- "Only," "first" or "unique in the market." The competitor check is not done.
- That Atlassian's native tool has no actor-based rollback. Say it works at the site level.
- Anything about other third-party backup tools.
- Any recovery point claim from the company materials near Agent Rollback. Use the attachment wording above as written.
- Restore speeds, time saved, ROI, customer names or quotes. None is approved.
- "Audit-ready," "compliant" or any standard. Say "exportable for auditors" and stop.
- "Guaranteed," "complete," "everything" or "any change."
- A plan name, price or date.
- That Atlassian is unreliable, or that AI or automation owners are the problem.

## Talk track (under 150 words)

"Picture an automation rule that overwrites a custom field across 30 projects. Today you restore the whole site and lose everyone's legitimate work since the backup, or you fix it by hand. Agent Rollback gives you a third option. You see every change grouped by who or what made it, preview what will change back, and undo just that actor's changes. Changes your people made after stay in place. Each rollback is logged, and the log is exportable for auditors. Rewind sits on top of Atlassian's native Backup and Restore, which works at the site level. Straight limits: Jira Cloud only, Confluence on the roadmap with no date. Only changes after your first Rewind backup can be rolled back. Attachments an agent deleted come from the latest backup, which may be up to 24 hours old. It sits in a specific plan tier, not every plan."

(Word count: 147.)

## Discovery questions

Ask these before you name the feature.

1. Are AI agents, automation rules or integrations writing to your Jira issues today, or is that planned?
2. If one of them changed a few thousand issues the wrong way tomorrow, what would you do first? How long would that take?
3. Who has to approve a new agent or automation going into Jira, and what do they ask for before they say yes?
4. Do you have a Rewind Jira Cloud backup in place today, and since when? (This sets what can be rolled back.)

Follow-ups if there is time:
- Would you restore the whole site for something like that, or fix it by hand? What would you lose either way?
- Is anyone asking you for a record of what was changed and who changed it?

## Objection handling

| They say | You say | Proof |
|---|---|---|
| "Atlassian already has native backup and restore." | "It does, and Rewind sits on top of it. Native works at the site level and is the right tool for a full-site loss. Agent Rollback is for the case where one agent or rule did the damage and you want to undo just that." Do not say native lacks actor-based rollback. | `context/company.md`, positioning against native. `04-positioning.md`, section 1. |
| "We can just restore the whole site." | "You can. The cost is the legitimate changes your people made since the backup. Agent Rollback undoes one actor's changes and keeps theirs. What would a day of lost changes cost you?" | `04-positioning.md`, section 1 and section 2 (Keep human work). No cost figure is approved. |
| "We can fix it by hand." | "You can, and nothing legitimate gets lost. The question is scale. How many issues could one agent or rule touch in your setup?" | `04-positioning.md`, section 1. No time or error benchmark is approved. |
| "Can it roll back what the agent did last month?" | "Only changes made after your first Rewind backup can be rolled back. If your backup started after that change, we cannot undo it. Better to know now than on the bad day." | `05-messaging.md`, Must say 1. |
| "What about attachments an agent deleted?" | "Those are restored from the most recent backup, which may be up to 24 hours old." If they ask what happens to files created or changed since the last backup, say you will confirm. | `05-messaging.md`, Must say 2. Use the PRD wording as written. A human is still deciding the wording. [NEED PROOF: what is and is not recoverable for attachments created or changed since the last backup] [NEED PROOF: how the attachment recovery point works in Agent Rollback] |
| "Does it work on Confluence?" | "Jira Cloud only at launch. Confluence is on the roadmap, no date committed. I will not give you a date I do not have." | `05-messaging.md`, Must say 3. Roadmap mention needs sign-off: [NEED PROOF: sign-off to mention Confluence roadmap publicly]. |
| "Which plan is it in, and what does it cost?" | "It is included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. I will confirm the plan and price for you." | `05-messaging.md`, Must say 4. [NEED PROOF: plan names and pricing] |
| "Will it overwrite what my team changed afterward?" | "The design keeps changes people made after the bad event. The preview shows what will change back and what will stay before you restore. If a person edited the same field the agent changed, I will confirm how that is handled." | PRD facts. [NEED PROOF: how a rollback is handled when a person later edited the same issue or field] |
| "Is the audit log compliant with our audit standard?" | "Each rollback is recorded with who ran it, what changed and when, and the record is exportable for auditors. I cannot name a standard. I can get you the export details." | PRD fact only. [NEED PROOF: audit log retention, export format, any named standard] Legal review pending. |
| "Can it tell my AI agent apart from my automation rules?" | "Actor view groups changes by person, automation rule, integration or AI agent. I will check with engineering how each one is identified and whether rollback works for each." | [NEED PROOF: how Actor view tells the four actor types apart] |
| "How fast is a rollback? How many issues can it handle?" | "I do not have a speed or a limit I can stand behind. I will find out." | [NEED PROOF: rollback speed and limits on time window or number of issues] No benchmark is approved. |
| "Who in our company can run a rollback?" | "It is built for the Jira Cloud admin. I will confirm which permissions it needs." | [NEED PROOF: roles and permissions needed to run a rollback] |
| "Does it work on our large site?" | "Rewind covers Jira and Confluence sites above Atlassian's native size limits. I will confirm that Agent Rollback does too." | `context/proof-points.md` for backup coverage. [NEED PROOF: Agent Rollback on large sites] |
| "Do you have a customer who used it?" | "Not one I can name today. I can walk you through the preview and the audit log instead." | [NEED PROOF: no customer name, quote or benchmark is approved] |
| "We are not running AI agents yet." | "Fair. It also covers automation rules and integrations. And if IT will ask for a recovery plan before approving agents, this is one you can show them. Who approves that on your side?" | `05-messaging.md`, pillar 3. |

## FAQ

**Q:** What is Agent Rollback?
**A:** It lets a Jira Cloud admin find and undo every change made by one actor: a person, an automation rule, an integration or an AI agent. You pick a time window, preview what will change back, and restore only that actor's changes. Changes people made after the bad event stay in place.

**Q:** What can it roll back?
**A:** Issues and fields are what the sources name. Comments, workflows, permissions and other objects are not confirmed. [NEED PROOF: which Jira data types and fields can be rolled back] Do not imply more.

**Q:** How far back can it go?
**A:** Only changes made after your first Rewind backup can be rolled back. (Limitation 1.)

**Q:** What happens with attachments?
**A:** Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. (Limitation 2.) [NEED PROOF: what is and is not recoverable for attachments created or changed since the last backup]

**Q:** Does it cover Confluence or other platforms?
**A:** Jira Cloud only at launch. Confluence is on the roadmap, no date committed. (Limitation 3.) Do not turn that into a timeframe.

**Q:** Which plans include it?
**A:** It is included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. The tier name and price are not set. [NEED PROOF: plan names and pricing] (Limitation 4.)

**Q:** When is it available?
**A:** [NEED PROOF: GA date] Do not give a date until product supplies one.

**Q:** Does it replace Atlassian's native Backup and Restore?
**A:** No. Rewind sits on top of it. Native works at the site level and is the right tool for a full-site recovery. Recovering your own data is a shared responsibility.

**Q:** Does it need a Rewind Jira Cloud backup?
**A:** Yes. A Rewind Jira Cloud backup must be in place, and the customer must be on the plan tier that includes Agent Rollback.

**Q:** What happens if a person edited the same issue the agent changed?
**A:** Not confirmed. The design keeps human work made after the bad event. How a conflict on the same issue or field is handled is open. [NEED PROOF: conflict handling] Do not promise a clean result.

**Q:** Can I see what will happen before I restore?
**A:** Yes. The blast radius preview shows which issues, fields and projects will change back and what will stay as is. Preview accuracy and size limits are open. [NEED PROOF: preview accuracy and limits]

**Q:** What does the audit log give me?
**A:** A record of each rollback: who ran it, what changed, when. It is exportable for auditors. Retention, export format and any named standard are open, and legal review is pending. Make no compliance claim.

**Q:** Can it tell an AI agent from an automation rule?
**A:** Actor view groups changes by person, automation rule, integration or AI agent. How each is identified, and whether rollback works for each, is open. [NEED PROOF: actor type detection] Use "AI agent, automation rule or integration" as examples only.

**Q:** Is there a limit on time window, number of issues or speed?
**A:** The PRD says any time window. No size limit or speed is stated and no benchmark is approved. [NEED PROOF: limits and rollback speed]

**Q:** Who can run a rollback?
**A:** The Jira Cloud admin is the primary user. The exact role or permission is not stated. [NEED PROOF: roles and permissions]

**Q:** Does it work on large sites?
**A:** Rewind backup covers sites above Atlassian's native size limits. Whether Agent Rollback does is not stated. [NEED PROOF: Agent Rollback on large sites]

**Q:** Is it the only tool that does this?
**A:** Do not say so. No competitor check has been done. [NEED PROOF: competitor capability check]

**Q:** Can I quote a customer or a result?
**A:** No. None is approved. [NEED PROOF: customer name, quote or benchmark]

## Competitive quick take

Claims here come from `04-positioning.md` and `context/company.md` only.

| Alternative | Where they stop | Where we go further |
|---|---|---|
| Atlassian native Backup and Restore | Built for full-site recovery. It works at the site level and is the right tool for a full-site loss. Used for an agent mistake, a site restore also takes back legitimate changes made since the backup. This is a fit question, not a reliability one. | Rewind sits on top of native and does not replace it. Agent Rollback undoes one actor's changes in a time window and keeps changes people made afterward. Rewind also restores a single ticket, page, file or configuration without a full-site restore. |
| Fix it by hand | Nothing legitimate is lost, but it is slow when an agent or rule has touched thousands of issues or many projects. No time or error benchmark is approved. | Find all of one actor's changes in one place, preview, and restore. Speed: [NEED PROOF: rollback speed]. |
| Do nothing | Fine until the first large bad change. Approvers who sign off on AI rollouts may ask for a recovery plan first. | A preview-then-restore plan and an audit log exportable for auditors that the admin can show an approver. |
| Rewind single-item restore | Restores a chosen ticket, page, file or configuration. The sources do not say it finds and undoes all changes by one actor. | Agent Rollback is the new actor-level capability. It is not an existing proof point. |
| Other third-party backup tools | [NEED PROOF: competitor capability check] | [NEED PROOF: competitor capability check] Say nothing about them. If asked: "I will not speak for other tools. Here is what Agent Rollback does." |

## Field feedback applied

`learnings/field-feedback.md` was read. It has no entries yet ("none yet"), so there is nothing to mark addressed and nothing left open.

| Entry | What changed | Where |
|---|---|---|
| None | No change. Objections come from persona fears, the four limitations and the open gaps in `02-launch-context.md`. | n/a |
