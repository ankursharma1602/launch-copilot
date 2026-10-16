# Audience: Agent Rollback for Jira

**Builds on:** 01-launch-brief.md, 02-launch-context.md | **Personas from:** context/personas.md (no new personas added)

> Closed beta feedback is mock, internal and from a small group (11 enabled accounts). It is used here to test the personas, not as proof. Say "in closed beta" when citing it. Nothing from it is approved for customer-facing use. [NEED PROOF: approval to use closed beta results or quotes]

## Primary persona: The Atlassian admin

- **Why primary:** This is the person who runs the rollback and lives with the result. The launch is built for them: find what one actor changed, see the effect first, undo it, leave people's work alone. The brief's problem statement (restore the whole site or fix by hand) is their problem. `context/personas.md` already lists them as the primary user, and closed beta agrees.
- **What closed beta showed:** In closed beta, the clearest value came from Jira admins in financial services, manufacturing and healthcare who were cleaning up after bad changes. Two of the three roles that spoke up about value were admins, and they talked about preview and keeping people's work. This confirms the persona file. One difference: the persona file and the product pitch lean toward AI agents, but in closed beta more rollbacks were on automation rules (12 of 23) than on AI agents (8 of 23), and a healthcare admin said most of their bad changes come from rules. So for this persona, lead with "the one actor that went wrong", whether that is a rule, an integration or an agent. Treat AI agents as the growing case, not the only one. This is a small mock sample, so it is a reason to widen the wording, not a market finding.
- **Trigger moment:** A rule, integration or agent has changed many issues or fields across projects, and the admin now has to decide between restoring the whole site and fixing by hand. In closed beta, customers described this as "the bad Tuesday" when one rule overwrote a field across many projects, and the dread of that call. A second trigger: the company is about to roll out AI agents in Jira Cloud and the admin will be the one asked "what if it goes wrong?"
- **What they own / fear / want:**
  - Owns: uptime, configuration, permissions, automations and increasingly the AI tools wired into Jira (`context/personas.md`).
  - Fears: something breaks at scale and they cannot undo it without losing everyone's legitimate work. They are the person everyone looks at.
  - Wants: a surgical undo, and to know what will change before it changes.
- **Their words:**
  - Closed beta (role-attributed, short phrases only): a financial services admin talked about "two choices" and dreading the call. A second financial services admin said "nothing was a surprise" after the preview. A manufacturing admin said the part that sold the team was that people's later changes stayed in place. A healthcare admin said most bad changes come from "rules, not agents".
  - Persona file: "roll back," "restore," "automation rule," "bulk change," "blast radius," "undo."
- **What turns them off:** Fear-mongering, vague reassurance, copy that does not sound like someone who has run Jira, and any "undo everything" claim that hides the limits. They will check the first-backup limit and the attachment limit, so state both plainly. In closed beta two accounts did not at first understand the first-backup limit, and one admin wanted the attachment limit clearer.

## Secondary persona: The IT or security leader

- **Why:** They approve, and the brief's pipeline logic depends on them: security and IT leaders want a recovery plan before they approve an AI rollout. In closed beta, a head of IT in healthcare said they need a recovery plan before approving, and named the preview and the audit log as what they would attach to the approval. A platform lead at a software company described the same security question. This supports the persona file, but it is one head of IT in a small mock sample. [NEED PROOF: how often AI governance is a buying reason, no CRM capture today]
- **Role in the message:** They get the risk framing (accountability, recovery plan, audit evidence). They do not get a separate campaign. The admin carries the message to them.
- **Watch for:** The same person asked in closed beta who can run a rollback. That is not settled. [NEED PROOF: who can run a rollback]. Do not state a permission model.

## Best-fit segments

All signals are things a salesperson or marketer could observe or ask. Sizes and shares are not sourced. [NEED PROOF: number of Rewind Jira Cloud customers in each segment]

| Segment | Signals to look for | Why they fit | Evidence |
|---|---|---|---|
| Jira Cloud sites with heavy automation | Many automation rules or bulk changes across several projects. Admin talks about rules overwriting fields. | Closed beta rollbacks were mostly on automation rules. The scale example in the handoff is a rule changing a custom field across 30 projects. | Closed beta feedback (mock, small sample); handoff epic and demo notes |
| Teams rolling out AI agents in Jira Cloud | Pilot or planned rollout of AI agents. A platform or productivity lead needs IT or security sign-off. | Growth driver 3 in `context/company.md` (AI usage). In closed beta, a platform lead said the feature gave them an answer for security and let them say yes. | `context/company.md`; closed beta feedback (mock) |
| Regulated industries on Jira Cloud | Financial services, healthcare or manufacturing. Audit readiness named as a concern. | These industries are named customers types in `context/proof-points.md` and were in the closed beta group. The audit log is part of the build. | `context/proof-points.md`; closed beta company types (mock) |
| Existing Rewind Jira Cloud backup customers | Rewind backup already running on the Jira Cloud site. | Rollback only covers changes after the first Rewind backup, and the feature is included in Jira Cloud backup plans at a higher tier. | Handoff limitations and availability. Plan tier: [NEED PROOF: plan names and pricing] |
| Sites with very large size or unusual data types | Sites above Atlassian's size limits, or needs beyond issues and fields. | Not a confirmed fit. Behavior is unknown. Ask first, do not assume. | [NEED PROOF: behavior on sites above Atlassian's size limits]; [NEED PROOF: confirmed list of rollback-able Jira data types] |

## Buying group

| Role | Persona | Part in the decision |
|---|---|---|
| User and champion | Atlassian admin | Runs the rollback, finds the problem, makes the case. Primary audience. |
| Approver | IT or security leader (Head of IT, IT Director, CISO, VP Engineering) | Signs off on the plan tier and on the AI rollout. Wants the recovery plan and audit evidence. Secondary audience. |
| Influencer | AI or automation owner (platform or productivity lead) | Needs approval to deploy agents. Supports the case because this lets them get to yes. No dedicated message in this launch. |
| Pricing gate | Not a persona | Plan tier and price are not set. [NEED PROOF: plan names and pricing] |

## Out of focus for this launch

- **Confluence-only admins and Confluence demand.** The build is Jira Cloud only. Four closed beta accounts asked for Confluence (mock). No date is committed, and Legal must review any mention.
- **The AI or automation owner as a lead audience.** They are in the buying group and can be named as a beneficiary, but the launch does not lead with them. The closed beta signal for them is one platform lead. Never frame them as the problem. They are the person who gets to say yes to AI.
- **Teams without Rewind backup on Jira Cloud.** Rollback depends on the first backup. These buyers need the backup story first, which is not this launch.
- **Data center or non-Atlassian users.** Not in the handoff.
- **Buyers who want proof of time saved or ROI.** No such figure exists. [NEED PROOF: any outcome measure]

## Open questions

- Is the admin-first order right once real customer research is done? Personas are demo personas, inferred from public positioning. Validate before relying on them. [NEED PROOF: customer research]
- Do automation rules matter more than AI agents beyond this small beta? Needs a source beyond mock closed beta feedback. [NEED PROOF: share of bad changes from rules versus agents]
- Who is allowed to run a rollback, and how does the IT or security leader sign off? [NEED PROOF: who can run a rollback]
- Can the closed beta language be used outside the company? Customers have not agreed. [NEED PROOF: approval to use closed beta results or quotes]
- How do we find best-fit accounts in the CRM, given AI governance as a buying reason is not captured? [NEED PROOF: CRM capture of "AI governance cited as a buying reason"]
- Does the admin's trigger differ for AI agents versus rules versus integrations? Actor view detection is not documented, so do not claim how it tells them apart. [NEED PROOF: how Actor view identifies person, rule, integration and AI agent]
