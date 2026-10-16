# Channel copy: Agent Rollback for Jira (Tier 2)

**Builds on:** 05-messaging.md, 06-campaign-strategy.md | **Persona:** the Atlassian admin (primary) | **Launch date:** not stated in any asset

**Produced for this tier:** customer email, in-app message, release note, LinkedIn post, on-image text for four visuals (email header, in-app banner, LinkedIn image, one-pager layout).
**Deliberately skipped:** blog post outline and blog hero image (Tier 1 only), Sales FYI (Tier 3 only).

> No beta numbers, customer quotes, price, plan name or date appear anywhere below. Scale scenarios are not used. Limitations were written into each asset first, then the rest was fitted around them.

## Customer email

**Subject A:** Undo the one change, not the whole site (38 characters)
**Subject B:** Undo what one rule or AI agent changed in Jira (46 characters)
**Preview:** Undo one actor's changes in Jira Cloud, see the effect first. (61 characters)

A rule, an integration or an AI agent changed issues it should not have. You could restore the whole site and lose your team's work, or fix it by hand.

With Agent Rollback, pick the one actor and a time window. See which issues, fields and projects will change back, and which will stay. Then undo that actor's changes. Separate edits people made after the bad event stay in place. Each rollback is logged with who ran it, what changed and when. The log can be exported.

Good to know:
- Works on Jira Cloud. It can undo changes made after your first Rewind backup.
- Covers issues and fields.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- Included in Rewind's Jira Cloud backup plans at a specific plan tier.

**CTA:** Read the release note [link]

(Body word count: 140 plus 4 for the CTA, under 150.)

## In-app message

**Headline:** Undo what one rule or agent changed (7 words)
**Body:** Jira Cloud, after your first backup. Agent-deleted attachments come from the latest backup, which may be up to 24 hours old. Specific plan tier. (24 words)
**Button:** See details (2 words)

## Release note

**Title:** Agent Rollback: undo what one rule, integration or AI agent changed in Jira Cloud

**Summary:** When a rule, an integration or an AI agent changes issues it should not have, you no longer have to choose between a whole-site restore and fixing it by hand. Agent Rollback works on Jira Cloud and can undo changes made after your first Rewind backup. Pick the one actor and a time window, see what will change back, then undo just that actor's changes.

**What's new**
- **Actor view:** See changes in Jira grouped by who or what made them: a person, an automation rule, an integration or an AI agent.
- **Blast radius preview:** Before you restore anything, see which issues, fields and projects will change back and which will stay as they are.
- **Selective rollback:** Undo all changes by one actor in a time window, or pick specific issues or fields. No whole-site restore.
- **Keep human work:** Separate edits people made after the bad event stay in place.
- **Audit log:** Each rollback is recorded with who ran it, what changed and when. The log can be exported.

**How to get started**
1. [NEED PROOF: how a customer turns the feature on, and whether it needs setup]
2. Make sure Rewind backup is running on your Jira Cloud site.
3. Open Actor view. Pick the rule, integration or AI agent and a time window.
4. Review the preview of what will change back and what will stay.
5. Roll back all of that actor's changes, or pick specific issues or fields.
6. Check the audit log entry for the rollback.

**Availability and known limits**
- Works on Jira Cloud.
- Can undo changes made after your first Rewind backup.
- Covers issues and fields.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
- Included in Rewind's Jira Cloud backup plans at a specific plan tier.

## LinkedIn post

A rule, an integration or an AI agent changed issues it should not have. Restore the whole site, or fix it by hand?

Agent Rollback lets you pick the one actor and a time window. See what will change back before you restore anything. Separate edits people made after the bad event stay in place. Every rollback is logged.

Limits: Jira Cloud, changes after your first Rewind backup, issues and fields. Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old. Included at a specific plan tier.

Read the release note: [link]

(Count: 112 words, under 120. No hashtags, no emojis.)

## On-image text

Written to be rendered unchanged. Counts include the wordmark "Rewind". The email header, in-app banner and LinkedIn image carry no limitations, disclaimers, plan caveats or "only" claims. Those sit in the copy above.

### Email header (13 words)
- Wordmark: Rewind
- Headline: Undo the one change, not the whole site.
- Supporting line: Agent Rollback for Jira

### In-app banner (13 words)
- Wordmark: Rewind
- Headline: Undo what one rule or AI agent changed.
- Supporting line: See the effect first.

### LinkedIn image (17 words)
- Wordmark: Rewind
- Headline: Undo the one actor, not the whole site.
- Supporting line: See what will change back before you restore.

### One-pager layout (28 words)
- Wordmark: Rewind
- Headline: Undo what one rule or AI agent changed.
- Supporting line: See what changes back first.
- Small limits line (the only visual allowed one): Jira Cloud. Changes after your first Rewind backup. Issues and fields. Specific plan tier.

## Notes for the reviewer and design

- The attachment limit does not fit the one-pager's one small line within 30 words. It must be carried in the one-pager body copy in 09-sales-enablement.md. The in-app body carries it in shortened form ("latest backup" for "most recent backup", "Agent-deleted" for "deleted by an agent") to fit 25 words. The attachment wording is still an open item. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
- The next step is the release note because how a customer turns the feature on is unknown. [NEED PROOF: how a customer turns the feature on, and whether it needs setup]
- The Confluence roadmap line is left out of every asset. It needs Legal sign-off and none of these assets mention Confluence.
- "Exportable for auditors" is not used. Copy says "can be exported".
- Brand hex codes and typeface are unconfirmed, so no visual leaves the team yet. [NEED PROOF: confirm brand hex codes and typeface]
