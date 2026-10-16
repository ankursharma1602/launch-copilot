# Messaging: Agent Rollback for Jira

**Builds on:** 02-launch-context.md, 03-audience.md, 04-positioning.md | **Launch date:** [NEED PROOF: GA date]

> Agent Rollback is a hypothetical product from a mock handoff. Closed beta numbers and quotes are mock, internal evidence. They informed the wording here. Nothing below quotes them or uses their numbers. Any customer-facing use of beta results or quotes is [NEED PROOF: approval to use closed beta results or quotes].

## Core message

When a rule, an integration or an AI agent changes issues it should not have, Agent Rollback lets a Jira Cloud admin undo just what that one actor changed, see the effect first, and leave people's work alone, with every rollback recorded.
Support: Capabilities are established by the closed beta handoff (Actor view, blast radius preview, selective rollback, keep human work, audit log). Outcome proof: [NEED PROOF: any outcome measure, such as time saved or restore time]. Surrounding company proof that is approved: Rewind protects 16 cloud applications and is trusted by more than 25,000 organizations (`context/proof-points.md`). That supports the company, not this feature.

## Value pillars

| Pillar | Claim | Proof | Source |
|---|---|---|---|
| 1. Undo the one actor, not the whole site | Pick the rule, integration or AI agent that went wrong and a time window. Undo its changes, or pick specific issues or fields. Changes people made after the bad event stay in place. No whole-site restore. | Capability: handoff ROLL-101, ROLL-103, ROLL-104 and demo notes (separate edits by a person after the bad event were still in place). Limit: same-field edits are not decided, so say only "separate edits stay". No outcome figure. [NEED PROOF: any outcome measure] [NEED PROOF: behavior when a person edited the same field the agent changed] [NEED PROOF: how Actor view identifies person, rule, integration and AI agent] | 04 section 3 (Actor view, Selective rollback, Keep human work); 02 "What's built" |
| 2. See it before it changes | Before anything is restored, see which issues, fields and projects will change back and which will stay as they are. | Capability: handoff ROLL-102 and demo notes. No outcome measure. Customer reaction to the preview is mock beta evidence: [NEED PROOF: approval to use closed beta results or quotes] | 04 section 3 (Blast radius preview) |
| 3. A record you can hand to security | Each rollback is logged with who ran it, what changed and when, and the log can be exported. This gives the approver something to attach to an AI rollout sign-off. | Capability: handoff ROLL-105 and demo notes (entry shown and exported). Use "can be exported" until Legal clears "exportable for auditors". [NEED PROOF: Legal approval of "exportable for auditors"] [NEED PROOF: what the audit log contains beyond who ran it, what changed and when, and the export format] | 04 section 3 (Audit log) |

Pillar order: 1 and 2 carry the admin. Pillar 3 carries the IT or security leader. Pillar 3 is the claim the approver acts on, so it stays in the kit even though it is not the lead.

## Angles by persona

### The Atlassian admin (primary)
- **Lead with:** The moment of failure and the two bad options: restore the whole site and lose your team's work since the backup, or fix it by hand, issue by issue. Then the way out: undo the one actor's changes.
- **Pillar:** 1 first, then 2.
- **Words to use:** roll back, undo, restore, automation rule, integration, AI agent, bulk change, blast radius, issues, fields, projects, time window, "the one actor that went wrong". Scale illustrations may be used only as scenarios, for example "an automation rule overwrites a custom field across 30 projects" or "an agent reclassifies 4,000 issues". Label them as examples, not results.
- **Proof to use:** Handoff capabilities (Actor view, preview, selective rollback, keep human work). Company proof only as a trust line. Customer quotes and beta numbers: none. [NEED PROOF: approval to use closed beta results or quotes]
- **Avoid:** Leading with AI alone (rules and integrations are the actor too, and AI is the growing case). "Every change" or "undo everything" without the data type caveat. Any claim about same-field edits. Fear-mongering and vague reassurance. Any claim about what Atlassian's native tool lacks. Any permission model.

### The IT or security leader (secondary)
- **Lead with:** The question they ask before approving AI agents: what happens when one gets it wrong? Answer: the admin can see the effect before restoring, undo only that actor's changes, and the rollback is recorded.
- **Pillar:** 3 first, then 2.
- **Words to use:** recovery plan, audit log, record of who ran it, what changed and when, exported, shared responsibility. Frame AI as the reason the safety net matters.
- **Proof to use:** Handoff ROLL-102 and ROLL-105 capabilities. Company-level proof for trust (25,000 organizations, customers in financial services, healthcare and manufacturing). No "recovery plan" outcome claim. [NEED PROOF: how often AI governance is a buying reason]
- **Avoid:** Stating who can run a rollback. [NEED PROOF: who can run a rollback] "Exportable for auditors" before Legal clears it. Compliance or certification language, and anything that implies the audit log satisfies a regulation. Framing the AI or automation owner as the problem. Giving this persona their own campaign: the admin carries the message to them.

## Must say (limitations every asset repeats)

Use the wording below. Short assets keep items 1 to 4 at minimum. Write them into the draft first, then cut other words.

1. **First backup.** "Agent Rollback can undo changes made after your first Rewind backup." Not "any time window" or "anything that happened" without this.
2. **Attachments.** "Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old." This is the handoff wording only. Do not explain how restored attachments relate to deletion time. Do not use "under 24 hours" or any recovery point claim next to it. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase] (Support lead, Product manager Jira and Engineering lead own the final wording.)
3. **Platform.** "Agent Rollback works on Jira Cloud." If Confluence comes up, the only line is: "Confluence is on the roadmap. No date is committed." This Confluence line needs sign-off from Legal before it goes public. [NEED PROOF: Legal approval of any Confluence mention] Do not add a date, a quarter or "coming soon".
4. **Plan.** "Included in Rewind's Jira Cloud backup plans at a specific plan tier." Do not name the tier or a price. [NEED PROOF: plan names and pricing] Customers need Rewind backup running on their Jira Cloud site.
5. **Scope of "every change".** Do not write "every change" or "everything" unless the data type caveat sits next to it: the handoff confirms issues and fields only. [NEED PROOF: confirmed list of rollback-able Jira data types]
6. **Keep human work.** Say only what the demo showed: separate edits people made after the bad event stay in place. Do not say how it behaves when a person edited the same field the agent changed. [NEED PROOF: behavior when a person edited the same field the agent changed]
7. **Do not state:** a permission model [NEED PROOF: who can run a rollback]; how Actor view tells a person, rule, integration and AI agent apart [NEED PROOF: how Actor view identifies person, rule, integration and AI agent]; large-site behavior, and do not carry the backup claim about sites above Atlassian's size limits over to this feature [NEED PROOF: behavior on sites above Atlassian's size limits]; any time saved, restore time or ROI figure [NEED PROOF: any outcome measure]; how a customer turns it on [NEED PROOF: how a customer turns the feature on, and whether it needs setup].

## Vocabulary

- **Use:** undo, roll back, restore, the one actor that went wrong, rule, integration, AI agent, issues, fields, projects, time window, preview, what will change back and what will stay, people's changes stay in place, audit log, recorded, can be exported, Jira Cloud, after your first Rewind backup, shared responsibility, "Undo the one change, not the whole site."
- **Avoid:**
  - Banned words (`context/voice.md`): peace of mind, game-changer, revolutionary, seamless, cutting-edge, best-in-class, unlock, supercharge, leverage (as a verb), robust, effortless, world-class, next-generation, synergy, disrupt.
  - Em dashes and exclamation marks.
  - Terms the positioning rules out: "Atlassian has no actor-based rollback" or any claim that the native tool lacks something (say it works at the site level and Rewind sits on top of it); "only", "first" or "no other tool" claims; any claim about other third-party backup tools; "under 24 hours" next to Agent Rollback; "every change" or "undo everything" without the caveat; "exportable for auditors" until Legal clears it; "AI safety" or "AI governance" as a category name (the frame is backup and recovery for Jira Cloud, by actor); verbatim customer quotes and any beta number; words that imply Atlassian is unreliable; words that blame AI or automation owners.

## Headline check

Headlines say what the admin gets, not the feature name. Candidates below are for the copywriter. None uses beta evidence.

| Candidate headline | Passes? | Note |
|---|---|---|
| Undo what one rule, integration or AI agent changed. Keep everything else. | Yes | Gets back control. "Everything else" must be followed by the limits in body copy. Check against Must say 5 in long form. |
| Undo the one change, not the whole site. | Yes | From the voice file's preferred patterns. |
| See what will change back before you restore anything. | Yes | Pillar 2. |
| Give security a record of every rollback. | Yes | Pillar 3. Here "every rollback" means rollbacks the product logs, not "every change". |
| Your team's work stays when you roll back one actor. | Yes with limit | Only as the demo showed: separate edits stay. Keep Must say 6 close by. |
| Introducing Agent Rollback with Actor view, blast radius preview and selective rollback. | No | Feature names, not what the customer gets. |
| Roll back every AI agent change in Jira. | No | "Every change" without caveat, and AI-only framing. |
| The only way to roll back by actor. | No | "Only" claim has no source. [NEED PROOF: competitor capability check] |
| Rollback in minutes, not days. | No | Time claim, no outcome figure exists. [NEED PROOF: any outcome measure] |

## Traceability

| Message | Comes from (04-positioning.md section) |
|---|---|
| Core message: two bad options, then undo one actor | What this means for messaging, point 1; section 3 Selective rollback; section 1 notes |
| Pillar 1 | Section 3 (Actor view, Selective rollback, Keep human work); What this means for messaging, points 3 and 4 |
| Pillar 2 | Section 3 (Blast radius preview); What this means for messaging, point 2 |
| Pillar 3 | Section 3 (Audit log); section 6 (security and IT leaders want a recovery plan); What this means for messaging, point 4 |
| Name the actor broadly (rule, integration, AI agent) | Section 4 refinement; section 5 risk |
| Backup and recovery frame, no new category name | Section 5 chosen frame |
| Native tool: site-level only, Rewind sits on top | Section 1 notes; What this means for messaging, closing paragraph |
| Shared responsibility line | Section 6, second trend |
| Must say items 1 to 7 | Section 3 limits list; What this means for messaging, closing paragraph; 02 limitations 1 to 8 |
| Persona angles | 03-audience.md primary and secondary persona; section 4 |

## Positioning gaps found

- **No outcome proof.** Positioning has no time saved, restore time or ROI figure. Pillars rest on capability only. Messages cannot say "faster" or "in minutes". Needs measurement. [NEED PROOF: any outcome measure]
- **No customer proof usable externally.** The strongest value language comes from mock closed beta feedback. Until customers agree, no pillar has a customer proof point. [NEED PROOF: approval to use closed beta results or quotes]
- **Uniqueness unproven.** Positioning rates no attribute as confirmed unique against the native tool or other vendors, so no message claims "only" or "first". [NEED PROOF: source for native tool capability; competitor capability check]
- **"Keep human work" is partial.** Positioning supports separate edits only. The same-field case is open, so the pillar 1 claim stays narrow.
- **Approver message is thin.** Pillar 3 depends on audit log contents, export format and Legal wording, plus an undecided permission model. Positioning does not support a stronger claim to security buyers. [NEED PROOF: what the audit log contains beyond who ran it, what changed and when, and the export format; who can run a rollback]
- **Call to action.** Positioning has no next step for the reader because setup and plan tier are unknown. [NEED PROOF: how a customer turns the feature on, and whether it needs setup; plan names and pricing]
- **Attachment wording conflict unresolved.** The handoff's "up to 24 hours old" and the public "recovery points under 24 hours" can read as a conflict. A human must decide before GA. Until then, only the handoff wording is used.
- **Confluence line needs sign-off.** The roadmap line in Must say 3 is held for Legal.
