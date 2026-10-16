# Sales enablement: Agent Rollback for Jira (Tier 2)

**Builds on:** 02-launch-context.md, 03-audience.md, 04-positioning.md, 05-messaging.md, 06-campaign-strategy.md | **Kit delivery:** L-10 | **GA date:** [NEED PROOF: GA date]

> Agent Rollback is a hypothetical product from a mock handoff. Closed beta numbers and quotes are mock, internal evidence from a small group. They are not customer proof. Do not say them on a call or write them in an email. Any external use is [NEED PROOF: approval to use closed beta results or quotes].

## One-pager

**Headline:** Undo what one rule, integration or AI agent changed. Leave people's work alone.

**The problem:** When one actor changes a lot of issues it should not have, the admin has two bad options. Restore the whole site and lose the team's work since the backup, or fix it by hand. An agent that reclassifies 4,000 issues, or a rule that overwrites a custom field across 30 projects, are examples of the scenario, not results.

**What it does:**
- Actor view groups changes by who or what made them: a person, an automation rule, an integration or an AI agent.
- Blast radius preview shows which issues, fields and projects will change back, and which will stay, before anything is restored.
- Selective rollback undoes one actor's changes in a time window, or only the issues or fields you pick. Separate edits people made after the bad event stay in place. Each rollback is recorded in an audit log that can be exported.

**Why Rewind:**
- Rewind sits on top of Atlassian's native Backup and Restore. Native is built for full-site recovery. Agent Rollback is for the one actor that went wrong. It does not replace native.
- Rewind protects 16 cloud applications and is trusted by more than 25,000 organizations, including companies in financial services, healthcare and manufacturing. This supports the company, not the feature.

**Who to call about it:**
- Existing Rewind Jira Cloud backup customers (the feature needs Rewind backup running).
- Jira Cloud sites with heavy automation: many rules, bulk changes or integrations across projects.
- Teams rolling out AI agents in Jira Cloud that need IT or security sign-off.
- Regulated teams (financial services, healthcare, manufacturing) where audit evidence matters.
- Champion: the Jira admin. Approver: the IT or security leader.

**Limits to state up front:**
1. Agent Rollback can undo changes made after your first Rewind backup.
2. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
3. It works on Jira Cloud. Confluence is on the roadmap. No date is committed. [NEED PROOF: Legal approval of any Confluence mention] Say this line only if asked.
4. It is included in Rewind's Jira Cloud backup plans at a specific plan tier. Rewind backup must be running on the site. [NEED PROOF: plan names and pricing]
5. The handoff confirms issues and fields. Other Jira data types are not confirmed. [NEED PROOF: confirmed list of rollback-able Jira data types]

**Do not say:**
- "Every change" or "undo everything" without the data type limit next to it.
- "Under 24 hours" or any recovery point claim next to Agent Rollback.
- That Atlassian's native tool lacks anything. Say it works at the site level and Rewind sits on top.
- "First", "only" or "no other tool". Nothing about other third-party tools. [NEED PROOF: competitor capability check]
- Who can run a rollback, how Actor view tells actor types apart, or how it behaves on very large sites.
- How it behaves when a person edited the same field the agent changed.
- Any time saved, restore time, ROI, plan, price or date. [NEED PROOF: any outcome measure]
- Any closed beta number or quote. [NEED PROOF: approval to use closed beta results or quotes]
- How a customer turns it on. [NEED PROOF: how a customer turns the feature on, and whether it needs setup]

## Talk track (under 150 words)

"You have two options when a rule, an integration or an AI agent changes the wrong issues. Restore the whole site and lose your team's work since the backup, or fix it by hand. Agent Rollback is a third option. Pick the actor that went wrong and a time window. Preview which issues, fields and projects will change back and which will stay. Then undo that actor's changes. Separate edits people made after the bad event stay in place. Each rollback is recorded in an audit log that can be exported. The limits: it works on Jira Cloud. It covers changes after your first Rewind backup. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. And it sits at a specific plan tier."

(About 134 words.)

## Discovery questions

Ask these before you pitch.
1. When a rule, integration or agent changes something it should not have, what do you do today? Restore the site, fix it by hand, or something else?
2. How many automation rules, integrations or AI agents can edit issues in your Jira Cloud site today?
3. Are you planning or piloting AI agents in Jira? Who has to approve that, and what do they ask you first?
4. If you had to show IT or security a recovery plan for one actor going wrong, what would you show them?
5. Is Rewind backup already running on that Jira Cloud site, and since when? (Rollback covers changes after the first Rewind backup.)

## Objection handling

| They say | You say | Proof |
|---|---|---|
| "Atlassian already has native backup and restore." | "Yes, and Rewind sits on top of it. It does not replace it. Native is built for full-site recovery. Agent Rollback is for the day one rule, integration or agent went wrong and you want to undo only that." Do not say native lacks anything. | `context/company.md` (positioning against native); 04 section 1 |
| "We can restore the whole site if something breaks." | "You can. The cost is the legitimate work people did since that backup. With Agent Rollback you pick the actor and a window, and separate edits people made after the bad event stay in place." | Handoff ROLL-103, ROLL-104 and demo notes |
| "We fix it by hand. It is fine." | "That works for a few issues. Ask how it goes when one actor touched thousands of issues or many projects. The preview shows exactly what would change back before you commit." | Handoff epic scale examples (illustrations, not results) |
| "Can I undo every change the agent made?" | "Up to the limits. Changes made after your first Rewind backup. Issues and fields are confirmed. Other Jira data types are not confirmed yet. I will check anything specific you need." | 02 limitations 1 and 4. [NEED PROOF: confirmed list of rollback-able Jira data types] |
| "We have had Jira for years. Can you roll back what happened last year?" | "No. Rollback covers changes made after your first Rewind backup." | 02 limitation 1 |
| "What if a deleted attachment is not the latest version?" | "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. That is the wording we have today." Stop there. | Handoff release notes. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase] |
| "Who is allowed to run a rollback?" | "That is still being decided. I will come back to you with the answer." Do not guess a role. | [NEED PROOF: who can run a rollback] |
| "What if a person edited the same field the agent changed?" | "The demo showed separate edits by people staying in place. The same-field case is not decided yet, so I will not guess. I will find out." | Handoff demo notes. [NEED PROOF: behavior when a person edited the same field the agent changed] |
| "Does it work on our very large site?" | "I do not have that answer for this feature. I will ask Sales Engineering." Do not reuse the backup claim about large sites. | [NEED PROOF: behavior on sites above Atlassian's size limits] |
| "Will the audit log satisfy our auditors?" | "Each rollback is recorded with who ran it, what changed and when, and the log can be exported. I will not tell you it meets a specific audit requirement." | Handoff ROLL-105. [NEED PROOF: Legal approval of "exportable for auditors"] [NEED PROOF: audit log contents and export format] |
| "Do you have customer results or references?" | "Not that I can share today. I can show you the preview and the audit log in a demo." | [NEED PROOF: approval to use closed beta results or quotes] |
| "Is this the only tool that does this?" | "I will not make that claim. What I can say is what Agent Rollback does and what it does not." | [NEED PROOF: competitor capability check] |
| "We will slow down AI agents until we have a recovery plan." (IT or security) | "That is a fair order. The preview shows what would change back before anything does. The audit log records each rollback. Those are the two things to look at for your plan. Here is what the limits are." | Handoff ROLL-102, ROLL-105; 05 Pillar 3 |

## FAQ

**Q:** What is it in one sentence?
**A:** It lets a Jira Cloud admin undo the changes of one rule, integration or AI agent in a time window, see the effect first, and leave people's work alone.

**Q:** Does it go back before we started with Rewind?
**A:** No. Agent Rollback can undo changes made after your first Rewind backup. Two closed beta accounts did not get this at first (mock, internal), so say it early.

**Q:** What happens to attachments an agent deleted?
**A:** Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. That is the handoff wording and we stop there. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]

**Q:** Does it work on Confluence?
**A:** Not in this build. Agent Rollback works on Jira Cloud. If asked: Confluence is on the roadmap. No date is committed. Do not add a date, a quarter or "coming soon". [NEED PROOF: Legal approval of any Confluence mention]

**Q:** Which plan includes it, and what does it cost?
**A:** It is included in Rewind's Jira Cloud backup plans at a specific plan tier. I do not have the plan name or price. [NEED PROOF: plan names and pricing]

**Q:** When is it available?
**A:** Closed beta is heading to GA. I do not have a date. [NEED PROOF: GA date]

**Q:** Can it undo "every change"?
**A:** Say no to that wording. The handoff confirms issues and fields, and only changes after your first Rewind backup. [NEED PROOF: confirmed list of rollback-able Jira data types]

**Q:** Are people's changes kept?
**A:** In the demo, edits a person made after the bad event, separate from the agent's changes, were still in place after the rollback. What happens when a person edited the same field the agent changed is not decided. [NEED PROOF: behavior when a person edited the same field the agent changed]

**Q:** Who can run a rollback?
**A:** Not settled. Do not state a role or permission model. [NEED PROOF: who can run a rollback]

**Q:** How does Actor view tell a person, a rule, an integration and an AI agent apart?
**A:** It is not documented yet. Do not explain how detection works. [NEED PROOF: how Actor view identifies person, rule, integration and AI agent]

**Q:** Does it work on sites above Atlassian's size limits?
**A:** Unknown for this feature. The backup claim about large sites does not carry over. [NEED PROOF: behavior on sites above Atlassian's size limits]

**Q:** What is in the audit log and what format is the export?
**A:** Each rollback is recorded with who ran it, what changed and when. Export is available. Contents beyond that and the export format are not confirmed. Use "can be exported", not "exportable for auditors", until Legal clears it. [NEED PROOF: audit log contents and export format] [NEED PROOF: Legal approval of "exportable for auditors"]

**Q:** How do I turn it on?
**A:** I do not have the steps or whether setup is needed. [NEED PROOF: how a customer turns the feature on, and whether it needs setup]

**Q:** Is it only for AI agents?
**A:** No. The actor can be an automation rule, an integration or an AI agent. In closed beta (mock, internal, small group) more rollbacks were on rules than on agents, so ask the admin which actor worries them. Do not repeat the numbers to customers.

**Q:** Can I quote beta results or customers?
**A:** No. They are internal and customers have not agreed. [NEED PROOF: approval to use closed beta results or quotes]

**Q:** Is it faster than what we do today?
**A:** There is no time saved or restore time figure. Do not say faster or in minutes. [NEED PROOF: any outcome measure]

## Competitive quick take

| Alternative | Where they stop | Where we go further |
|---|---|---|
| Atlassian native Backup and Restore | Works at the site level, built for full-site recovery (`context/company.md`). Rewind sits on top of it and does not replace it. | Agent Rollback undoes one actor's changes in a window, with a preview, and keeps separate edits by people in place. Do not say native lacks anything. |
| Restore the whole site | Brings back the data, and the team's legitimate work since that backup is lost. | Pick the actor and window. Separate edits people made after the bad event stay in place. |
| Fix it by hand | Slow when one actor touched many issues or projects. | The preview shows what changes back. Rollback does it for the actor you pick. |
| Do nothing | The wrong values stay in issues and fields. | Same as above. |
| Rewind single-item restore | Restores one ticket, page, file or configuration at a time. | Agent Rollback works by actor across many items. They are different capabilities, so do not use the single-ticket claim as proof for this. |
| Other third-party backup tools | Not checked. | No claim. [NEED PROOF: competitor capability check] |

## Field feedback applied

`learnings/field-feedback.md` has no entries. Nothing to apply. Nothing left open.

| Entry | What changed | Where |
|---|---|---|
| (none) | Not applicable | Not applicable |

## Needs a human (open questions reps will hit)

Plan names and pricing, GA date, attachment wording, who can run a rollback, same-field edits, large-site behavior, rollback-able data types, Actor view detection, audit log contents and export format, how to turn it on, Legal review of "exportable for auditors" and Confluence, source for native tool capability, competitor check, approval to use beta results or quotes.
