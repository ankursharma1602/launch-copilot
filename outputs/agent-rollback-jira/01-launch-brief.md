# Launch brief: Agent Rollback for Jira

**Source:** inputs/prd-agent-rollback-jira.md | **Launch date:** [NEED PROOF: GA date] | **Status:** Kickoff

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product.

## What is launching
Jira admins can find and undo every change made by one AI agent, automation rule or integration, in any time window. They do it without restoring the whole site and without touching changes made by people. It is available for Jira Cloud first.

## Why it matters to the business
This ties to growth driver 3 in `context/company.md`: AI usage. AI agents now act directly on SaaS data, which creates new rollback and recovery needs. Agent Rollback gives Rewind a specific answer to that need in Jira.

The commercial logic, as the PRD frames it:
- **Expansion:** the capability is included at a higher plan tier, so it gives existing Jira customers a reason to upgrade. Plan names and pricing are [NEED PROOF: plan names and pricing].
- **Pipeline:** IT and security leaders must approve AI rollouts and want a recovery plan before they say yes. The PRD proposes tracking opportunities where AI governance is a buying reason.
- **Fit with the Atlassian migration driver (driver 1):** it builds on Rewind's existing Jira Cloud backup base. How much it helps migration-led deals is not stated in the PRD.

## Goals
The PRD labels its success metrics "proposed". None has a baseline or target.

| Goal | Metric | Baseline | Target | Source |
|---|---|---|---|---|
| Adoption | % of active Jira customers who open Actor view within 30 days | [NEED PROOF: current active Jira customer count and baseline] | [NEED PROOF: target %] | PRD, Success metrics |
| Expansion | Upgrades to the plan that includes Agent Rollback within 90 days | [NEED PROOF: current plan mix] | [NEED PROOF: target upgrade count or %] | PRD, Success metrics |
| Pipeline | New opportunities where AI governance is cited as a buying reason | [NEED PROOF: baseline count, and whether the CRM can capture this reason] | [NEED PROOF: target count] | PRD, Success metrics |

## Timeline
No launch date is given, so launch day is "L". Offsets and owners below are placeholders for the team to confirm. They are not commitments.

| Milestone | When | Depends on |
|---|---|---|
| GA date confirmed | Before any other milestone | Product decision on [NEED PROOF: GA date] |
| Plan names and pricing confirmed | Before copy is final | Pricing decision |
| Competitor capability check complete | Before positioning is final | Research on other third-party backup tools |
| Launch kit built and reviewed | Before L | Tier decision, positioning, messaging |
| Sales enablement delivered to reps | Before L | Approved messaging and limitations wording |
| Launch day | L | GA date |
| Adoption read-out | L + 30 days | Actor view usage data |
| Expansion read-out | L + 90 days | Plan upgrade data |

## Stakeholders
The PRD names no people, so these are roles.

| Role | Owns in this launch |
|---|---|
| Product manager for Jira | PRD facts, GA date, known limitations, Confluence roadmap wording |
| Product marketing lead | Launch brief, positioning, messaging, campaign strategy |
| Pricing and packaging owner | Plan names, pricing, which tier includes Agent Rollback |
| Sales leadership and enablement | Rep readiness, talk track, objection handling |
| Marketplace and channel owner | Atlassian Marketplace listing and partner communication |
| Customer success or support lead | Customer communication, handling of the attachment limitation |
| Revenue operations | Tracking for the three success metrics, including "AI governance cited as a buying reason" |
| Legal or compliance reviewer | Audit log and "exportable for auditors" wording |
| Engineering lead | Accuracy of what the product does at launch |

## Open questions
| Question | Why it matters | Who can answer |
|---|---|---|
| What is the GA date? | Every date in the plan depends on it. | Product manager for Jira |
| What are the plan names and pricing, and which plan includes Agent Rollback? | The expansion goal depends on it. Copy cannot name a plan without it. | Pricing and packaging owner |
| What can other third-party backup tools do for actor-based rollback? | The PRD leaves this blank. Competitive claims beyond Atlassian cannot be made. | Product marketing or competitive intelligence |
| What are the baselines and targets for the three success metrics? | The PRD calls them proposed and gives no numbers. Without them, nobody can call the launch a success or a miss. | Product manager, revenue operations |
| Can the business track "AI governance cited as a buying reason" in opportunities today? | The pipeline metric needs a field or a process. | Revenue operations |
| The PRD says attachments deleted by an agent come from the most recent backup, "which may be up to 24 hours old". `context/company.md` and `context/proof-points.md` say Rewind supports recovery points under 24 hours. Which wording is right for Agent Rollback? | The two statements read differently. Copy must not promise a recovery point the product does not deliver here. | Product manager for Jira, engineering lead |
| The PRD says only changes made after a customer's first Rewind backup can be rolled back. Should this be stated in all customer-facing assets? | A short asset can drop it. Customers who expect to roll back older agent changes would be misled. | Product manager, product marketing lead |
| Are there any claims about the Atlassian native tool beyond what `context/company.md` says? The PRD says it has "no actor-based rollback". | The context says native is built for full-site recovery. The "no actor-based rollback" claim is the PRD's own and has no source behind it. | Product manager, product marketing lead |
| Does Agent Rollback work for changes made by every kind of actor named in the PRD (people, automation rules, integrations, AI agents), and how does it tell them apart? | Messaging should only promise what Actor view can identify. | Engineering lead |
| Is there any customer evidence, such as a named customer, quote or benchmark, that can be used? | `context/proof-points.md` approves no customer logos, quotes, restore time benchmarks or ROI figures. | Customer success, product marketing lead |
| Is a Confluence date or any public mention of it allowed? | The PRD says "on the roadmap, no date committed". Roadmap language needs sign-off. | Product manager, legal reviewer |
| Which tier does this launch get? | Not decided here. The campaign strategy step scores it with `context/tiering.md`. | Campaign strategy agent, with human review |
