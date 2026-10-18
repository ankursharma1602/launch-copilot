# Agent Rollback for Jira: Launch Plan of Record

Tier 2 launch | Status: draft, ready for review | Owner: Product Marketing | Updated: 2026-10-18

## 1. Executive summary
- **What:** Agent Rollback lets a Jira Cloud admin undo everything one rule, integration or AI agent changed, see the effect first, and keep people's own work.
- **For whom:** Jira admins first. IT and security leaders who approve AI rollouts second.
- **Why now:** rules and AI agents edit Jira at a scale no person does, and the feature is moving from closed beta to general availability.
- **Tier and date:** Tier 2, a targeted launch. Target date not set. All dates below count from launch day (L).
- **Goal:** get eligible Jira customers using it in 30 days, upgrading in 90 days, and give Sales a new story with security buyers.
- **Decisions needed:** GA date, plan names and pricing, brand sign-off, Legal review, and approval to use beta proof. See section 10.

## 2. Why
**The customer problem.** When a rule, integration or AI agent changes issues it should not have, admins have two bad options. They restore the whole site and lose everyone's legitimate work since the backup. Or they fix it by hand, issue by issue.

**The evidence.**
- In closed beta, admins described this as "the bad Tuesday", when one rule overwrote a field across many projects.
- They also said the preview and keeping people's later edits were what made them trust it.
- Rewind's CEO named AI usage as a growth driver: AI agents now act directly on SaaS data, which creates new recovery needs.
- Closed beta results are internal and from a small group. We do not use them in customer-facing work until customers approve.

**Launch goals and KPIs.** Baselines and targets are not set yet. Product owns setting them before the go/no-go.

| Goal | KPI | Read at |
|---|---|---|
| Adoption | Share of active Jira customers who open the new activity view within 30 days | L+30 |
| Expansion | Upgrades to the plan that includes Agent Rollback | L+90 |
| Pipeline | New opportunities where AI governance is a buying reason | L+90 |
| Sales readiness | Reps who pass the readiness quiz | L-5 |

The pipeline KPI cannot be read until Revenue Operations can record the buying reason in the CRM.

## 3. What
**In plain words.** An admin picks the rule, integration or AI agent that went wrong and a time window. They see exactly what will change back and what will stay. Then they undo it. Each rollback is logged.

**What it does**
- Groups every change in Jira by who or what made it: a person, a rule, an integration or an AI agent.
- Shows a preview of which issues, fields and projects will change back, before anything does.
- Undoes everything one rule, integration or AI agent changed in a time window, or just the issues and fields you pick.
- Leaves in place the changes people made after the bad event.
- Records each rollback with who ran it, what changed and when, and lets you export the log.

**What it does not do**
- It only covers changes made after the customer's first Rewind backup.
- Attachments deleted by an agent are restored from the most recent backup, which may be up to 24 hours old.
- It works on Jira Cloud only. Confluence is on the roadmap with no date.
- Beyond issues and fields, we have not confirmed what else can be rolled back.
- We have not decided what happens when a person edited the same field after the agent. We do not claim anything about it.
- We do not yet know how it behaves on very large sites, or who is allowed to run a rollback.

**Availability.** Included in Rewind's Jira Cloud backup plans at a higher plan tier. Plan name and price are not set, so customer copy says "a specific plan tier".

## 4. Who
- **Primary buyer and user:** the Jira admin. They run the rollback and make the case inside the company. They own uptime, rules and the AI tools wired into Jira, and they are the person everyone looks at when something breaks.
- **Secondary buyer:** the IT or security leader. They approve the plan and any AI rollout. They want a recovery plan and a record to attach to the approval. They get the message through the admin, with no separate campaign.
- **Best-fit accounts to reach first:** existing Rewind Jira Cloud customers, sites with heavy automation, teams rolling out AI agents, and regulated industries.
- **Out of scope:** Confluence-only admins, teams without Rewind backup on Jira Cloud, buyers who want ROI proof, and very large sites or unusual data types until we have answers.

## 5. How we win
**Positioning.** The real competitor is the choice between restoring everything and fixing it by hand. Atlassian's own restore is built for full-site recovery. Agent Rollback is for the bad Tuesday, when one rule or agent went wrong and the rest of the site is fine. We do not claim Atlassian lacks anything, and we do not name other tools.

**Core message.** When a rule, an integration or an AI agent changes issues it should not have, undo just what it changed, see the effect first, and leave people's work alone.

**Three pillars**
1. **Undo the one change, not the whole site.** Pick what went wrong and a time window. People's later edits stay in place.
2. **See it before it changes.** Preview what will change back and what will stay before you commit.
3. **A record you can hand to security.** Every rollback is logged, and the log can be exported.

**Proof.**
- Approved today: Rewind protects 16 cloud applications for more than 25,000 organizations, including financial services, healthcare and manufacturing. This supports the company, not this feature.
- The product itself: the features above are built and shown in the demo.
- Not yet available: customer results, quotes and any time-saved figure. We say so in the copy and do not fill the gap.

Detail: [04-positioning.md](04-positioning.md), [05-messaging.md](05-messaging.md).

## 6. Where
| Phase | When | Channel and tactic |
|---|---|---|
| Pre-launch | L-28 to L-18 | Build the copy, visuals, sales kit and checklist |
| Pre-launch | L-17 to L-14 | Review, with Legal, Support and Brand sign-off |
| Pre-launch | L-10 to L-5 | Sales kit delivered (L-10), rep session (L-7), readiness quiz (L-5) |
| Launch | L | Customer email with header image to existing Jira Cloud customers |
| Launch | L | In-app message and banner for admins inside Rewind |
| Launch | L | Release note |
| Launch | L+1 | LinkedIn post and image, to reach admins and IT leaders beyond our customers |
| Launch | From L | Sales one to one, with admin and approver together |
| Post-launch | L+14, L+30 | Review questions reps could not answer |
| Post-launch | L+30 | Adoption check |
| Post-launch | L+90 | Upgrade and pipeline check, and lessons review |

No paid media, press or analyst push in this tier.

## 7. Enablement
| Audience | What they get | When |
|---|---|---|
| **Sales and Sales Engineering** | One-pager, 30-second talk track, discovery questions, objection handling, FAQ and a competitive take: [09-sales-enablement.md](09-sales-enablement.md) | Delivered L-10 |
| **Sales and Sales Engineering** | 30-minute live session with role-plays: [09b-enablement-session.md](09b-enablement-session.md) | L-7 |
| **Sales and Sales Engineering** | Readiness quiz: [09c-readiness-quiz.md](09c-readiness-quiz.md) | Due L-5 |
| **Sales** | Ongoing answers and call prep from the Sales Enablement Lead | From L |
| **Customer Success** | Nothing built for CS in this kit. Proposal: share the FAQ and limits in the sales kit, and brief CS on the first-backup and attachment limits. Needs an owner. | Proposed for L-7 |
| **Partners** | Nothing built for Partners in this kit and no partner plan in the sources. Needs a decision on whether partners are in scope. | To decide |

Rule for everyone: say every limit out loud, before the customer asks.

## 8. Launch team
Roles only. The handoff names no people. Names to be added by the launch lead.

| Role | Owns in this launch |
|---|---|
| **Product Marketing** (launch lead) | This plan, positioning, messaging, copy, what claims are allowed |
| **Product Manager, Jira** | Scope, GA date, success metrics, which data types can be rolled back. Runs the go/no-go |
| **Engineering lead** | How the activity view tells a person from a rule, integration or AI agent; the same-field case; large sites |
| **Pricing and packaging** | Plan name and price |
| **Sales and Sales Engineering** | Using the kit; sourcing any claim about Atlassian or other tools |
| **Sales Enablement Lead** | Sales kit, rep session, quiz, feedback from reps |
| **Customer Success** | Who can run a rollback; customer agreement to use beta results |
| **Support lead** | Plain wording for the attachment limit |
| **Marketing (lifecycle and social)** | Email, in-app, release note, LinkedIn |
| **Legal** | Review of "exportable for auditors" and any Confluence mention |
| **Brand team** | Sign-off on colours and typeface |
| **Revenue Operations** | CRM field for "AI governance cited as a buying reason" |
| **Partners** | To be named, if in scope |

**Who decides.** The Product Manager for Jira makes the go/no-go call at L-3. Product Marketing recommends. Legal and the Brand team can each block their own items.

## 9. Key dates and the go/no-go
| When | Milestone |
|---|---|
| L-28 | Build starts. GA date confirmed |
| L-17 to L-14 | Final review and one revision pass |
| L-15 | Owners answer open questions: pricing, attachment wording, Legal, brand, data types |
| L-10 | Sales kit delivered |
| L-7 | Rep session |
| L-5 | Quiz due. Baselines and targets set |
| L-3 | Go/no-go |
| L | Email, in-app message and release note go live |
| L+1 | LinkedIn post and image |
| L+30 | Adoption check |
| L+90 | Upgrade and pipeline check |

**Go/no-go: all six must be met at L-3, or the date moves.**
1. GA date confirmed.
2. Plan wording settled: either the real plan name and price, or "a specific plan tier".
3. Legal has cleared "exportable for auditors" and any Confluence line, or both are cut.
4. Support, Product and Engineering have agreed the attachment wording.
5. Brand team has confirmed colours (yellow #FFC72C, navy #16225C) and typeface.
6. Product analytics can count how many customers open the activity view.

Approval to use beta results is not a gate, because the kit does not use them.

## 10. Risks and open decisions
**Decisions needed now**

| Decision | Owner | Needed by |
|---|---|---|
| GA date | Product Manager, Jira | L-28 |
| Plan names and pricing | Pricing and packaging | L-15 |
| Brand sign-off on visuals | Brand team | L-15 |
| Legal review of "exportable for auditors" and the Confluence line | Legal | L-15 |
| Approval to use closed beta results and quotes in public | Customer Success | Not a gate. Review at L+30 |
| Partners in scope or not | Launch lead | L-28 |

**Risks**

| Risk | What we do |
|---|---|
| No GA date | Every date is counted from L, and the go/no-go moves the launch if needed |
| Attachment wording conflict between the beta handoff and our existing backup wording | Use the handoff wording only. Never say "under 24 hours" next to Agent Rollback |
| No source for a claim that Atlassian lacks this | Say Atlassian's restore works at the site level. Make no stronger claim |
| No customer proof or outcome numbers | Lead with the problem and the two bad options. No speed, time or ROI claims |
| Limits get lost in short assets | Images carry no limits, so the email, in-app message and release note carry them all |
| Customers misread the first-backup limit | State it plainly in every written asset and in the sales kit |
| Open product questions (who can run it, large sites, same-field edits) | Reps have holding lines. We make no claim until answered |
| CRM cannot record the buying reason | Revenue Operations adds a field before L, or the L+90 pipeline read is reported as not measurable |
| A larger eligible base could justify a bigger launch | Re-score at the go/no-go if the base is sized |

The full list of open items, by file, is in [11-review.md](11-review.md#full-open-items).

## 11. Launch assets
Status: all assets passed review. Three sales files needed one wording fix first. Items marked "Waiting" need a decision from section 10 before release.

| Asset | Owner | Status | File |
|---|---|---|---|
| Launch brief | Product Marketing | Final | [01-launch-brief.md](01-launch-brief.md) |
| Product context | Product Marketing | Final | [02-launch-context.md](02-launch-context.md) |
| Audience | Product Marketing | Final | [03-audience.md](03-audience.md) |
| Positioning | Product Marketing | Final | [04-positioning.md](04-positioning.md) |
| Messaging | Product Marketing | Final | [05-messaging.md](05-messaging.md) |
| Campaign strategy | Product Marketing | Final | [06-campaign-strategy.md](06-campaign-strategy.md) |
| Customer email, in-app message, release note, LinkedIn post | Marketing (lifecycle, social) | Waiting: GA date, pricing, Legal | [07-channel-copy.md](07-channel-copy.md) |
| Design briefs | Product Marketing, Brand team | Waiting: brand sign-off | [08-design-briefs.md](08-design-briefs.md) |
| Email header | Marketing | Waiting: brand sign-off | [email-header.png](visuals/email-header.png) |
| In-app banner | Marketing | Waiting: brand sign-off | [in-app-banner.png](visuals/in-app-banner.png) |
| LinkedIn image | Marketing | Waiting: brand sign-off | [linkedin-image.png](visuals/linkedin-image.png) |
| One-pager layout | Sales Enablement Lead | Waiting: brand sign-off, pricing | [one-pager-layout.png](visuals/one-pager-layout.png) |
| Sales kit | Sales Enablement Lead | Waiting: attachment wording, Legal | [09-sales-enablement.md](09-sales-enablement.md) |
| Rep session plan | Sales Enablement Lead | Ready | [09b-enablement-session.md](09b-enablement-session.md) |
| Readiness quiz | Sales Enablement Lead | Waiting: pass mark | [09c-readiness-quiz.md](09c-readiness-quiz.md) |
| Launch checklist | Product Marketing | Ready | [10-launch-checklist.md](10-launch-checklist.md), [10-launch-checklist.csv](10-launch-checklist.csv) |
| Review results and open items | Reviewer | Final | [11-review.md](11-review.md) |

## 12. Results vs goals
To be filled in at L+30, L+60 and L+90.

| KPI | Target | L+30 | L+60 | L+90 |
|---|---|---|---|---|
| Share of active Jira customers opening the activity view | To set | | | |
| Upgrades to the plan that includes Agent Rollback | To set | | | |
| New opportunities citing AI governance | To set | | | |
| Reps passing the readiness quiz | To set | | | |
| What we learned | | | | |

<sub>Drafted by Launch CoPilot: 11 agents, reviewed before release.</sub>
