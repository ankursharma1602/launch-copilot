# Launch context: Agent Rollback for Jira

**Source:** inputs/closed-beta-handoff-agent-rollback-jira.md | **Builds on:** 01-launch-brief.md | **Launch date:** [NEED PROOF: GA date]

> The handoff is a hypothetical, mock document. Agent Rollback is not a real or announced Rewind product. Later agents must treat every fact below as coming from that handoff, and must not state a fact that is not in this file.

## What's shipping

Agent Rollback lets Jira Cloud admins find and undo every change made by one AI agent, automation rule or integration, in a chosen time window. They do not have to restore the whole site, and changes people made are left alone. Before anything is restored, the admin sees which issues, fields and projects will change back and which will stay as they are. Each rollback is recorded in an audit log that can be exported. Five stories (ROLL-101 to ROLL-105) are done and in closed beta. It is Jira Cloud only. It is included in Rewind's Jira Cloud backup plans at a tier that is not yet named.

## What's built

Everything in this section traces to the epic (section 1), the release notes (section 2) or the demo notes (section 3) of the handoff. No beta numbers or quotes are used here as proof that a capability exists.

### Capabilities in customer terms

| Handoff capability | What the customer can do | Source in handoff | Matters most to |
|---|---|---|---|
| Actor view (ROLL-101) | See every change in Jira grouped by who or what made it: a person, an automation rule, an integration or an AI agent, so the admin can tell which actor caused the problem. | Epic story ROLL-101; release notes "Actor view"; demo notes (admin opened Actor view, picked the agent and a time window, saw the full list of changes) | Jira admin |
| Blast radius preview (ROLL-102) | See exactly which issues, fields and projects will change back, and which will stay as they are, before restoring anything. | Epic story ROLL-102; release notes "Blast radius preview"; demo notes | Jira admin; IT or security leader |
| Selective rollback (ROLL-103) | Undo all changes by one actor in a time window, or pick specific issues or fields. No whole-site restore needed. | Epic story ROLL-103; release notes "Selective rollback" | Jira admin |
| Keep human work (ROLL-104) | Keep the changes people made after the bad event. In the demo, edits the presenter made as a person after the bad event were still in place after the rollback. | Epic story ROLL-104; release notes "Keep human work"; demo notes | Jira admin |
| Audit log (ROLL-105) | Have each rollback recorded with who ran it, what changed and when. Export is available. The epic says exportable for auditors. | Epic story ROLL-105; release notes "Audit log"; demo notes (entry shown and exported) | IT or security leader |

Scale example in the epic and demo: an agent reclassifies 4,000 issues, or an automation overwrites a custom field across 30 projects. These are illustrations the handoff uses, not measured results.

### Limitations

1. Only changes made after the customer's first Rewind backup can be rolled back. | Must say: yes
2. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. | Must say: yes. The exact wording is an open item, see "Where the closed beta handoff and context/ disagree".
3. It works on Jira Cloud only. Confluence is not in this build. | Must say: yes, wherever platform coverage is mentioned.
4. Beyond issues and fields, the handoff does not confirm which Jira data types can be rolled back. | Must say: yes. Copy must not say or imply "every change" or "everything" without this caveat. [NEED PROOF: confirmed list of rollback-able Jira data types]
5. Rollback of a field that a person edited after the agent changed it is not covered in the beta tests and is not decided. | Must say: not in customer copy until decided. Do not claim how it behaves. Keep "keep human work" to what the demo showed (separate edits left in place).
6. Behavior on very large sites, above Atlassian's size limits, is unknown. | Must say: do not carry the backup claim about large sites over to this feature.
7. Who is allowed to run a rollback is not settled. | Must say: do not state a permission model. [NEED PROOF: who can run a rollback]
8. How Actor view tells apart a person, a rule, an integration and an AI agent is not documented. | Must say: do not explain how detection works.

Limitations 1 and 2 are stated by the handoff as known limitations. Limitations 3 to 8 are stated or implied by the handoff (not in this build, open Slack items). All are recorded here so later agents repeat them and do not widen the claim.

### Availability

- Plans: included in Rewind's Jira Cloud backup plans at the [NEED PROOF: plan names and pricing] tier. Until pricing confirms, the only safe wording from the handoff is "a specific plan tier". Owner: Pricing and packaging.
- Platforms: Jira Cloud first.
- Date: [NEED PROOF: GA date]. Current status is closed beta, heading to GA.
- Not committed: Confluence is on the roadmap, no date committed. Do not turn this into a promise. Legal asked to review any Confluence mention before it goes public.

### Dependencies

- Pricing and packaging: plan name and price.
- Rewind's Jira Cloud backup: rollback is limited to changes after the customer's first Rewind backup, and deleted attachments come from the most recent backup. The customer needs Rewind backup running on the site.
- Legal: review of the words "exportable for auditors" and any Confluence mention before they go public.
- Support: plain wording for the attachment limitation before GA (requested in the demo).
- Engineering: documentation of how Actor view separates actor types; a decision on the person-edited-after-agent case.
- Customer success: decision on who may run a rollback.
- Product manager, Jira: confirmation of which data types can be rolled back.
- Revenue operations: CRM capture of "AI governance cited as a buying reason" (needed to measure the proposed pipeline metric).
- Customer permission: any external use of beta numbers or quotes needs customer agreement first. Customers have not agreed.

## What closed beta customers said

> Status of this feedback: **MOCK.** The handoff labels the beta stats and the customer feedback as invented for the demo, not from real customers. Internal evidence from a small group. Not an approved proof point. Any external use is `[NEED PROOF: approval to use closed beta results or quotes]`. Nothing in this section proves a capability exists. Capabilities are only established in "What's built".

### Beta numbers

| Measure | Value | Sample and period | Source in handoff |
|---|---|---|---|
| Beta accounts invited | 14 | 6 weeks (mock) | Section 4 |
| Beta accounts with Agent Rollback enabled | 11 | 11 of the 14 invited | Section 4 |
| Accounts that opened Actor view | 9 of 11 | 11 enabled accounts | Section 4 |
| Accounts that ran a blast radius preview | 7 of 11 | 11 enabled accounts | Section 4 |
| Accounts that ran at least one rollback | 5 of 11 | 11 enabled accounts | Section 4 |
| Total rollbacks run | 23 | 11 enabled accounts, 6 weeks | Section 4 |
| Rollbacks on actors that were AI agents | 8 of 23 | 23 rollbacks | Section 4 |
| Rollbacks on actors that were automation rules | 12 of 23 | 23 rollbacks | Section 4 |
| Rollbacks on actors that were integrations | 3 of 23 | 23 rollbacks | Section 4 |
| Accounts that exported the audit log | 4 of 11 | 11 enabled accounts | Section 4 |
| Company types in the beta | Financial services, healthcare, manufacturing, software | Beta group | Section 4 |

Notes for later agents:
- The sample is 11 enabled accounts, mock, internal. The handoff itself says "small group, internal, not for external use". Do not turn these into percentages for public use, rates, averages or time saved. No time-saved, restore time or ROI figure exists in the handoff.
- The handoff does not say how accounts were chosen, whether they were typical, or what the rollbacks were about.
- The handoff does not report how many of the 5 accounts that ran a rollback were the same accounts behind the 23 rollbacks. Do not infer a per-account figure.

### Who got the most value

The handoff does not measure value. From the feedback only (mock):
- Jira admins who deal with bad changes from automation rules (financial services, manufacturing, healthcare).
- A platform lead rolling out AI agents at a software company, who needs an answer for security.
- A head of IT in healthcare who wants a recovery plan before approving an AI rollout.

Usage split (mock): automation rules were the actor in 12 of 23 rollbacks, AI agents in 8 of 23, integrations in 3 of 23. The product pitch centres on AI agents, but in this small beta more rollbacks were on automation rules. A healthcare admin said the same (quote below).

### The language customers used

All quotes are mock, attributed to roles only.
- The problem, before: "Before this, if a rule went wrong I had two choices: restore the whole site and lose everyone's work, or sit there fixing it by hand. I used to dread that call." (Jira admin, financial services)
- The preview: "I picked the rule, picked the window and saw what would change back. Nothing was a surprise." (Jira admin, financial services)
- Keeping people's work: "The part that sold my team was that people's changes after the mistake were still there." (Jira admin, manufacturing)
- The type of event: "the bad Tuesday when one automation rule overwrote a field across a bunch of projects." (Jira admin, manufacturing)
- The security question: "the first question from security is always what happens when one gets it wrong. Now I have an answer I can show them." (Platform lead running AI agents, software company)
- Approval: "I did not want to be the person who slowed down the agent rollout. This lets us say yes." (Platform lead running AI agents, software company)
- Recovery plan: "I need a recovery plan before I approve an AI rollout. The preview and the audit log are what I would attach to the approval." (Head of IT, healthcare)
- Rules over agents: "Most of my bad changes come from rules, not from agents." (Jira admin, healthcare)

Before the beta, accounts said they had been fixing bad changes by hand, restoring the whole site, or doing nothing (mock, summarized by Product).

### What they compared it to

- The native site restore: "We compared it to the native site restore. That is built for a disaster. This is for the bad Tuesday..." (Jira admin, manufacturing, mock). This is one customer's view. It is not a sourced claim about Atlassian's tool.
- Restoring the whole site, fixing by hand, or doing nothing (accounts' practice before the beta, mock).

### Friction and requests

- Confluence: four beta accounts asked for the same thing on Confluence (mock).
- First-backup limitation: two accounts did not understand at first that only changes after the first Rewind backup can be rolled back (mock).
- Attachments: a healthcare admin had a deleted attachment come back from the last backup, "so it was not the latest version" and wished that were clearer in the product (mock). This is a customer observation of the limitation. It adds no detail on how restore works.
- Permissions: the head of IT in healthcare said, "I want to know exactly who can run a rollback." (mock). This matches the open item on who may run a rollback.
- Audit log export: two accounts did not use it (mock). Four of 11 did export it.
- Demo room questions, not answered: who may run a rollback, what happens if a person edited the same field the agent changed, whether it works on very large sites.

## Beta to GA

- All five stories are "Done, in beta". The handoff does not say what, if anything, changes at GA. Treat the beta build as what is known, not as a GA guarantee.
- Open in the Slack thread, nothing resolved here:
  - Attachment wording (see disagreements below).
  - Whether the claim "Atlassian native has no actor-based rollback" can be made.
  - How Actor view separates a person, a rule, an integration and an AI agent (not documented).
  - Rollback of a field a person edited after the agent (not covered in beta tests, not decided).
  - Who may run a rollback (admin only, or other roles).
  - Which Jira data types beyond issues and fields can be rolled back.
  - Behavior on sites above Atlassian's size limits.
  - Legal review of "exportable for auditors" and any Confluence mention.
  - Plan name and price.
  - Whether beta numbers or quotes can be used externally.
  - CRM capture of "AI governance cited as a buying reason".
- The six-week beta is a small group of 11 enabled accounts. Behavior at GA scale, on large sites, and with roles beyond the beta users is untested in the handoff.
- Success metrics are proposed only. None has a baseline or target.

## Gaps (need an answer before launch)

| Gap | Why it matters | Who can answer |
|---|---|---|
| [NEED PROOF: GA date] | Sets every date. | Product manager, Jira |
| [NEED PROOF: plan names and pricing] | Buyer's next step and expansion goal. | Pricing and packaging |
| [NEED PROOF: source for "Atlassian native Backup and Restore has no actor-based rollback"] | The handoff states it, Sales Engineering asked for a source, and none is on file. Do not use it in any asset until sourced. | Sales Engineering, Product manager, Jira |
| [NEED PROOF: competitor capability check for other third-party backup tools] | Blocks any "only Rewind" style claim. | Product marketing, Sales Engineering |
| [NEED PROOF: approval to use closed beta results or quotes] | Customers have not agreed. No customer proof exists for launch today. | Customer success (customer agreement), then Product marketing and Legal |
| [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase] | Support asked for it. See disagreement 1. | Support lead, Product manager, Jira, Engineering lead |
| [NEED PROOF: how Actor view identifies person, rule, integration and AI agent] | Any claim about identifying AI agents depends on it. | Engineering lead |
| [NEED PROOF: behavior when a person edited the same field the agent changed] | Sits next to the "keep human work" claim. | Engineering lead, Product manager, Jira |
| [NEED PROOF: who can run a rollback] | IT and security buyers ask first. | Customer success, Product manager, Jira |
| [NEED PROOF: confirmed list of rollback-able Jira data types beyond issues and fields] | Limits what "every change" can mean. | Product manager, Jira |
| [NEED PROOF: behavior on sites above Atlassian's size limits] | Cannot reuse the backup large-site claim. | Sales Engineering, Engineering lead |
| [NEED PROOF: Legal approval of "exportable for auditors" and any Confluence mention] | Compliance and roadmap wording risk. | Legal |
| [NEED PROOF: any outcome measure, such as time saved, restore time or issues recovered] | None in the handoff. Nothing of this kind may be stated. | Product manager, Jira (would need to be measured) |
| [NEED PROOF: what the audit log contains beyond who ran it, what changed and when, and what export format is offered] | Handoff states only those three fields and that export is available. | Product manager, Jira |
| [NEED PROOF: how a customer turns the feature on, and whether it needs setup] | Not stated. A launch asset may need a next step. | Product manager, Jira |
| [NEED PROOF: CRM capture of "AI governance cited as a buying reason"] | Pipeline metric cannot be measured. | Revenue operations |

## Where the closed beta handoff and context/ disagree

1. **Attachment recovery wording.** Handoff (release notes): deleted attachments are restored "from the most recent backup, which may be up to 24 hours old". `context/company.md` and `context/proof-points.md` (public, Rewind blog, Apr 2026): Rewind supports "recovery points under 24 hours". The two can read as a conflict, and the handoff's Slack thread asks which to use for Agent Rollback. **Flagged, not resolved.** A human (Support lead, Product manager, Jira, Engineering lead) must decide. Until then, later agents must not use "under 24 hours" for Agent Rollback's attachment restore and must not explain how restored attachments relate to deletion time. Use only the handoff wording and add `[NEED PROOF: ...]`.
2. **"No actor-based rollback" in Atlassian's native tool.** Handoff (competitive notes): Atlassian's native Backup and Restore "works at the site level and has no actor-based rollback". `context/company.md` says only that the native tool is built for full-site recovery, and that Rewind sits on top of it. No source for the "no actor-based rollback" part is on file, and Sales Engineering asked whether it is a belief or a fact. **Flagged, not resolved.** Later agents may use the site-level framing that `context/company.md` supports. They must not state "no actor-based rollback" as fact. Voice rule: never imply Atlassian is unreliable.
3. **Large sites.** `context/proof-points.md` says Rewind covers Jira and Confluence sites above Atlassian's native size limits (backup). The handoff does not say Agent Rollback does. **Flagged, not resolved.** Do not carry the backup claim over to this feature.
4. **"Every change" and "any time window".** The epic says rollback finds and undoes "every change" "across any time window". The release notes limit this to changes after the customer's first Rewind backup, and the data types beyond issues and fields are unconfirmed. Both statements are recorded. Copy must carry the limitations next to either phrase. A human must decide how far the wording can go.
5. **Single-item restore.** `context/proof-points.md` says Rewind restores a single ticket, page, file or configuration. The handoff describes Agent Rollback as restoring by actor, across many items. These are different capabilities. Do not use the single-ticket proof point as evidence for actor-based rollback.
