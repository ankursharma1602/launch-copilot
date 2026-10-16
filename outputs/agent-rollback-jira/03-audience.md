# Audience: Agent Rollback for Jira

> The PRD marks this as a hypothetical release. Personas in `context/personas.md` are demo personas, inferred from public positioning. Validate against real customer research before relying on them. No persona is added here. The three below are sharpened for this launch.

## Primary persona: The Atlassian admin

- **Why primary:** The PRD names Jira Cloud admins as the primary user. Every capability (Actor view, Blast radius preview, Selective rollback, Keep human work) is something the admin does with their hands. The admin is also the person who gets looked at when an agent or automation goes wrong, and the one who has to choose today between a whole-site restore and a manual fix. The admin is the one who will open Actor view, so the adoption metric depends on them.
- **Trigger moment:** An automation rule or AI agent has made a large number of wrong changes and someone has noticed. The PRD's own scale examples describe it: an agent reclassifies 4,000 issues, or an automation overwrites a custom field across 30 projects. These are illustrations of the problem, not customer data. A second trigger comes before any bad day: the admin is asked to put another agent or automation into Jira and wants to know they can undo it. In both cases the question is the same: "Can I undo just this, without losing everyone else's work since the last backup?"
- **What they own / fear / want:**
  - Owns: uptime, configuration, permissions, migrations, automations, and increasingly the AI tools wired into Jira.
  - Fears: something breaks at scale and they cannot undo it without restoring the whole site. They are the person everyone looks at.
  - Wants: a fast, surgical restore, and proof they can recover before the bad day happens.
- **Their words:** "roll back," "restore," "automation rule," "bulk change," "sandbox," "RPO." Add the object names admins use: issues, fields, projects. Use "undo the one change, not the whole site" from `context/voice.md`.
- **What turns them off:** Fear-mongering. Vague "peace of mind" copy. Anything that reads as if it was not written by someone who has run Jira. Also: a launch that hides the limits (changes only after the first Rewind backup, attachments up to 24 hours old). Admins find these out on the bad day, so say them up front.

## Secondary persona: The IT or security leader

- **Why:** The PRD names IT and security leaders as secondary: they must approve AI rollouts and want a recovery plan before they say yes. They hold the approval and the budget, and the plan tier decides the expansion goal. Audit log and Blast radius preview speak to their needs (accountability, evidence for auditors, nothing that adds work for their team). They are secondary because they rarely use the product and they decide on what the admin shows them.
- **Trigger moment:** An AI or automation rollout lands on their desk for approval and they need a recovery plan first.
- **What they own / fear / want:** Owns risk, compliance, audit readiness and vendor spend. Fears a data loss event that becomes an audit finding, a customer incident or a board conversation. Wants clear accountability under the shared responsibility model and evidence for auditors.
- **Their words:** "shared responsibility," "business continuity," "governance," "retention policy," "RTO and RPO."
- **What turns them off:** Feature lists without risk framing, unclear pricing, anything that adds work for their team. Pricing is an open gap, so do not wave at it. Also do not make audit or compliance claims beyond "exportable for auditors" (see open questions).

## The AI or automation owner: in the buying group, not a lead target

This persona is not primary or secondary here, because the PRD does not name them as a target. They still matter. They are the person who gets to say yes to AI, and Agent Rollback is the safety net that helps them get that yes from IT and security. Their words ("agents," "guardrails," "blast radius," "undo," "human in the loop") can be used in copy aimed at the admin and the IT leader. Never frame them as the cause of the problem. The agent or rule is one actor among several, and people appear in Actor view too.

## Best-fit segments

Signals are things a salesperson or marketer could observe. Criteria come from the PRD and `context/`. No sizes, shares or counts are stated, because none are sourced.

| Segment | Signals to look for | Why they fit | Evidence |
|---|---|---|---|
| Jira Cloud customers running AI agents in Jira | Rolling out or already running AI agents that edit issues. The admin or platform lead mentions agents, "human in the loop" or guardrails. | The PRD's primary segment: companies using AI agents. Agents edit at a scale no human does. | PRD, Who it's for and Problem. Size: [NEED PROOF: number of Rewind Jira Cloud customers running AI agents] |
| Jira Cloud customers with heavy automation | Many automation rules, bulk changes or integrations that write to issues or custom fields across projects. | The PRD's primary segment also names "heavy automation." | PRD, Who it's for. Size: [NEED PROOF: number of customers with heavy automation, and how "heavy" is defined] |
| Existing Rewind Jira Cloud backup customers | Already has a Rewind Jira Cloud backup in place. | Agent Rollback needs a Rewind Jira Cloud backup, and only changes after the first backup can be rolled back. It is also an upgrade path inside the plan. | PRD, Availability and Known limitations. `02-launch-context.md`, Dependencies. Plan mix: [NEED PROOF: current plan mix] |
| Companies where IT or security must approve AI rollouts | An AI governance review, a recovery plan requirement, or an IT or security approver in the AI project. | The PRD names this group as secondary, and its pipeline metric tracks AI governance as a buying reason. | PRD, Who it's for and Success metrics. Whether the CRM can capture it: [NEED PROOF: revenue operations confirmation] |
| Regulated organizations that need audit evidence | Customers in financial services, healthcare or manufacturing, with an auditor asking for records of changes. | The audit log is exportable for auditors. Rewind customers include these industries. | `context/proof-points.md` (industries only). Do not claim the log meets any audit standard: [NEED PROOF: audit log retention, export format and standards] |
| Jira Cloud migrating teams adding automation and AI after the move | Recently moved to Atlassian cloud and now adding automation or agents. | Ties to growth driver 1 in `context/company.md`. | How much it helps migration-led deals is not stated in the PRD: [NEED PROOF: migration-led fit] |

Segment rule: all segments need Jira Cloud. Jira Cloud is the only platform at launch. Confluence is on the roadmap with no date, so do not build a Confluence segment.

## Buying group

| Role | Persona | Part in the decision |
|---|---|---|
| User | Atlassian admin | Opens Actor view, previews the blast radius, runs the rollback. Starts the conversation and builds the case. |
| Approver (economic buyer) | IT or security leader | Approves AI rollouts and spend. Wants a recovery plan, evidence for auditors, and a clear plan tier and price before saying yes. |
| Influencer | AI or automation owner | Wants to deploy agents and needs IT and security approval. Agent Rollback is their safety net. They push for it internally. |
| Gatekeeper (inferred, not in the PRD) | Legal or compliance reviewer on the customer side | May review "exportable for auditors." [NEED PROOF: whether customers involve compliance reviewers in this purchase] |
| Channel | Atlassian Marketplace and partners | A route to market named in `context/company.md`. Their part in this purchase is [NEED PROOF: share of Jira buyers who buy through Marketplace or partners]. |

## Out of focus for this launch

- **Confluence-only admins and teams.** Confluence is on the roadmap with no committed date. Do not target them or imply coverage.
- **Teams on other platforms (GitHub, Shopify and the rest of the 16 apps).** This is a Jira Cloud launch.
- **Jira customers on plans below the tier that includes Agent Rollback, as a first-wave target for direct promotion.** They matter as the upgrade audience, but the tier and price are not named ([NEED PROOF: plan names and pricing]), so no plan-based targeting yet.
- **The AI or automation owner as a lead audience.** Covered above. They are an ally in the story, not the audience the copy leads with.
- **Buyers who want to roll back changes made before their first Rewind backup.** The product cannot do that. Do not attract them.
- **Buyers looking for a full-site restore only.** Rewind sits on top of Atlassian's native Backup and Restore and does not replace it. That need is served by the native tool. Do not frame native as unreliable.
- **Individual people as a target.** The product covers changes by people too, but the launch is about agents, rules and integrations. Not a person-monitoring tool.

## Open questions

- Which customers are in the primary segment? Number of Rewind Jira Cloud customers running AI agents or heavy automation: [NEED PROOF: segment sizes and source].
- Do these demo personas match real customers? `context/personas.md` says to validate them. [NEED PROOF: customer research].
- Which Jira or Rewind permission is needed to run a rollback? This decides whether the admin can act alone or needs IT sign-off. [NEED PROOF: roles and permissions].
- Does the IT or security leader need the plan name and price to move forward? [NEED PROOF: plan names and pricing].
- Can the CRM capture "AI governance cited as a buying reason"? [NEED PROOF: revenue operations confirmation].
- Can Actor view tell AI agents apart from automation rules and integrations? Copy for the AI-agent segment depends on it. [NEED PROOF: how Actor view tells actor types apart].
- Does it work on large sites above Atlassian's size limits? [NEED PROOF: engineering confirmation].
- Is any customer evidence approved for this audience? None is in `context/proof-points.md`.
- Must-say limitations (all four from `02-launch-context.md`) apply to every segment. The attachment wording conflict (up to 24 hours vs "under 24 hours") is still open for a human to decide.
