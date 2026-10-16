# Positioning: Agent Rollback for Jira

**Builds on:** 01-launch-brief.md, 02-launch-context.md, 03-audience.md | **Method:** Obviously Awesome, six parts in order | **Launch date:** [NEED PROOF: GA date]

> Closed beta feedback is MOCK, internal and from a small group (11 enabled accounts). It shapes this analysis. It is not approved proof. Any beta number or quote used outside the team is [NEED PROOF: approval to use closed beta results or quotes]. "Customers compared it to X" describes how they see the alternatives. It is not a verified claim about X. Agent Rollback is a hypothetical product from a mock handoff.

## 1. Competitive alternatives

Starting point: what closed beta accounts said they used before or compared it to (restore the whole site, fix by hand, do nothing, and the native site restore). Then what `context/company.md` supports.

| Alternative | Why customers pick it | Where it stops | Source |
|---|---|---|---|
| Do nothing | No time, no tool, no one owns it. The bad change stays until someone notices the damage. | The wrong values stay in issues and fields across projects. In closed beta, some accounts said they had done nothing before. | Closed beta feedback (mock): accounts' practice before beta |
| Fix it by hand | Needs no new tool. The admin controls each edit. A financial services admin described the choice as restoring the whole site or "sit there fixing it by hand", and said they "dreaded that call". | Slow when one actor touched many issues or projects. The handoff's scale examples are an agent reclassifying 4,000 issues or a rule overwriting a custom field across 30 projects. These are illustrations, not measured results. | Closed beta feedback (mock); handoff epic and demo notes |
| Restore the whole site | Gets the data back. It is the one recovery path many admins know. | Per the same admin, it means losing everyone's legitimate work since the backup. Customers described this as "lose everyone's work". | Closed beta feedback (mock) |
| Atlassian native Backup and Restore | It comes with the platform. Customers compared it to Agent Rollback: a manufacturing admin said, "We compared it to the native site restore. That is built for a disaster. This is for the bad Tuesday." | `context/company.md` says the native tool is built for full-site recovery. Beyond that, no sourced statement on what it can or cannot do. Rewind sits on top of it and does not replace it. | `context/company.md`; closed beta feedback (mock). One customer's view, not a sourced claim about Atlassian's tool |
| Rewind single-item restore (today's Rewind) | Restores one ticket, page, file or configuration without a full-site restore. | It restores one item at a time. Agent Rollback works by actor across many items. These are different capabilities. | `context/company.md`; `context/proof-points.md`; 02, disagreement 5 |
| Other third-party backup tools | Not covered by closed beta feedback. | [NEED PROOF: competitor capability check for other third-party backup tools] | None on file |

Notes:
- The strongest alternative in the feedback is not a vendor. It is the choice between "restore everything" and "fix it by hand". Messaging should be set against that choice.
- Atlassian is not treated as unreliable. The frame is shared responsibility: the platform protects its own infrastructure, and the customer owns the effect of their own rules, integrations and agents (`context/company.md`, core idea).

## 2. Unique attributes

Taken from the five built capabilities in the handoff (02, "What's built"). "Alternatives that lack it" only holds where a source supports it. Where no source exists, the attribute is "not yet confirmed as unique".

| Attribute | Alternatives that lack it | Confirmed? | Source |
|---|---|---|---|
| Actor view: changes grouped by who or what made them (person, automation rule, integration, AI agent) | Whole-site restore and doing it by hand work from the site or the item, not from the actor that made the change. Native tool: works at the site level. Other tools: unknown. | Partly. It is a confirmed capability of Agent Rollback. It is not yet confirmed as unique against the native tool or other vendors. [NEED PROOF: source for native tool capability; competitor capability check] | Handoff ROLL-101; `context/company.md` |
| Blast radius preview: see which issues, fields and projects will change back and which will stay, before restoring | Fix by hand and whole-site restore give no equivalent view in the beta accounts' account of their old practice. | Not yet confirmed as unique. Confirmed as a capability. [NEED PROOF: competitor capability check] | Handoff ROLL-102 |
| Selective rollback: undo one actor's changes in a time window, or pick specific issues or fields, with no whole-site restore | Whole-site restore (by definition restores the site). Native tool: works at the site level. Rewind single-item restore works on one item at a time. | Partly. The difference from whole-site restore and single-item restore is sourced. Uniqueness against other vendors is not. | Handoff ROLL-103; `context/company.md` |
| Keep human work: changes people made after the bad event stay in place | Whole-site restore (per the beta admin: lose everyone's work). | Not yet confirmed as unique. Shown in the demo for separate edits only. Behavior when a person edited the same field the agent changed is not decided. [NEED PROOF: behavior when a person edited the same field the agent changed] | Handoff ROLL-104; demo notes |
| Audit log: each rollback recorded with who ran it, what changed and when, with export | Doing it by hand leaves no such record unless the admin builds one. | Not yet confirmed as unique. Contents beyond the three fields and the export format are unknown. [NEED PROOF: audit log contents and export format; Legal approval of "exportable for auditors"] | Handoff ROLL-105 |

What is most likely to hold up as distinct: the combination. One actor, one window, preview first, human work left alone, recorded. Whether any other tool offers that combination is [NEED PROOF: competitor capability check].

## 3. Value and proof

Value is written in the words closed beta customers used. Those quotes are mock and internal. They shaped the wording here. They are not approved proof and must not appear in customer-facing assets. [NEED PROOF: approval to use closed beta results or quotes]

| Attribute | Value to the customer (in their words) | Proof | Source |
|---|---|---|---|
| Actor view | Know which actor caused the problem, so the admin is not guessing. The "bad Tuesday when one automation rule overwrote a field across a bunch of projects" becomes one thing to find. | Capability is established by the handoff (ROLL-101, demo). Outcome proof: none. How Actor view tells a person, rule, integration and AI agent apart is not documented. [NEED PROOF: how Actor view identifies person, rule, integration and AI agent] | Handoff; closed beta (mock) |
| Blast radius preview | "Nothing was a surprise." Admin picks the rule and the window and sees what would change back before anything does. | Capability: handoff ROLL-102 and demo. No outcome measure. | Handoff; closed beta (mock) |
| Selective rollback | Escape the two bad options: restore the whole site and "lose everyone's work", or "sit there fixing it by hand". Undo the one change, not the whole site. | Capability: handoff ROLL-103. Single-ticket restore in `context/proof-points.md` is a different capability and is not proof for this. No time-saved or restore-time figure exists. [NEED PROOF: any outcome measure] | Handoff; closed beta (mock); `context/voice.md` |
| Keep human work | "People's changes after the mistake were still there." The part that sold one team. | Demo: edits made by a person after the bad event were still in place. Limit: same-field case not decided. [NEED PROOF: behavior when a person edited the same field the agent changed] | Handoff demo notes; closed beta (mock) |
| Audit log | Give security something to attach to an approval: "The preview and the audit log are what I would attach to the approval." Gives a platform lead an answer to "what happens when one gets it wrong". | Capability: handoff ROLL-105 and demo (entry shown and exported). "Exportable for auditors" needs Legal review. [NEED PROOF: Legal approval of "exportable for auditors"] | Handoff; closed beta (mock) |

Limits that travel with every value claim (02, limitations):
- Only changes made after the customer's first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
- Jira Cloud only. Confluence has no committed date.
- Data types beyond issues and fields are unconfirmed. [NEED PROOF: confirmed list of rollback-able Jira data types]
- Who can run a rollback is not settled. [NEED PROOF: who can run a rollback]
- Large-site behavior is unknown. [NEED PROOF: behavior on sites above Atlassian's size limits]

Approved proof that supports the surrounding story (not the feature itself): protects 16 cloud applications, trusted by more than 25,000 organizations, customers in financial services, healthcare and manufacturing (`context/proof-points.md`). Backups stored independently of the vendor platform is also approved, but it is a backup claim and should not be stretched to rollback.

## 4. Best-fit customers

Started from who got the most value in closed beta (mock, small sample), then checked against 03-audience.md and steps 1 to 3.

**Who cared most:**
- Jira admins cleaning up after bad changes from automation rules, in financial services, manufacturing and healthcare. They had been stuck between restoring the site and fixing by hand, and they valued the preview and keeping people's work.
- A platform lead rolling out AI agents at a software company, who needed an answer for security.
- A head of IT in healthcare who wanted a recovery plan before approving an AI rollout, and named the preview and audit log as what they would attach.

**What the best-fit account looks like (observable signals):**
- Jira Cloud site with Rewind backup already running. Rollback depends on the first backup.
- Heavy automation: many rules, bulk changes or integrations that touch several projects. An admin who talks about rules overwriting fields.
- A pilot or planned rollout of AI agents in Jira Cloud that needs IT or security sign-off.
- Regulated industry where audit evidence matters.
- The admin is the champion. The IT or security leader approves and wants the recovery plan and audit log.

**Refinement from steps 1 to 3:** The value comes from the gap between "restore everything" and "fix it by hand". So the best fit is not defined by AI alone. It is any site where one actor can change many things and the admin must undo only that. In this small beta, more rollbacks were on automation rules (12 of 23) than AI agents (8 of 23), and a healthcare admin said most bad changes come from rules. That is a reason to lead with "the one actor that went wrong", with AI agents as the growing case. It is not a market finding. [NEED PROOF: share of bad changes from rules versus agents]

**Who is not a fit for this launch:**
- Teams without Rewind backup on Jira Cloud. They need the backup story first.
- Confluence-only admins. Four beta accounts asked for Confluence (mock). No date is committed.
- Sites above Atlassian's size limits or needing data types beyond issues and fields. Not a confirmed fit. Ask first.
- Buyers who want time-saved or ROI proof. None exists.

## 5. Market category

- **Options considered:**
  1. *SaaS backup and recovery for Jira.* The category Rewind already sells in. Customers know it. It links to the backup the feature depends on.
  2. *AI agent governance or AI safety tooling.* Matches the head of IT's "recovery plan before I approve an AI rollout". It would also pull the product away from the admin's real problem (rules and integrations too) and into a space with no basis in our sources.
  3. *Jira change management or audit tooling.* Speaks to the audit log and the preview, but under-describes the undo and has no source in `context/`.
- **Chosen frame:** Backup and recovery for Jira Cloud, specifically recovery from the bad change of one actor: selective recovery by actor, as a part of Rewind's Jira Cloud backup. Describe the recovery job in plain words ("undo what one rule, integration or AI agent changed"). Do not coin a new category name.
- **What it makes customers assume:**
  - Good: it is a safety net the admin owns, it sits on top of the platform's own tool, it restores data, and it is part of a backup customers already trust. It fits the shared responsibility idea in `context/company.md`.
  - Bad: that it restores everything, like backup does. The limits cut against that: only changes after the first Rewind backup, attachments from the most recent backup, Jira Cloud only, and unconfirmed data types. Customers may also assume it is "just backup" and miss the actor, preview and keep-human-work parts.
- **Risk:** The frame may undersell the new part. Mitigation: the messaging leads with the moment of failure and the escape from the two bad options, then names the capability. A second risk is that "AI agent" in the category name hides the rule and integration cases that dominated the beta. Keep the frame on the actor, not on AI alone.

## 6. Relevant trends

Only from `context/company.md` or the handoff.

- **AI agents now act directly on SaaS data, which creates new rollback and recovery needs.** Source: `context/company.md`, growth driver 3 (CEO Mike Potter, Aug 2026). Why it matters now: the failure being solved is one actor changing many things at once, and AI agents add more such actors.
- **SaaS vendors protect their own infrastructure, not the customer's own mistakes, integrations, automations or AI agents.** Source: `context/company.md`, core idea. Why it matters now: it gives the shared responsibility frame without blaming Atlassian.
- **Security and IT leaders want a recovery plan before they approve an AI rollout.** Source: the handoff's pipeline logic (01-launch-brief.md) and one head of IT in closed beta (mock). Why it matters now: the preview and audit log give the approver something to point to. How often AI governance is a buying reason is unknown. [NEED PROOF: how often AI governance is a buying reason; CRM capture]
- **The Atlassian cloud migration** (growth driver 1, `context/company.md`). The product is Jira Cloud only, so it touches this driver. The handoff does not make the case, so the link is untested. Do not build messaging on it.

No market size, adoption rate or incident statistic is used. None is in the sources.

## What this means for messaging

1. **Lead with the two bad options, then the way out.** Restore the whole site and lose everyone's work, or fix it by hand. Undo the one actor's changes instead. Headline says what the admin gets back, not the feature name.
2. **See it before you change it.** The preview is the trust builder for both the admin and the approver. Say what will change back and what will stay.
3. **Keep people's work.** Say it as the demo showed it: separate edits by people after the bad event stay in place. Do not claim how same-field edits behave.
4. **Name the actor broadly.** One rule, integration or AI agent. AI is the reason the safety net matters, never the problem. For the approver, add the recovery plan and audit log framing, with Legal wording for "exportable for auditors".

Every asset carries the limits next to the claim: changes after the first Rewind backup only, attachments restored from the most recent backup (handoff wording only), Jira Cloud only. No "every change" without the data type caveat. No outcome figures. No claim that Atlassian's native tool lacks anything: say it works at the site level, and that Rewind sits on top of it. No claims about other third-party tools. No beta numbers or quotes outside the team.

## Open questions

- Source for what Atlassian's native tool can and cannot do for actor-level recovery. Until then, site-level framing only. [NEED PROOF: source for native tool capability]
- Competitor capability check, to decide whether any "only" or "first" claim is possible. [NEED PROOF: competitor capability check]
- Approval to use closed beta results or quotes externally. [NEED PROOF: approval to use closed beta results or quotes]
- Plain wording for the attachment limitation. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
- How Actor view tells actor types apart, and the same-field edit case. [NEED PROOF: how Actor view identifies person, rule, integration and AI agent; behavior when a person edited the same field the agent changed]
- Who can run a rollback, and which data types can be rolled back. [NEED PROOF: who can run a rollback; confirmed list of rollback-able Jira data types]
- Do rules matter more than agents beyond this beta? [NEED PROOF: share of bad changes from rules versus agents]
- Plan names and pricing. [NEED PROOF: plan names and pricing]
