# Enablement session: Agent Rollback for Jira

**Length:** 30 minutes | **When:** L-7 (live session) | **Audience:** Sales reps and Sales Engineers | **Prep for reps:** Read the one-pager, talk track and Limits in `09-sales-enablement.md` (delivered L-10). The quiz in `09c-readiness-quiz.md` is due L-5.

> Agent Rollback is a hypothetical product from a mock handoff. Closed beta numbers and quotes are mock, internal evidence. The trainer may mention what the beta taught the team. Reps must not repeat beta numbers or quotes to customers. [NEED PROOF: approval to use closed beta results or quotes]

## Agenda

| Time | Block | What happens | Who leads |
|---|---|---|---|
| 0:00 to 0:03 | Why this matters | The two bad options. One actor, many changes. | Sales enablement lead |
| 0:03 to 0:08 | Talk track and positioning | Say the talk track out loud. Cover the native line. | Sales enablement lead |
| 0:08 to 0:12 | Limits drill | Reps say the limits without looking. | Sales enablement lead, Sales Engineering |
| 0:12 to 0:17 | Role-play 1: the admin | Pairs. One rep, one buyer. | Reps in pairs |
| 0:17 to 0:22 | Role-play 2: the IT or security leader | Pairs. Swap roles. | Reps in pairs |
| 0:22 to 0:27 | Role-play 3: the AI or automation owner | Pairs. Swap roles. | Reps in pairs |
| 0:27 to 0:30 | Wrap-up and quiz | Open questions, next steps. | Sales enablement lead |

Blocks add up to 30 minutes.

## Talking points

1. **Two bad options.** When a rule, an integration or an AI agent changes the wrong issues, the admin restores the whole site and loses the team's work since the backup, or fixes it by hand. Agent Rollback is the third option. (05 core message, Pillar 1)
2. **The actor is broad.** Say rule, integration or AI agent. AI is why the safety net matters. It is never the problem. In the closed beta (internal, small group), more rollbacks were on rules than agents, so do not lead with AI alone. (05 admin angle; 04 section 4)
3. **See it first.** The blast radius preview shows which issues, fields and projects will change back and which will stay, before anything is restored. This is the part to demo. (05 Pillar 2)
4. **People's work stays.** Say only what the demo showed: separate edits people made after the bad event stay in place. Do not say how a same-field edit behaves. (05 Must say 6)
5. **A record for the approver.** Each rollback is logged with who ran it, what changed and when, and the log can be exported. Say "can be exported". Do not say "exportable for auditors" until Legal clears it. (05 Pillar 3)
6. **Rewind sits on top of native.** Native Backup and Restore works at the site level. Rewind does not replace it. Never say native lacks anything. (04 section 1; `context/company.md`)
7. **The limits, out loud.** Say them before the customer asks. After your first Rewind backup only. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Jira Cloud. A specific plan tier. Issues and fields are confirmed, other data types are not. Stop at that wording on attachments. (05 Must say 1 to 5)

## Role-play 1: The Atlassian admin (primary)

- **Setup:** A Jira admin at a mid-size company. Rewind backup runs on their Jira Cloud site. They own many automation rules. You called after the email went out.
- **The rep's goal:** Find the pain with discovery questions, then land the third option and state the limits without being asked.
- **The buyer says:**
  1. "Last time a rule went wrong I either had to restore the site or fix it by hand. Neither was good."
  2. "Can I roll back everything it did, even from last year?"
  3. "If I roll back, do my team's edits survive?"
- **What good looks like:** Asks question 1 and 2 from discovery before pitching. Answers line 2 with "after your first Rewind backup, and issues and fields are confirmed". Answers line 3 with the demo wording only: separate edits stay in place. Offers the preview. Uses the word "actor", rule or integration, not only AI.
- **Common mistake:** Saying "everything" or "any time window". Or promising the same-field case works.

## Role-play 2: The IT or security leader (secondary)

- **Setup:** A Head of IT in a regulated company. The admin brought you in. They have to approve an AI agent rollout in Jira and want a recovery plan first.
- **The rep's goal:** Give them the preview and audit log as things to look at, state the limits, and say plainly what is not decided.
- **The buyer says:**
  1. "Who exactly can run a rollback?"
  2. "Will the audit log satisfy my auditors?"
  3. "Do you have customer references and numbers?"
- **What good looks like:** Line 1: "That is still being decided. I will come back to you." No guessed role. Line 2: each rollback is recorded with who ran it, what changed and when, and the log can be exported. No claim it meets a requirement. Line 3: "Not that I can share today. I can show you the preview and the audit log." Keeps the tone calm, no fear.
- **Common mistake:** Guessing "admins only". Saying "exportable for auditors". Quoting beta results.

## Role-play 3: The AI or automation owner (emerging influencer)

- **Setup:** A platform lead rolling out AI agents across Jira. They need IT and security to say yes. They worry you will frame them as the risk.
- **The rep's goal:** Position Agent Rollback as what helps them get to yes. Never frame them as the problem.
- **The buyer says:**
  1. "Security keeps asking what happens when an agent gets it wrong."
  2. "Is this only for AI agents? We have plenty of rules too."
  3. "Is Atlassian's own restore not enough?"
- **What good looks like:** Line 1: preview plus audit log are the two things to show security, with the limits. Line 2: no, the actor can be a rule, integration or agent. Line 3: native works at the site level, Rewind sits on top, no claim that native lacks anything.
- **Common mistake:** Saying "no other tool does this". Saying "Atlassian has no actor-based rollback". Making the owner sound like the risk.

## Wrap-up

- Reps take the one-pager and Limits home. Practice the talk track out loud once before L.
- Complete the readiness quiz (`09c-readiness-quiz.md`). It is due L-5. Proposed pass mark is 7 of 8. [NEED PROOF: pass mark and target share of reps, from 06 success metrics]
- Questions nobody could answer in the session go to `learnings/field-feedback.md`. Quiz gaps go there too.
- Open items to say out loud: plan name and price, GA date, who can run a rollback, same-field edits, large sites, attachment wording, data types. Reps say "I will find out", never guess.
