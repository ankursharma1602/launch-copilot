# Closed beta handoff: Agent Rollback for Jira

> HYPOTHETICAL. A mock handoff written to demo Launch CoPilot. Agent Rollback is not a real or announced Rewind product. The closed beta accounts, numbers, quotes and Slack messages below are invented. The feedback is mock, not from real customers.

**From:** Product manager, Jira (role, no name)
**To:** Product marketing
**Status:** Closed beta, heading to GA
**GA date:** [NEED PROOF: GA date]

## 1. Jira epic summary

**Epic (mock key ROLL-100): Agent Rollback for Jira**

Agent Rollback lets Jira admins find and undo every change made by a specific AI agent, automation rule or integration, across any time window, without restoring the whole site or touching changes made by people.

**Problem.** AI agents and automation rules now edit Jira issues at a scale no human does. When one goes wrong, for example an agent reclassifies 4,000 issues or an automation overwrites a custom field across 30 projects, admins today have two bad options: restore the whole site and lose every legitimate change since the backup, or fix things by hand. Native tools restore at the site level, not by actor.

**Who it's for.**
- Primary: Jira Cloud admins at companies using AI agents or heavy automation.
- Secondary: IT and security leaders who must approve AI rollouts and want a recovery plan before they say yes.

**User stories.**

| Story | As a... | I want to... | So that... | Status |
|---|---|---|---|---|
| ROLL-101 Actor view | Jira admin | see every change grouped by who or what made it: a person, an automation rule, an integration or an AI agent | I can tell which actor caused the problem | Done, in beta |
| ROLL-102 Blast radius preview | Jira admin | see exactly which issues, fields and projects will change back, and what will stay as is, before I restore | I am not surprised by the result | Done, in beta |
| ROLL-103 Selective rollback | Jira admin | undo all changes by one actor in a time window, or pick specific issues or fields | I fix the problem without restoring the whole site | Done, in beta |
| ROLL-104 Keep human work | Jira admin | keep the changes people made after the bad event | legitimate work is not lost | Done, in beta |
| ROLL-105 Audit log | IT or security leader | have every rollback recorded with who ran it, what changed and when, exportable for auditors | I can show what happened | Done, in beta |

**Availability.**
- Plans: included in Rewind's Jira Cloud backup plans at the [NEED PROOF: plan names and pricing] tier.
- Platforms: Jira Cloud first. Confluence on the roadmap, no date committed.
- Launch date: [NEED PROOF: GA date]

**Success metrics (proposed).**
- Adoption: % of active Jira customers who open Actor view within 30 days
- Expansion: upgrades to the plan that includes Agent Rollback within 90 days
- Pipeline: new opportunities where AI governance is cited as a buying reason

**Competitive notes.**
- Atlassian's native Backup and Restore works at the site level and has no actor-based rollback.
- Other third-party backup tools: [NEED PROOF: competitor capability check]

## 2. Release notes (engineering, closed beta build)

**Agent Rollback, closed beta build (mock build notes)**

Added
- Actor view: change history grouped by actor type (person, automation rule, integration, AI agent).
- Blast radius preview: lists issues, fields and projects that will change back, and those that will stay as is.
- Selective rollback: roll back all changes by one actor in a chosen time window, or select issues or fields.
- Keep human work: changes made by people after the bad event are left in place.
- Audit log: each rollback is recorded (who ran it, what changed, when). Export is available.

Known limitations
- Only changes made after the customer's first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.

Not in this build
- Confluence. On the roadmap, no date committed.

## 3. Notes from the demo

Internal demo to Product, Sales Engineering and Support (mock notes, roles only).

- Demo opened with an agent that had reclassified 4,000 issues. The admin opened Actor view, picked the agent and a time window, and saw the full list of changes.
- Blast radius preview was the moment the room reacted. It shows which issues, fields and projects change back and which stay as they are, before anything is restored.
- The presenter then made a few edits as a person after the bad event. After the rollback, those edits were still in place.
- The audit log entry for the rollback was shown and exported.
- Questions from the room: who is allowed to run a rollback, what happens if a person edited the same field the agent changed, and whether this works on very large sites. None was answered in the demo. See open questions below.
- Support asked for plain wording on the attachment limitation before GA.

## 4. Closed beta stats

> Mock numbers for the demo. Small group, internal, not for external use.

| Measure | Value |
|---|---|
| Beta period | 6 weeks (mock) |
| Beta accounts invited | 14 |
| Beta accounts with Agent Rollback enabled | 11 |
| Accounts that opened Actor view | 9 of 11 |
| Accounts that ran a blast radius preview | 7 of 11 |
| Accounts that ran at least one rollback | 5 of 11 |
| Total rollbacks run | 23 |
| Rollbacks run on actors that were AI agents | 8 of 23 |
| Rollbacks run on actors that were automation rules | 12 of 23 |
| Rollbacks run on actors that were integrations | 3 of 23 |
| Accounts that exported the audit log | 4 of 11 |
| Company types in the beta | Financial services, healthcare, manufacturing, software |

## 5. Closed beta customer feedback

> MOCK. These are invented for the demo. They are not from real customers. Roles only, no names.

**Jira admin, financial services (mock)**
"Before this, if a rule went wrong I had two choices: restore the whole site and lose everyone's work, or sit there fixing it by hand. I used to dread that call."
"I picked the rule, picked the window and saw what would change back. Nothing was a surprise."

**Jira admin, manufacturing (mock)**
"We compared it to the native site restore. That is built for a disaster. This is for the bad Tuesday when one automation rule overwrote a field across a bunch of projects."
"The part that sold my team was that people's changes after the mistake were still there."

**Platform lead running AI agents, software company (mock)**
"We are rolling out more agents, and the first question from security is always what happens when one gets it wrong. Now I have an answer I can show them."
"I did not want to be the person who slowed down the agent rollout. This lets us say yes."

**Head of IT, healthcare (mock)**
"I need a recovery plan before I approve an AI rollout. The preview and the audit log are what I would attach to the approval."
"I want to know exactly who can run a rollback."

**Jira admin, healthcare (mock)**
"I did not expect to use it for automation rules this much. Most of my bad changes come from rules, not from agents."
"We had one deleted attachment that came back from the last backup, so it was not the latest version. I wish that were clearer in the product."

**Other feedback themes (mock, summarized by Product)**
- Four beta accounts asked for the same thing on Confluence.
- Two accounts did not understand at first that only changes after the first Rewind backup can be rolled back.
- Two accounts did not use the audit log export.
- Before the beta, accounts said they had been fixing bad changes by hand, restoring the whole site, or doing nothing.

## 6. Open questions from the Slack thread

Pasted from the #agent-rollback-ga thread (mock, roles only).

- **Product manager, Jira:** Pricing and packaging still owes us the plan name and price. Without it we can only say "a specific plan tier".
- **Support lead:** The attachment limitation says the backup "may be up to 24 hours old". The company site says recovery points are under 24 hours. Which do we say for Agent Rollback?
- **Sales Engineering:** Can we say Atlassian native has no actor-based rollback? Do we have a source, or is that just what we believe?
- **Engineering lead:** How Actor view tells apart a person, a rule, an integration and an AI agent is not documented yet.
- **Engineering lead:** Rollback of a field that a person edited after the agent is not covered in the beta tests. Not decided.
- **Customer success:** Who is allowed to run a rollback is not settled. Admin only, or other roles?
- **Product manager, Jira:** Which Jira data types can be rolled back beyond issues and fields is not confirmed.
- **Sales Engineering:** Do we know how it behaves on sites above Atlassian's size limits?
- **Legal:** Please check the wording "exportable for auditors" and any mention of Confluence before it goes public.
- **Revenue operations:** We cannot yet capture "AI governance cited as a buying reason" in the CRM.
- **Product marketing:** Can we use any beta numbers or quotes externally? Customers have not agreed to that.
