# Launch context: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. If a fact is not in this file, downstream agents should not state it.

## What's shipping
Agent Rollback lets a Jira Cloud admin find and undo every change made by one specific actor: a person, an automation rule, an integration or an AI agent. The admin picks a time window, previews what will change back, and restores only that actor's changes. Changes made by people after the bad event stay in place. Every rollback is recorded in an audit log that can be exported for auditors. It is included in Rewind's Jira Cloud backup plans at a tier that is not yet named. Jira Cloud only at first.

## Capabilities in customer terms
| PRD capability | What the customer can do | Matters most to |
|---|---|---|
| Actor view | See every change in Jira grouped by who or what made it: a person, an automation rule, an integration or an AI agent. | Jira admin; AI or automation owner |
| Blast radius preview | Before restoring, see which issues, fields and projects will change back and what will stay as is. | Jira admin; IT or security leader |
| Selective rollback | Undo all changes by one actor in a time window, or pick specific issues or fields to undo. | Jira admin |
| Keep human work | Roll back an actor's changes while changes people made after the bad event are preserved. | Jira admin |
| Audit log | Have a record of each rollback (who ran it, what changed, when) and export it for auditors. | IT or security leader; Jira admin |
| Whole-site alternative (problem the PRD describes) | Avoid the two options admins have today: restore the whole site and lose legitimate changes since the backup, or fix by hand. | Jira admin |

Scale examples the PRD uses for the problem: an agent reclassifies 4,000 issues, or an automation overwrites a custom field across 30 projects. These are illustrations of the problem, not customer data. Do not present them as real incidents or typical cases.

## Limitations
1. Only changes made after the customer's first Rewind backup can be rolled back. | Must say: yes
2. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. | Must say: yes
3. Jira Cloud only at launch. Confluence is on the roadmap with no date committed. | Must say: yes, wherever platform coverage is mentioned
4. Agent Rollback is included only in the Rewind Jira Cloud backup plans at a specific tier, so not every plan has it. Tier name is not yet known. | Must say: yes, wherever plans are mentioned

Notes on limitations:
- Limitation 2 is flagged below because it conflicts in wording with `context/`. Repeat the PRD wording as written until a human decides.
- Limitation 4 is a reading of "included in ... at the [tier]". The PRD does not say which plans exclude it. Confirm.

## Availability
- Plans: included in Rewind's Jira Cloud backup plans at the [NEED PROOF: plan names and pricing] tier.
- Platforms: Jira Cloud first.
- Date: [NEED PROOF: GA date]
- Not committed: Confluence is "on the roadmap, no date committed." Do not turn this into a promise or a timeframe.

## Dependencies
- Customer must have a Rewind Jira Cloud backup in place. Only changes after the first Rewind backup can be rolled back.
- Customer must be on the plan tier that includes Agent Rollback.
- Customer must be a Jira Cloud admin (PRD primary user) to use it. Which Jira or Rewind permission this needs is not stated.
- Pricing and packaging decision (plan names, tier, price) before any asset names a plan.
- GA date from product before any dated asset.
- Competitor capability check on other third-party backup tools before any competitive claim beyond Atlassian.
- Revenue operations ability to capture "AI governance cited as a buying reason" for the pipeline metric.
- Legal or compliance review of the "exportable for auditors" wording.

## Gaps (need an answer before launch)
| Gap | Why it matters | Who can answer |
|---|---|---|
| [NEED PROOF: GA date] | Every dated asset depends on it. | Product manager for Jira |
| [NEED PROOF: plan names and pricing, and which tier includes Agent Rollback] | Copy cannot name a plan or price. The expansion goal depends on it. | Pricing and packaging owner |
| [NEED PROOF: competitor capability check on other third-party backup tools] | No claim about other tools can be made. | Product marketing or competitive intelligence |
| [NEED PROOF: sources for the claim that Atlassian native "has no actor-based rollback"] | The claim is the PRD's own. See flagged item below. | Product manager, product marketing lead |
| [NEED PROOF: how Actor view tells the four actor types apart, and whether rollback works for every type] | Messaging should only promise what Actor view can identify. | Engineering lead |
| [NEED PROOF: which Jira data types and fields can be rolled back] | The PRD names issues and fields. It does not list comments, workflows, permissions, or other objects. Do not imply more. | Engineering lead |
| [NEED PROOF: how a rollback is handled when a person later edited the same issue or field the actor changed] | "Keep human work" is stated, but conflict handling is not. | Engineering lead |
| [NEED PROOF: audit log retention, format of export, and whether it meets any named audit standard] | "Exportable for auditors" is all the PRD says. No compliance claims can be made. | Engineering lead, legal or compliance reviewer |
| [NEED PROOF: roles and permissions needed to run a rollback] | IT leaders will ask who can run one. | Engineering lead |
| [NEED PROOF: limits on time window or number of issues per rollback, and expected rollback time] | The PRD says "any time window" but no scale or speed. No restore time benchmarks are approved. | Engineering lead |
| [NEED PROOF: baselines and targets for the three proposed success metrics] | No success definition exists. | Product manager, revenue operations |
| [NEED PROOF: any customer name, quote or benchmark] | None is approved in `context/proof-points.md`. | Customer success, product marketing lead |
| [NEED PROOF: sign-off to mention Confluence roadmap publicly] | Roadmap language needs approval. | Product manager, legal reviewer |
| [NEED PROOF: does Agent Rollback work on large sites above Atlassian's size limits] | `context/` says Rewind covers these sites. The PRD is silent for this feature. | Engineering lead |

## Where the PRD and context/ disagree
Flagged for a human. Not resolved here.

1. **Attachment recovery point (24-hour wording conflict).**
   - PRD: attachments deleted by an agent are restored from the most recent backup, "which may be up to 24 hours old."
   - `context/company.md` and `context/proof-points.md`: Rewind supports recovery points under 24 hours.
   - A human must decide which wording applies to Agent Rollback and whether the company-level "under 24 hours" claim can sit near this feature in any asset. Until then, any asset that mentions attachments must use the PRD wording, and no asset should pair Agent Rollback with the "under 24 hours" claim.

2. **"No actor-based rollback" claim about Atlassian.**
   - PRD: "Atlassian's native Backup and Restore works at the site level and has no actor-based rollback."
   - `context/company.md`: native is "built for full-site recovery." It does not say native lacks actor-based rollback. `context/proof-points.md` has no source for it.
   - A human must source or approve the claim before any asset states it. Until then, downstream agents may say native works at the site level, as `context/` supports, but not that it has no actor-based rollback.

3. **Rewind restores a single item vs. Agent Rollback scope.** Not a conflict, a boundary: `context/` approves single ticket, page, file or configuration restore. The PRD adds actor-based rollback as a new capability. Do not describe actor-based rollback as an existing proof point.

## Voice reminders for later agents
- Never imply Atlassian is unreliable. The point is shared responsibility.
- Never frame AI or automation owners as the problem.
- No customer evidence, restore times or ROI figures are approved.
