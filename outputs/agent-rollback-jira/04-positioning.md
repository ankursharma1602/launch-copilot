# Positioning: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. Personas and company context are demo material. Validate before real use.

This is built in order from the evidence. Each part feeds the next. There is no positioning statement. The six parts are the positioning.

## 1. Competitive alternatives

The question: if Agent Rollback did not exist, what would a Jira Cloud admin whose agent or automation just made wrong changes do?

| Alternative | Why customers pick it | Where it stops | Source |
|---|---|---|---|
| Do nothing | Nothing bad has happened yet. The agents and rules work. Rolling out AI is the priority, and recovery is a problem for later. | The first time an agent or rule makes bad changes at scale, there is no plan. IT and security leaders who must approve AI rollouts want a recovery plan before they say yes, so "nothing" can also stall the rollout. | PRD, Problem and Who it's for. `03-audience.md`, trigger moments. |
| Fix it by hand | It needs no new tool and no restore. The admin controls each change and nothing legitimate is lost. | It is slow when an agent has changed thousands of issues or a rule has overwritten a field across many projects. The PRD's examples are 4,000 issues and 30 projects. These are illustrations of the problem, not customer data. Speed and error rates by hand: [NEED PROOF: no time or error benchmark is approved]. | PRD, Problem. |
| Restore the whole site (Atlassian's native Backup and Restore) | It is built for full-site recovery. It is the tool Atlassian provides, and Rewind sits on top of it and does not replace it. It is the right tool for a full-site loss. | It works at the site level. Used for an agent mistake, it takes back every legitimate change made since the backup, along with the bad ones. This is a fit question, not a reliability question. Native does what it was built to do. Recovery of your own data is a shared responsibility. | `context/company.md`, Positioning against Atlassian's native Backup and Restore. PRD, Problem. |
| Rewind's existing single-item restore | Restores a single ticket, page, file or configuration without a full-site restore. Customers who already have Rewind use it. | It is built to restore a chosen item. The sources do not say it can find and undo all changes by one actor across a time window. Actor-based rollback is the new capability and is not an existing proof point. | `context/proof-points.md`, Atlassian-specific. `02-launch-context.md`, item 3 under disagreements. |
| Other third-party backup tools | [NEED PROOF: competitor capability check] | [NEED PROOF: competitor capability check] | PRD, Competitive notes: blank. No claim is made about these tools. |

What this tells us: the real competitor is the choice between two bad options, restore everything or fix it by hand, plus the habit of doing nothing until it happens. Nothing here compares Rewind to another vendor.

## 2. Unique attributes

Uniqueness is only claimed against alternatives we can source. Native is sourced at the site level only. Other third-party tools are unchecked.

| Attribute | Alternatives that lack it | Confirmed? | Source |
|---|---|---|---|
| Actor view: every change grouped by who or what made it (person, automation rule, integration, AI agent) | Doing nothing and fixing by hand have no such view. Native works at the site level. Other tools: [NEED PROOF: competitor capability check] | Partly. Confirmed as new for Rewind. Not yet confirmed as unique in the market. | PRD, What it does 1. |
| Blast radius preview: before restoring, see which issues, fields and projects change back and what stays | Not stated in any source for any alternative | Not yet confirmed as unique. | PRD, What it does 2. |
| Selective rollback: undo all changes by one actor in a time window, or pick issues or fields | Native works at the site level, so it restores the site and not one actor. Other tools: [NEED PROOF: competitor capability check] | Confirmed against native at the site level only. Not yet confirmed as unique against other vendors. Do not say native "has no actor-based rollback" until a human sources it. | PRD, What it does 3. `context/company.md`. `02-launch-context.md`, disagreement 2. |
| Keep human work: changes people made after the bad event are preserved | A whole-site restore returns the site to the backup, so later legitimate changes are lost (the PRD states this as the cost of that option). Other tools: [NEED PROOF: competitor capability check] | Confirmed as the difference from a whole-site restore. Not yet confirmed as unique in the market. Conflict handling when a person edited the same field is [NEED PROOF: engineering confirmation]. | PRD, Problem and What it does 4. |
| Audit log: each rollback recorded (who ran it, what changed, when), exportable for auditors | Not stated in any source for any alternative | Not yet confirmed as unique. No compliance or standards claim is allowed. | PRD, What it does 5. |

The combination is the strongest attribute: find by actor, preview, undo only that actor, keep human work, record it. Each piece alone may exist elsewhere, which we have not checked. The combined workflow for Jira is what the PRD describes as new.

## 3. Value and proof

| Attribute | Value to the customer | Proof | Source |
|---|---|---|---|
| Actor view | The admin can answer "what did this agent or rule actually change?" in one place, instead of searching issue by issue. | PRD fact only. [NEED PROOF: how Actor view tells the four actor types apart] | PRD, What it does 1. |
| Blast radius preview | The admin and the IT leader see what will change back and what will stay before anything is restored. Nothing is a surprise. | PRD fact only. [NEED PROOF: preview accuracy and any limits on size] | PRD, What it does 2. |
| Selective rollback | Undo the one actor's changes, not the whole site. The admin does not trade a bad fix for a lost day of everyone's work. | PRD fact only. No restore time benchmark is approved. [NEED PROOF: rollback speed and limits on time window or number of issues] | PRD, What it does 3. `context/proof-points.md`, Not yet approved. |
| Keep human work | People's changes made after the bad event stay in place. | PRD fact only. [NEED PROOF: how conflicts are handled when a person edited the same issue or field] | PRD, What it does 4. |
| Audit log | The IT or security leader gets a record of each rollback to show auditors, and a recovery plan to attach to an AI rollout approval. | PRD fact only: "exportable for auditors." [NEED PROOF: retention, export format, any named standard] | PRD, What it does 5. |
| Whole combination | A Jira admin can say yes to more agents and automation because they can undo one actor's work. Rewind's company context says AI agents create new rollback and recovery needs. | Company-level proof exists: Rewind protects 16 cloud applications for more than 25,000 organizations, including companies in financial services, healthcare and manufacturing. This is trust context, not proof the feature works. Customer evidence for this feature: [NEED PROOF: no customer name, quote or benchmark is approved]. | `context/proof-points.md`. `context/company.md`. |

Limits that travel with the value (all four are must-say, from `02-launch-context.md`):
1. Only changes made after the customer's first Rewind backup can be rolled back.
2. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Use the PRD wording. Do not put the company-level "under 24 hours" claim near Agent Rollback until a human resolves the conflict.
3. Jira Cloud only at launch. Confluence is on the roadmap, no date committed.
4. Included only at a specific plan tier. [NEED PROOF: plan names and pricing]

## 4. Best-fit customers

Who cares most, given the value above and the alternatives they have today:

**The core fit is a Jira Cloud admin whose team has agents or heavy automation writing to issues, and who has been or will be asked to approve or defend that setup.** The value (undo one actor, keep everyone else's work) is worth most where an actor can change a lot, fast, and where a whole-site restore would cost real legitimate work.

Observable signals, taken from `03-audience.md`:
- Already has a Rewind Jira Cloud backup. This is a hard requirement, and only changes after the first backup can be rolled back. It is also the upgrade audience for the plan tier.
- Runs or is rolling out AI agents that edit Jira issues. The admin or platform lead talks about guardrails, "human in the loop" or blast radius.
- Has many automation rules, bulk changes or integrations that write to issues or custom fields across projects.
- Has an IT or security approver in the AI project asking for a recovery plan.
- Regulated settings (financial services, healthcare, manufacturing) where an auditor asks for records of changes. Do not claim the log meets any standard.

How the alternatives sharpen this: customers who today choose "fix it by hand" or "restore the whole site" are the ones for whom Agent Rollback is a visible gain. Customers who choose "do nothing" become best-fit at the moment an approver asks for a recovery plan or the first bad change lands.

Who does not fit:
- Anyone who wants to roll back changes made before their first Rewind backup. The product cannot do it.
- Buyers who only need a full-site restore. Native serves that need. Do not frame it as unreliable.
- Confluence-only teams and other platforms. Jira Cloud only at launch.
- Jira customers on plans below the included tier, as a first-wave direct target. They are the upgrade audience, but the tier is unnamed.
- A person-monitoring use. Actor view includes people, but the launch is about agents, rules and integrations.

Segment sizes are unsourced: [NEED PROOF: number of Rewind Jira Cloud customers running AI agents or heavy automation].

## 5. Market category

- **Options considered:**
  1. **SaaS backup and recovery.** The frame Rewind already owns (`context/company.md`). Customers know it. It makes the value of recovery obvious.
  2. **Actor-based rollback for Jira** (a capability within backup). Names the new thing precisely, in the words the PRD uses.
  3. **AI governance or AI safety tooling.** Matches why IT and security leaders care, and the pipeline metric cites AI governance as a buying reason. But the sources do not support a governance product. The audit log is "exportable for auditors" and nothing more.
- **Chosen frame:** SaaS backup and recovery for Jira Cloud, with actor-based rollback as the new capability inside it. Agent Rollback is a part of Rewind's Jira Cloud backup plans, not a separate product category.
- **What it makes customers assume:**
  - Good: it is built on a backup that is independent of the vendor platform, sits on top of Atlassian's native tool, and is run by the people who restore Jira. The shared responsibility story fits without blame.
  - Good: the value is understood fast. Recover one thing, not everything.
  - Bad: customers may assume it can roll back anything from any time. It cannot: only after the first Rewind backup, and attachments come from the latest backup.
  - Bad: customers may assume it replaces native Backup and Restore. It does not. Say that Rewind sits on top.
  - Bad: customers may assume it covers Confluence or all Jira data types. Only Jira Cloud at launch. Data types: [NEED PROOF: which objects and fields can be rolled back].
- **Risk:** The "backup" frame can make the AI angle look like a bolt-on. The AI angle comes from the company context (growth driver 3), so it should be a lead reason, said in the admin's words. The opposite risk is leaning into "AI governance," which invites compliance claims the sources cannot support. Keep the governance language to what the audit log does and the recovery plan an approver wants.

## 6. Relevant trends

Only trends in `context/company.md` or the PRD. No market data is added.

- **AI agents now act directly on SaaS data, which creates new rollback and recovery needs.** Source: `context/company.md`, growth driver 3 (CEO Mike Potter, Aug 2026). Why it matters now: agents are the actors the feature is built to undo.
- **AI agents and automation rules edit Jira issues at a scale no human does.** Source: PRD, Problem. Why it matters now: a mistake can reach thousands of issues before anyone notices, so the whole-site restore and manual fix options are both worse than before. The PRD's 4,000 issues and 30 projects are illustrations of the problem, not customer data.
- **IT and security leaders must approve AI rollouts and want a recovery plan before they say yes.** Source: PRD, Who it's for. Why it matters now: a recovery plan is a condition for adopting AI, so recovery affects the pace of the rollout.
- **The Atlassian cloud migration.** Source: `context/company.md`, growth driver 1. Why it matters now: teams that have moved to cloud may be adding automation and agents. How much this helps migration-led deals: [NEED PROOF: migration-led fit].
- **Not used:** adoption rates of AI in Jira, incident counts or analyst forecasts. None is in the sources: [NEED PROOF: any market data].

## What this means for messaging

Messaging must carry these ideas, in this order:
1. **The moment and the two bad options.** An agent or rule has changed a lot of things. Admins can restore the whole site and lose everyone's legitimate work, or fix it by hand. Lead with the moment the admin recognizes (voice rule: problem, then capability, then proof).
2. **Undo the one actor, keep human work.** Find every change by one agent, rule or integration, preview the blast radius, restore only that, and leave people's changes alone. This is the core value. Say "undo the one change, not the whole site" in the admin's own words (issues, fields, projects, automation rules).
3. **A recovery plan you can show an approver.** Preview before restore and an audit log exportable for auditors give the IT or security leader something to attach to an AI rollout. Say "exportable for auditors" and no more.
4. **Shared responsibility, sitting on top of native.** Native works at the site level and is the right tool for a full-site recovery. Rewind sits on top and covers the actor-level need. No blame, no unreliability framing, and AI and automation owners are never the problem.

Guardrails for messaging:
- Every asset that mentions what can be rolled back carries the first-backup limit. Every platform mention carries Jira Cloud only (Confluence on the roadmap, no date). Every plan mention notes that it is a specific tier. Every attachment mention uses the PRD wording.
- No claim that native "has no actor-based rollback" and no claim about other third-party tools.
- No pairing of Agent Rollback with "under 24 hours."
- No restore speeds, ROI, customer names or quotes.

## Open questions

- [NEED PROOF: competitor capability check] on other third-party backup tools. Until done, no "only," "first" or "unique in the market" claim.
- [NEED PROOF: source or approval for "no actor-based rollback" for Atlassian native]. Until then, say native works at the site level.
- Which attachment wording applies to Agent Rollback (PRD "up to 24 hours old" or the company "under 24 hours")? A human decides.
- [NEED PROOF: how Actor view tells people, automation rules, integrations and AI agents apart, and whether rollback works for each]. Messaging about "AI agents" specifically depends on it.
- [NEED PROOF: which Jira data types and fields can be rolled back, how conflicts with later human edits are handled, and limits on time window and size].
- [NEED PROOF: audit log retention, export format, any named standard]. Legal or compliance should review "exportable for auditors."
- [NEED PROOF: plan names and pricing, and GA date].
- [NEED PROOF: any customer name, quote or benchmark for this feature].
- [NEED PROOF: segment sizes and validation of the demo personas against real customer research].
- Is the Rewind single-item restore a real alternative for actor-level mistakes in practice, or do customers not use it that way? [NEED PROOF: customer research].
