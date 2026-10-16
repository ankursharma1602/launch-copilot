# Launch brief: Agent Rollback for Jira

**Source:** inputs/closed-beta-handoff-agent-rollback-jira.md | **Launch date:** [NEED PROOF: GA date] | **Status:** Kickoff

> The handoff is a hypothetical, mock document. Agent Rollback is not a real or announced Rewind product. Closed beta numbers and quotes are internal mock evidence from a small group. They frame this brief only. They are not proof and must not appear in customer-facing assets (see `context/proof-points.md`).

## What is launching

Jira admins can find and undo every change made by one AI agent, automation rule or integration, in any time window, without restoring the whole site and without touching changes people made. Before they undo anything, they see which issues, fields and projects will change back and which will stay as they are. Every rollback is recorded in an audit log.

The release has five capabilities, all done and in closed beta: Actor view (ROLL-101), Blast radius preview (ROLL-102), Selective rollback (ROLL-103), Keep human work (ROLL-104) and Audit log (ROLL-105). It is Jira Cloud only. Confluence is on the roadmap with no date committed.

Known limitations the handoff states:
- Only changes made after the customer's first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.

## Why it matters to the business

Growth driver 3 in `context/company.md`: AI usage. AI agents now act directly on SaaS data, which creates new rollback and recovery needs. Agent Rollback is a product answer to that need, in Jira, where Rewind already sells backup.

The commercial logic, as the handoff frames it:
- **Expansion.** It is included in Rewind's Jira Cloud backup plans at a higher tier. Plan name and price are not set. [NEED PROOF: plan names and pricing]
- **Pipeline.** Security and IT leaders want a recovery plan before they approve an AI rollout. The handoff proposes counting new opportunities where AI governance is a buying reason. Revenue operations cannot capture that in the CRM yet.
- **Link to the Atlassian cloud migration (driver 1).** The product is Jira Cloud only, so it also touches the first driver. The handoff does not make that case, so the link is untested.

The handoff's problem statement: admins now have two bad options when an agent or rule goes wrong. They restore the whole site and lose every legitimate change since the backup, or they fix things by hand. Context supports the site-level versus single-item framing (`context/company.md`, Atlassian native tool is built for full-site recovery).

## Goals

These are the handoff's proposed success metrics. None has a baseline or target yet.

| Goal | Metric | Baseline | Target | Source |
|---|---|---|---|---|
| Adoption | % of active Jira customers who open Actor view within 30 days of L | [NEED PROOF: baseline] | [NEED PROOF: target] | Handoff, section 1 |
| Expansion | Upgrades to the plan that includes Agent Rollback within 90 days of L | [NEED PROOF: current upgrade rate] | [NEED PROOF: target] | Handoff, section 1 |
| Pipeline | New opportunities where AI governance is cited as a buying reason | [NEED PROOF: baseline; not captured in CRM today] | [NEED PROOF: target] | Handoff, section 1 and Slack (revenue operations) |

The pipeline metric cannot be measured until the CRM can capture the buying reason. That is an open question below.

## Timeline

The GA date is not given, so launch day is "L". This brief does not set pre-launch dates. The campaign strategy and launch ops steps own those.

| Milestone | When | Depends on |
|---|---|---|
| Closed beta (6 weeks, mock) | Done | Not applicable |
| Open questions below resolved or explicitly deferred | Before L, dates [NEED PROOF: owner dates] | Named answerers |
| Plan name and price confirmed | Before L, date [NEED PROOF: pricing date] | Pricing and packaging |
| Legal review of public wording | Before L, date [NEED PROOF: legal date] | Final draft of external copy |
| Approval to use any beta numbers or quotes externally | Before L, if wanted | Customer agreement, then approval |
| GA | L, [NEED PROOF: GA date] | Items above |
| Adoption check (Actor view opened) | L+30 | Product analytics set up |
| Expansion check (upgrades) | L+90 | Plan and pricing live |

## Stakeholders

Roles only. The handoff names no people.

| Role | Owns in this launch |
|---|---|
| Product manager, Jira | Handoff, scope, success metrics, which data types can be rolled back |
| Engineering lead | How Actor view separates actor types, the person-edited-after-agent case, large-site behavior |
| Pricing and packaging | Plan name and price |
| Product marketing | Launch brief, positioning, messaging, launch kit, what claims are allowed |
| Sales Engineering | Competitive claim sourcing, large-site questions, demo |
| Sales | Using the kit with prospects and customers |
| Support lead | Plain wording of the attachment limitation, reading the first-backup limitation to customers |
| Customer success | Who may run a rollback, onboarding of beta accounts, customer agreement for external use of feedback |
| Legal | Review of "exportable for auditors" and any Confluence mention |
| Revenue operations | CRM capture of "AI governance cited as a buying reason" |
| Brand team | Confirmation of visual identity before visuals leave the team (`context/brand.md`) |

## Open questions

Carried from the handoff's Slack thread and from checking it against `context/`. Nothing here is resolved in this brief.

| Question | Why it matters | Who can answer |
|---|---|---|
| **Attachment wording versus context.** The handoff says deleted attachments come from the most recent backup, "which may be up to 24 hours old". The company site and `context/company.md` say Rewind recovery points are under 24 hours. Which wording do we use for Agent Rollback? | These can read as a contradiction. Support asked for plain wording before GA. A wrong choice weakens trust or overclaims. | Support lead, Product manager, Jira, Engineering lead |
| **"No actor-based rollback" in Atlassian native.** The handoff states native Backup and Restore "has no actor-based rollback" and Sales Engineering asked if there is a source. `context/company.md` says only that the native tool is built for full-site recovery. No source is on file. | A competitive claim with no source cannot ship. It also touches the voice rule not to imply Atlassian is unreliable. | Sales Engineering, Product manager, Jira. [NEED PROOF: source for native tool capability] |
| **Other third-party backup tools.** Capability check not done. | Limits any "only Rewind" style claim. | Product marketing, Sales Engineering. [NEED PROOF: competitor capability check] |
| **GA date.** Not given. | Sets every date in the plan. | Product manager, Jira |
| **Plan names and pricing.** Pricing and packaging owes these. Until then the handoff only says "a specific plan tier". | Without it the expansion goal and the buyer's next step are unclear. | Pricing and packaging |
| **Can beta numbers or quotes be used externally?** Customers have not agreed. `context/proof-points.md` lists beta results and quotes as not approved. | Decides whether any customer proof exists at launch. Today there is none. | Customer success (customer consent), then Product marketing and Legal (approval) |
| **How does Actor view tell a person, a rule, an integration and an AI agent apart?** Not documented. | Any claim about identifying AI agents depends on it. | Engineering lead |
| **What if a person edited the same field the agent changed?** Not covered in beta tests. Not decided. | It sits close to the "keeps human work" promise. | Engineering lead, Product manager, Jira |
| **Who is allowed to run a rollback?** Admin only, or other roles? Security and IT buyers asked. | An approval-minded buyer will ask first. | Customer success, Product manager, Jira |
| **Which Jira data types can be rolled back beyond issues and fields?** Not confirmed. | Limits what "every change" can mean in copy. | Product manager, Jira |
| **Behavior on sites above Atlassian's size limits.** Context says Rewind covers such sites for backup. Whether Agent Rollback does is not known. | Do not carry the backup claim over to this feature without proof. | Sales Engineering, Engineering lead. [NEED PROOF: large-site behavior] |
| **Legal wording.** "Exportable for auditors" and any Confluence mention need review before going public. | Compliance claims and roadmap statements carry legal risk. | Legal |
| **How to track the pipeline metric.** CRM cannot capture "AI governance cited as a buying reason". | The pipeline goal cannot be measured at L. | Revenue operations |
| **Customer misunderstanding of the first-backup limitation.** Two beta accounts (mock) did not understand that only changes after the first Rewind backup can be rolled back. | Limitation must be stated plainly in customer-facing assets. | Support lead, Product marketing |
| **Confluence demand.** Four beta accounts (mock) asked for it. No date is committed. | Risk of implying a date. Only Legal-approved roadmap wording can be used. | Product manager, Jira, Legal |
| **Tier.** Not decided here. | The campaign strategy step scores it with `context/tiering.md`. | Campaign strategy |
| **Brand assets.** Hex codes and typeface in `context/brand.md` are not confirmed by Rewind. | Visuals should not go outside the team unconfirmed. | Brand team. [NEED PROOF: confirm brand hex codes and typeface] |
