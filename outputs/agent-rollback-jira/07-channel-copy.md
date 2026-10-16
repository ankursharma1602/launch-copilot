# Channel copy: Agent Rollback for Jira (Tier 2)

**Produced for this tier:** customer email, in-app message, release note, LinkedIn post. Plus exact on-image text for four visuals (email header, in-app banner, LinkedIn image, one-pager layout).
**Deliberately skipped:** blog post outline and blog hero image (Tier 1 only). Sales FYI (Tier 3 only). Sales assets are written in `09-sales-enablement.md`.

> Hypothetical release written to demo Launch CoPilot. No plan name, price or date appears. Placeholders are marked `[NEED PROOF: ...]`.

The four Must say limits, short form used below:
1. First backup: only changes made after the first Rewind backup can be rolled back.
2. Attachments: restored from the most recent backup, which may be up to 24 hours old.
3. Platform: Jira Cloud only at launch. Confluence on the roadmap, no date committed.
4. Plan: included at a specific tier, so not every plan has it.

---

## Customer email
Audience: existing Rewind Jira Cloud customers. Persona: Atlassian admin, then IT or security leader. Pillars 1, 2, 3.

**Subject A:** Undo one agent's changes, not the whole site (44 characters)
**Subject B:** Undo one actor's changes in Jira (32 characters)
**Preview:** Preview what changes back, keep your team's work, undo only that actor. (71 characters)

Hi [First name],

When an agent or automation rule changes thousands of Jira issues the wrong way, you can restore the whole site and lose your team's work, or fix it by hand.

Agent Rollback gives you another way. Find what one actor changed, preview what will change back, and undo only that. Changes people made since stay in place. Each rollback is recorded, and the record is exportable for auditors.

Before you start:
- Only changes made after your first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- Jira Cloud only at launch. Confluence is on the roadmap, no date committed. [NEED PROOF: sign-off to mention Confluence roadmap publicly]
- Included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. [NEED PROOF: plan names and pricing]

**CTA:** Open Actor view [NEED PROOF: destination link]

Body is about 130 words.

**Email header, on-image text (verbatim, 24 words):**
- Headline: Undo one agent's changes, not the whole site.
- Footer strip: Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back.

---

## In-app message
Audience: admins inside Rewind. Limits written first, then headline and button fitted around them.

**Headline:** Undo one agent, not the whole site (7 words)
**Body:** Only changes after first backup roll back. Deleted attachments restore from a backup up to 24 hours old. Jira Cloud only, not every plan. (24 words)
**Button:** See Actor view (3 words)

**In-app banner, on-image text (verbatim):**
- Line 1: Undo one agent, not the whole site.
- Line 2: Jira Cloud only. Changes after your first backup. Not on every plan.
- Button label: See Actor view

Note: "Confluence on the roadmap" is left out of the in-app and banner short form because the roadmap line has no sign-off. The release note and email carry it with the flag.

---

## Release note

**Title:** Undo the changes of one actor in Jira, not the whole site

**Summary:** Agent Rollback lets a Jira Cloud admin find every change made by one actor, preview what will change back, and restore only that. An actor can be a person, an automation rule, an integration or an AI agent. Changes people made after the bad event stay in place.

**What's new**
- Actor view: see changes in Jira grouped by who or what made them. [NEED PROOF: how Actor view tells people, automation rules, integrations and AI agents apart]
- Blast radius preview: before you restore, see which issues, fields and projects will change back and what will stay as is.
- Selective rollback: undo all changes by one actor in a time window, or pick the issues or fields to undo.
- Keep human work: changes people made after the bad event are preserved. [NEED PROOF: how a rollback is handled when a person later edited the same issue or field]
- Audit log: each rollback is recorded (who ran it, what changed, when). The record is exportable for auditors.

**How to get started**
1. Confirm your site has a Rewind Jira Cloud backup. [NEED PROOF: roles and permissions needed to run a rollback]
2. Open Actor view [NEED PROOF: navigation path in the Rewind app] and pick the actor.
3. Choose a time window, or pick specific issues or fields.
4. Review the blast radius preview.
5. Restore. Export the audit log if an auditor asks.

**What to know**
- Only changes made after your first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- Rewind sits on top of Atlassian's native Backup and Restore, which works at the site level. Keep using native for a full-site recovery.

**Availability:** Jira Cloud only at launch. Confluence is on the roadmap, no date committed. [NEED PROOF: sign-off to mention Confluence roadmap publicly] Agent Rollback is included in Rewind's Jira Cloud backup plans at a specific tier, so not every plan has it. [NEED PROOF: plan names and pricing] Available from [NEED PROOF: GA date].

---

## LinkedIn post
Audience: admins and IT leaders outside the customer base. Limits written first, hook and body fitted around them. Under 120 words (about 108).

Picture an agent reclassifying 4,000 Jira issues. Restore the whole site, or fix them by hand?

Agent Rollback finds what one actor changed, previews what changes back, and undoes only that. Your team's later work stays. Each rollback is logged and exportable for auditors.

The limits, up front:
- Only changes after your first Rewind backup can be rolled back.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- Jira Cloud only at launch. Confluence on the roadmap, no date committed.
- Included at a specific plan tier, so not every plan has it.

[NEED PROOF: destination link]

Hashtags: none. Sign-off needed on the Confluence line: [NEED PROOF: sign-off to mention Confluence roadmap publicly]

**LinkedIn image, on-image text (verbatim, 28 words):**
- Headline: Undo one agent's changes, not the whole site.
- Sub-line: Keep your team's work.
- Footer strip: Jira Cloud only at launch. Only changes after your first Rewind backup. Not on every plan.

---

## One-pager layout, on-image text (verbatim, 42 words)
For the sales one-pager visual. Design uses this text as written.

- Headline: Undo one agent's changes, not the whole site. (8 words)
- Limits box title: What to know (3 words)
- Limits box lines (15 words):
  - Attachments: backup up to 24 hours old.
  - Confluence: roadmap, no date. [NEED PROOF: sign-off to mention Confluence roadmap publicly]
  - Not on every plan.
- Footer: Jira Cloud only at launch. Only changes after your first Rewind backup can be rolled back. (16 words)

**Approved exception to the 30-word cap:** the one-pager is 42 words. It is a print layout with a must-say limits box, and limits come first per lessons. The cap still applies to the other three visuals.

## Body for the sales one-pager (not on the visual)
The full one-pager body, with the four limits and objection handling, is in `09-sales-enablement.md`. The block text below is source material for it, not on-image text.

- Block 1 title: Undo the one actor
- Block 1 text: See changes grouped by who or what made them. Undo one actor's changes in a time window, or pick the issues or fields.
- Block 2 title: Keep your people's work
- Block 2 text: Preview which issues, fields and projects change back and what stays as is.
- Block 3 title: A recovery plan to show an approver
- Block 3 text: Each rollback is recorded. The record is exportable for auditors.
- Positioning line (body only): Rewind sits on top of Atlassian's native Backup and Restore, which works at the site level.

---

## Self-check
- Four limits present in the email, in-app, LinkedIn, release note and one-pager. Confluence roadmap is omitted only from the in-app message and banner, and flagged everywhere else pending sign-off.
- Email subjects 44 and 32 characters, preview 71. In-app headline 7 words, body 24, button 3.
- On-image words: email header 24, banner 22, LinkedIn image 28, one-pager 42. The first three are at or under 30. The one-pager is an approved exception to the 30-word cap (print layout with a must-say limits box, limits first). Its box lines are listed in the one-pager block above.
- No em dashes, exclamation marks, banned words, plan name, price or date.
- "Under 24 hours" does not appear. No claim that native lacks actor-based rollback. No third-party claims. No customer data. The 4,000 issues figure is the PRD illustration, framed as "picture".
- Open flags: GA date, plan names and pricing, links, Confluence sign-off, actor-type detection, conflict handling, permissions, audit log legal review.
