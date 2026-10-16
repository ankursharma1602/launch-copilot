# Messaging: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. Every message below comes from `04-positioning.md`. Where the positioning has no support, the message carries `[NEED PROOF: ...]` or is listed under "Positioning gaps found".

## Core message
When an AI agent or automation rule changes thousands of Jira issues the wrong way, Agent Rollback lets you find everything that one actor changed, preview the impact, and undo only that, so you keep the work your people did since, with a record of the rollback you can export for auditors.
Support: The alternative is to restore the whole site and lose legitimate changes, or to fix it by hand. Rewind sits on top of Atlassian's native Backup and Restore, which works at the site level, and covers the actor-level need. Rewind protects 16 cloud applications for more than 25,000 organizations. That is trust context, not proof of this feature.

Scope note: this message applies to Jira Cloud only, to changes made after the customer's first Rewind backup, and to the plan tier that includes Agent Rollback. Every asset that uses the core message carries the Must say list below.

## Value pillars
| Pillar | Claim | Proof | Source |
|---|---|---|---|
| 1. Undo the one actor, not the whole site | See every change grouped by who or what made it, then undo all of one actor's changes in a time window, or pick the issues or fields to undo. You do not trade a bad fix for a lost day of everyone's work. | PRD fact only. [NEED PROOF: how Actor view tells people, automation rules, integrations and AI agents apart] [NEED PROOF: rollback speed and limits on time window or number of issues] Illustration of the problem, not customer data: an agent reclassifies 4,000 issues, or an automation overwrites a custom field across 30 projects. | 04-positioning.md, section 3 (Actor view, Selective rollback). PRD, What it does 1 and 3. |
| 2. Keep your people's work | Changes people made after the bad event stay in place. Before anything is restored, you see which issues, fields and projects will change back and what will stay as is. | PRD fact only. [NEED PROOF: how a rollback is handled when a person later edited the same issue or field] [NEED PROOF: preview accuracy and any limits on size] | 04-positioning.md, section 3 (Keep human work, Blast radius preview). PRD, What it does 2 and 4. |
| 3. A recovery plan you can show an approver | Each rollback is recorded (who ran it, what changed, when) and the record is exportable for auditors. An IT or security leader can attach a preview-then-restore plan to an AI rollout approval. | PRD fact only: "exportable for auditors." [NEED PROOF: audit log retention, export format, any named standard] No compliance claim is made. Legal or compliance review of the wording is pending. | 04-positioning.md, section 3 (Audit log) and "What this means for messaging" item 3. PRD, What it does 5. |

Customer evidence for any pillar: [NEED PROOF: no customer name, quote or benchmark is approved in `context/proof-points.md`].

Supporting message (not a pillar): Recovery of your own data is a shared responsibility. Native Backup and Restore does what it was built to do and is the right tool for a full-site loss. Rewind sits on top of it. Source: 04-positioning.md, section 1 and "What this means for messaging" item 4.

## Angles by persona

### The Atlassian admin (primary)
- **Lead with:** The moment. An agent or rule has changed a lot of issues, and the choices are a whole-site restore or hours of fixing by hand. Then: "Undo the one change, not the whole site." A second lead for before the bad day: you are asked to add another agent or rule and want to know you can undo it.
- **Pillar:** 1, then 2.
- **Words to use:** roll back, restore, automation rule, bulk change, issues, fields, projects, actor, blast radius preview, "what did this agent change?"
- **Proof to use:** The PRD's two scale examples, labeled as illustrations of the problem. PRD facts for the four capabilities. No benchmark.
- **Avoid:** Fear-mongering. Vague reassurance copy. Restore speeds. Implying it undoes anything from any time. Hiding the first-backup limit or the attachment limit: admins find these out on the bad day, so state them up front.

### The IT or security leader (secondary)
- **Lead with:** The approval. You need a recovery plan before you say yes to an AI rollout. Here is one: preview what will change, restore only one actor's changes, keep a record you can export for auditors.
- **Pillar:** 3, then 2.
- **Words to use:** recovery plan, accountability, shared responsibility, business continuity, audit log, "exportable for auditors."
- **Proof to use:** PRD facts on preview and audit log. Company-level trust context (16 cloud applications, more than 25,000 organizations, customers in financial services, healthcare and manufacturing), stated as context only.
- **Avoid:** Any audit or compliance standard, certification, or "audit-ready" claim. "AI governance product" framing. Naming a plan or price (`[NEED PROOF: plan names and pricing]`). Feature lists without the risk framing. Anything that suggests extra work for their team.

### The AI or automation owner (influencer, not a lead target)
- **Lead with:** Use only inside copy aimed at the admin or IT leader: agents get approved faster when there is a way to undo one agent's work.
- **Pillar:** 1 and 3, as the safety net behind the yes.
- **Words to use:** agents, guardrails, blast radius, undo, human in the loop.
- **Proof to use:** Same PRD facts as above. No separate proof.
- **Avoid:** Framing this owner, their agent or their rules as the problem. The agent is one actor among several, and people show up in Actor view too. Do not direct copy at this persona as the lead audience. Do not promise rollback works for "AI agents" specifically until the actor-type question is answered.

## Must say (limitations every asset repeats)
Use this wording or a close, short form that keeps the meaning. Short assets write these in first, then cut other words.

1. **First backup.** "Only changes made after your first Rewind backup can be rolled back." Required wherever the asset says what can be rolled back.
2. **Attachments.** "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old." Required wherever attachments are mentioned. Use the PRD wording as written. A human still has to decide whether the company-level recovery point claim can sit near this feature.
3. **Platform.** "Jira Cloud only at launch. Confluence is on the roadmap, no date committed." Required wherever platform coverage is mentioned. Confluence roadmap wording still needs sign-off: [NEED PROOF: sign-off to mention Confluence roadmap publicly].
4. **Plan.** "Included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it." Required wherever plans are mentioned. Do not name the tier or price: [NEED PROOF: plan names and pricing].

Also required: GA date is [NEED PROOF: GA date]. No dated line until product supplies it.

## Vocabulary
- **Use:** undo the one change, not the whole site; roll back; restore; actor; automation rule; integration; AI agent; issues, fields, projects; blast radius preview; keep your people's work; audit log; "exportable for auditors"; shared responsibility; "sits on top of Atlassian's native Backup and Restore"; "native works at the site level."
- **Avoid:**
  - Banned list from `context/voice.md`: peace of mind, game-changer, revolutionary, seamless, cutting-edge, best-in-class, unlock, supercharge, leverage (as a verb), robust, effortless, world-class, next-generation, synergy, disrupt.
  - Em dashes and exclamation marks in customer-facing copy.
  - Any statement that Atlassian native lacks actor-based rollback. Say native works at the site level.
  - Any claim about other third-party backup tools, and "only," "first" or "unique in the market" wording.
  - Pairing Agent Rollback with the company-level recovery point claim.
  - Restore speeds, time saved, ROI, customer names, quotes, incident counts or adoption data.
  - "Guaranteed," "complete," "everything," "any change," or "audit-ready," "compliant."
  - Stating customer patterns as fact (lesson: "rarely," "usually," "often"). Describe the scenario or ask the buyer.
  - Framing Atlassian as unreliable, or AI and automation owners as the problem.
  - Feature names as headlines ("Actor view," "Selective rollback"). Use them in body copy only.

## Headline check
Headlines say what the customer gets back. Each is checked against the pillar it serves.

| Headline | Pillar | Passes? |
|---|---|---|
| Undo one agent's changes, not the whole site. | 1 | Yes. Customer outcome, in admin words. |
| Your agent changed thousands of issues. Get them back without losing your team's work. | 1, 2 | Yes. Problem, then outcome. Needs the first-backup limit nearby. |
| See what will change back before you restore anything. | 2 | Yes. |
| A recovery plan to show the person who approves your AI rollout. | 3 | Yes. No compliance claim. |
| Say yes to more automation, with a way to undo it. | 1, 3 | Yes. Needs a Jira Cloud only line where platform is stated. |

Rejected as feature-name headlines: "Introducing Actor view," "Agent Rollback is here," "Selective rollback for Jira."

## Traceability
| Message | Comes from (04-positioning.md section) |
|---|---|
| Core message, problem and two bad options | "What this means for messaging" item 1; section 1 (Competitive alternatives) |
| Pillar 1, undo the one actor | Section 3 (Actor view, Selective rollback); "What this means for messaging" item 2 |
| Pillar 2, keep your people's work and preview | Section 3 (Keep human work, Blast radius preview); section 2 (Keep human work) |
| Pillar 3, recovery plan for an approver | Section 3 (Audit log); "What this means for messaging" item 3 |
| Supporting message, shared responsibility and native at the site level | Section 1 (whole-site row); "What this means for messaging" item 4 |
| Company trust context (16 apps, 25,000 organizations) | Section 3 (Whole combination) |
| Persona leads and avoid lists | Section 4 (Best-fit customers); section 5 (bad assumptions); `03-audience.md` |
| Must say 1 to 4 | Section 3 (Limits that travel with the value); guardrails in "What this means for messaging" |
| Vocabulary avoid list | Guardrails in "What this means for messaging"; `context/voice.md` |

## Positioning gaps found
- **Actor types.** Positioning does not say how Actor view tells people, automation rules, integrations and AI agents apart, or whether rollback works for each. Messaging that names "AI agents" specifically is therefore limited to "AI agent, automation rule or integration" as examples of actors, with no promise per type.
- **Why now has no data.** Section 6 supports only the trend, not any adoption number or incident count. Messaging cannot cite market data.
- **Customer proof.** No customer name, quote or benchmark for this feature. All three pillars rest on PRD facts only.
- **"Keep human work" conflicts.** Positioning does not say what happens when a person edited the same field the actor changed. Pillar 2 cannot promise a clean result in that case.
- **Data types and limits.** Positioning does not list which objects can be rolled back (comments, workflows, permissions) or any size or window limit. Copy says "issues and fields" only.
- **Differentiation.** Positioning cannot confirm any attribute as unique in the market. Messaging uses no "only" or "first" claim and relies on the combined workflow and the whole-site contrast.
- **Attachment wording conflict** between the PRD and company context is still open for a human. Messaging uses the PRD wording.
- **Plan, price and GA date** are unknown. No message names a plan or a date.
- **Audit log wording** needs legal or compliance review before use in any customer-facing asset.
