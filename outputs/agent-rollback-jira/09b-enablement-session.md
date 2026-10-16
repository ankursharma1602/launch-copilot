# Enablement session: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. Personas are demo personas from `context/personas.md`. Validate against real customer research. Session timing per `06-campaign-strategy.md`: L-5 to L-3. GA date: [NEED PROOF: GA date].

**Length:** 30 minutes | **Audience:** Account executives, SDRs and sales engineers who sell Rewind Jira Cloud backup | **Prep for reps:** Read `09-sales-enablement.md` (one-pager, talk track, objections). Say the talk track out loud once. Know the four limits by heart.

## Agenda
| Time | Block | What happens | Who leads |
|---|---|---|---|
| 0:00 to 0:03 | Why this matters | The moment: an agent or rule changes thousands of issues. The two bad options today. | Enablement lead |
| 0:03 to 0:08 | The message and talk track | Walk the core message, the three pillars and the talk track. Reps say it back in pairs. | Enablement lead |
| 0:08 to 0:12 | Limits and the native question | The four limits, the attachment wording, and how to answer "Atlassian already has this." | Enablement lead, with a sales engineer |
| 0:12 to 0:17 | Role-play 1: Atlassian admin | Pairs. One rep, one buyer, one observer. | Reps, enablement lead observes |
| 0:17 to 0:22 | Role-play 2: IT or security leader | Pairs. Rotate roles. | Reps, enablement lead observes |
| 0:22 to 0:27 | Role-play 3: AI or automation owner | Pairs. Rotate roles. | Reps, enablement lead observes |
| 0:27 to 0:30 | Wrap-up and quiz | Open gaps, who to ask, the readiness quiz. | Enablement lead |

Blocks: 3 + 5 + 4 + 5 + 5 + 5 + 3 = 30 minutes.

## Talking points

- **Start with the moment.** An AI agent, automation rule or integration changes a lot of Jira issues the wrong way. The PRD's illustrations are 4,000 issues reclassified or a custom field overwritten across 30 projects. These are illustrations of the problem, not customer data. (Source: `05-messaging.md`, pillar 1.)
- **Two bad options today.** Restore the whole site and lose legitimate changes since the backup, or fix it by hand. Agent Rollback is a third option: undo the one actor, not the whole site. (Source: `05-messaging.md`, core message.)
- **How it works, in the admin's words.** See every change grouped by who or what made it. Pick a time window. Preview which issues, fields and projects change back and what stays. Restore only that actor's changes. Changes people made afterward stay. (Source: `05-messaging.md`, pillars 1 and 2.)
- **A plan to show an approver.** Each rollback is recorded with who ran it, what changed and when. The record is exportable for auditors. Say that and no more. No standard, no "audit-ready." (Source: `05-messaging.md`, pillar 3.)
- **Rewind sits on top of native.** Atlassian's native Backup and Restore works at the site level and is the right tool for a full-site loss. Recovering your own data is a shared responsibility. Never imply Atlassian is unreliable. Never say native lacks actor-based rollback. (Source: `05-messaging.md`, supporting message.)
- **Say the four limits before they find them.** Only changes made after your first Rewind backup can be rolled back. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Jira Cloud only at launch, Confluence on the roadmap with no date. Included in a specific plan tier, so not every plan has it. (Source: `05-messaging.md`, Must say.)
- **When you do not know, say so.** Speed, limits, permissions, conflict handling, actor-type detection, price, plan, date and customer proof are all open. Say "I will find out" and send the question to enablement. Do not guess. (Source: `02-launch-context.md`, Gaps.)

## Role-play 1: The Atlassian admin

- **Setup:** A Jira Cloud admin on a call with a team of one or two. They run automation rules and are starting to wire AI agents into Jira. Demo persona, validate against real research.
- **The rep's goal:** Find the pain with two discovery questions, give the talk track, and state all four limits without being asked.
- **The buyer says:**
  - "If an agent trashes a bunch of issues, I restore the whole site and everyone loses a day. I hate that."
  - "Does it only go back to when we started with Rewind?"
  - "What about attachments the agent deleted?"
- **What good looks like:** The rep asks about the last time something went wrong before pitching. The rep uses "undo the one change, not the whole site." The rep answers the second line with the first-backup limit and the third with the PRD attachment wording, word for word in meaning. The rep does not promise a restore time.
- **Common mistake:** Skipping the first-backup limit, or saying attachments come back "within 24 hours." Also: promising speed or saying it works on "everything."

## Role-play 2: The IT or security leader

- **Setup:** A Head of IT at a company in a regulated industry. They have to approve an AI rollout and want a recovery plan first. Demo persona, validate against real research.
- **The rep's goal:** Frame Agent Rollback as a recovery plan the admin can show them. Stay within "exportable for auditors." Be honest about plan and price being open.
- **The buyer says:**
  - "Is the audit log compliant with our standard?"
  - "What plan is this on, and what does it cost?"
  - "Atlassian already gives us backup and restore. Why pay for another layer?"
- **What good looks like:** The rep says each rollback is recorded with who ran it, what changed and when, and is exportable for auditors, and offers to get export details. The rep names no standard. On plan: "specific tier, not every plan, I will confirm the plan and price." On native: Rewind sits on top, native works at the site level and is the right tool for a full-site loss. The rep states the Jira Cloud only limit if platform comes up.
- **Common mistake:** Saying "audit-ready" or "compliant." Naming a plan or price. Implying Atlassian's tool is unreliable. Claiming native has no actor-based rollback.

## Role-play 3: The AI or automation owner

- **Setup:** A platform lead rolling out AI agents across Jira. They want to say yes to AI and need IT and security to approve. Demo persona, validate against real research. They are in the buying group, not the lead target.
- **The rep's goal:** Position Agent Rollback as the safety net behind the yes, never as a sign their agent is the problem. Find who approves and what that person asks for.
- **The buyer says:**
  - "I do not want my agent framed as the risk."
  - "Can it tell my agent apart from our automation rules?"
  - "How many issues can it handle at once, and how fast?"
- **What good looks like:** The rep says the agent is one actor among several and people show up in Actor view too. On the second line the rep says Actor view groups changes by person, automation rule, integration or AI agent, and that how each is identified is something they will confirm with engineering. On the third the rep says there is no speed or limit they can stand behind yet, and they will find out. The rep asks who approves the rollout and what they ask for.
- **Common mistake:** Promising rollback works per actor type. Quoting a speed. Talking as if the owner caused the problem. Treating them as the decision maker.

## Wrap-up

- Reps take the readiness quiz (`09c-readiness-quiz.md`) by L-2. Pass mark is 7 of 8.
- Keep the one-pager open on calls. The four limits go in the first two minutes.
- Send any question you cannot answer to enablement through `/ask-enablement`. It is logged in `learnings/field-feedback.md`.
- Open items reps should expect to hear about: GA date, plan names and pricing, competitor check, attachment wording, audit log wording, actor-type detection, data types, conflict handling, limits and permissions. Until product answers, use the holding lines in `09-sales-enablement.md`.
