# Campaign strategy: Agent Rollback for Jira

> The PRD marks this as a hypothetical release written to demo Launch CoPilot. Treat it as a mock Rewind product. GA date is [NEED PROOF: GA date], so all timing uses L-offsets from launch day (L).

## Tier decision

| Criterion | Score (1-5) | Weight | Reason |
|---|---|---|---|
| Customer reach | 2 | 25% | Jira Cloud only (PRD, Availability), included only at one plan tier ([NEED PROOF: plan names and pricing]), and it needs an existing Rewind Jira Cloud backup (`02-launch-context.md`, Dependencies). Day-one users are a slice of the Jira base. Slice size: [NEED PROOF: current plan mix]. |
| Commercial impact | 4 | 25% | Two of three PRD metrics are commercial: upgrades to the including plan within 90 days, and new opportunities citing AI governance (PRD, Success metrics). It is an upgrade lever and a pipeline reason. No baseline or target is given, so not a 5. |
| Strategic fit | 5 | 20% | Directly serves growth driver 3, AI usage, in `context/company.md`: AI agents act on SaaS data and create new rollback needs. This is the feature built for it. |
| Competitive weight | 3 | 15% | Closes a gap against the whole-site restore that native works at (`context/company.md`, PRD, Problem). Other third-party tools are unchecked ([NEED PROOF: competitor capability check]), and the "no actor-based rollback" claim about native has no source, so it cannot be scored higher. |
| Story value | 4 | 15% | A clear reason to pay attention now: agents and automation edit Jira at a scale no human does (PRD, Problem) and approvers want a recovery plan before they say yes (PRD, Who it's for). No market data backs it (`04-positioning.md`, section 6), so not a 5. |

**Weighted score:** (2 x 0.25) + (4 x 0.25) + (5 x 0.20) + (3 x 0.15) + (4 x 0.15) = 0.50 + 1.00 + 1.00 + 0.45 + 0.60 = **3.55**
**Tier:** 2 (3.55 is at least 2.8 and below 4.0, so it lands in exactly one tier. It is 0.45 below the Tier 1 line and 0.75 above the Tier 3 line.)
**Override:** None. No competitive event, regulatory deadline or launch dependency listed in `context/tiering.md` applies. The open items (GA date, pricing, competitor check) are information gaps, not overrides.

### What this tier gets
- Full upstream set: launch brief, launch context, audience, positioning, messaging (done, files 01 to 05).
- Full campaign strategy (this file).
- Customer email, in-app message, release note, LinkedIn post.
- Sales one-pager, talk track and objections, 30-minute enablement session plan, readiness quiz, sales FAQ.
- Launch checklist CSV.
- Four visuals, each with a design brief and rendered as SVG and PNG: email header, in-app banner, LinkedIn image, one-pager layout.

### What it deliberately does not get
- **Blog post outline and blog hero image.** These are Tier 1 only. The feature reaches a slice of the base and its proof is PRD facts only. A blog would stretch thin evidence and invite claims we cannot source (competitors, speed, customer results).
- **Sales FYI (short).** That is the Tier 3 replacement for the sales kit. This tier gets the full kit because reps will meet the native-restore and "what about attachments" objections.
- **Press, event or paid spend.** Not in the Tier 2 matrix.
- **Any dated, priced or plan-named line.** GA date, plan names and pricing are open. Doing less here is on purpose.

### What would change the tier
- **Up to Tier 1 (4.0 or more):** customer reach rises to 4 and the rest hold, for example if the including tier is the main Jira plan or the base moves to it. Score would be 4.05. Or a competitive event: a named rival ships actor-based rollback (only if the competitor check shows it, and as an override reason under `context/tiering.md`).
- **Down to Tier 3 (below 2.8):** the including tier turns out to be a small add-on and commercial impact drops to 2, competitive weight to 2 and story value to 3. Score would be (2 x 0.25) + (2 x 0.25) + (5 x 0.20) + (2 x 0.15) + (3 x 0.15) = 0.50 + 0.50 + 1.00 + 0.30 + 0.45 = 2.75, below 2.8. Commercial and competitive drops alone give 2.90, which stays Tier 2.

## Campaign plan

### Goals
From `01-launch-brief.md`, restated for Tier 2. None has a baseline or target.
1. **Adoption:** existing Jira Cloud customers open Actor view.
2. **Expansion:** customers on lower plans upgrade to the plan that includes Agent Rollback.
3. **Pipeline:** new opportunities where AI governance is cited as a buying reason.

Message to carry: undo one actor's changes, not the whole site, and keep your people's work (`05-messaging.md`, core message). Every asset carries the four Must say limits where they apply.

### Audience
From `03-audience.md`.
- **Primary:** the Atlassian admin on Jira Cloud. Trigger: an agent or rule made many wrong changes, or the admin is asked to add another one and wants to know they can undo it. Lead pillars 1, then 2.
- **Secondary:** the IT or security leader who approves AI rollouts. Lead pillar 3, then 2.
- **In the story, not the lead target:** the AI or automation owner.
- **Segments to reach first:** existing Rewind Jira Cloud backup customers; Jira Cloud customers running AI agents; customers with heavy automation; companies where IT or security must approve AI rollouts. Sizes: [NEED PROOF: segment sizes].
- **Not targeted:** Confluence-only teams, other platforms, buyers who want to roll back changes from before their first backup, and plan-based targeting of lower-tier customers until the tier and price are named.

### Channels

| Channel | Job | Asset | Owner (role) | When |
|---|---|---|---|---|
| Customer email | Tell existing Rewind Jira Cloud customers what they get back and how to try Actor view. Drives adoption. | Customer email, email header | Product marketing lead, with lifecycle marketing | Send at L. Segment set at L-7. |
| In-app message and banner | Reach admins inside Rewind at the moment they manage Jira backups. Drives Actor view opens. | In-app message, in-app banner | Product marketing lead, with product manager for Jira | Live at L. Ready for QA at L-3. |
| Release note | Give the accurate, complete record of what shipped and what it cannot do. | Release note | Product manager for Jira, reviewed by product marketing lead | Published at L. |
| LinkedIn | Reach admins and IT leaders outside the customer base with the moment-of-failure story. Supports pipeline. | LinkedIn post, LinkedIn image | Product marketing lead, with social owner | Post at L. Follow-up reply handling L to L+7. |
| Sales conversations | Equip reps to open and run AI governance and actor-level recovery conversations. Supports pipeline and expansion. | Sales one-pager, one-pager layout, talk track and objections, sales FAQ | Sales leadership and enablement | Delivered by L-5. |
| Rep enablement session | Make reps confident on limits and the native-restore question before launch. | 30-minute session plan, readiness quiz | Sales leadership and enablement | Session at L-5 to L-3. Quiz by L-2. |

Marketplace listing and partner notices are a dependency, not an asset in this plan (see Risks and dependencies).

### Assets in scope
Downstream agents produce these and only these.

| Asset | File |
|---|---|
| Launch brief | `01-launch-brief.md` (done) |
| Launch context | `02-launch-context.md` (done) |
| Audience | `03-audience.md` (done) |
| Positioning | `04-positioning.md` (done) |
| Messaging | `05-messaging.md` (done) |
| Campaign strategy | `06-campaign-strategy.md` (this file) |
| Customer email | `07-channel-copy.md` |
| In-app message | `07-channel-copy.md` |
| Release note | `07-channel-copy.md` |
| LinkedIn post | `07-channel-copy.md` |
| Sales one-pager | `09-sales-enablement.md` |
| Talk track and objections | `09-sales-enablement.md` |
| Sales FAQ | `09-sales-enablement.md` |
| Enablement session plan (30 min) | `09b-enablement-session.md` |
| Readiness quiz | `09c-readiness-quiz.md` |
| Launch checklist CSV | `10-launch-checklist.csv` (with `10-launch-checklist.md`) |
| Design briefs for the four visuals | `08-design-briefs.md` |
| Visual: email header | `visuals/` (SVG and PNG) |
| Visual: in-app banner | `visuals/` (SVG and PNG) |
| Visual: LinkedIn image | `visuals/` (SVG and PNG) |
| Visual: one-pager layout | `visuals/` (SVG and PNG) |
| Review | `11-review.md` |

**Not produced at this tier:** blog post outline, blog hero image, Sales FYI (short).

Rules for every asset: carry the Must say limits from `05-messaging.md` (first backup, attachments PRD wording, Jira Cloud only with Confluence on the roadmap and no date, specific plan tier). Short assets write the limits in first, then cut other words (lesson, 2026-10-16). No plan name, price or date. No claim that native lacks actor-based rollback, no claim about other tools, no "only" or "first" wording. No customer patterns stated as fact. Headlines lead with what the admin gets back.

### Timeline
Offsets are placeholders for the team to confirm. They are not commitments. GA date: [NEED PROOF: GA date].

| Phase | Window | What happens |
|---|---|---|
| Unblock | Before L-21 | Product supplies GA date. Pricing owner names the plan tier and price. Competitive intelligence finishes the competitor check. A human decides the attachment wording conflict and sources or drops the "no actor-based rollback" claim. Legal reviews "exportable for auditors" and the Confluence roadmap line. Revenue operations confirms the CRM can capture "AI governance cited as a buying reason." |
| Build | L-21 to L-8 | Channel copy, design briefs, visuals, sales kit and checklist built. Final review at L-8. |
| Enable | L-8 to L-3 | Reps get the one-pager, talk track and FAQ by L-5. Enablement session and quiz run L-5 to L-2. |
| Ready | L-3 to L-1 | In-app QA. Email segment and test send. Release note and LinkedIn post approved. Go or no-go at L-1. |
| Launch | L | Release note, in-app message and banner, email and LinkedIn post go live. |
| Sustain | L+1 to L+14 | Watch replies and rep questions. Unanswered rep questions go to `learnings/field-feedback.md`. Fix any copy that misleads on limits. |
| Measure | L+30 and L+90 | Adoption read-out at L+30. Expansion read-out at L+90. Pipeline reviewed at both. |

### Success metrics
Three PRD metrics (adoption, pipeline, expansion), which the PRD labels proposed, plus one working measure. Adoption appears in two rows: the raw count of Actor view opens (working measure) and the % of active Jira customers who open it within 30 days (PRD metric). The PRD gives no baselines or targets.

| Metric | Type | Baseline | Target | Source |
|---|---|---|---|---|
| Opens of Actor view (working measure) | Leading | [NEED PROOF: baseline, current active Jira customer count] | [NEED PROOF: target %] | Working measure, derived from PRD adoption metric |
| % of active Jira customers who open Actor view within 30 days | Leading (read at L+30) | [NEED PROOF: current active Jira customer count and baseline] | [NEED PROOF: target %] | PRD, Success metrics |
| New opportunities where AI governance is cited as a buying reason | Leading to lagging | [NEED PROOF: baseline count, and whether the CRM can capture this reason] | [NEED PROOF: target count] | PRD, Success metrics |
| Upgrades to the plan that includes Agent Rollback within 90 days | Lagging (read at L+90) | [NEED PROOF: current plan mix] | [NEED PROOF: target upgrade count or %] | PRD, Success metrics |

Note: the first row is the raw count behind the adoption %. It is a working measure for the Sustain phase, not a PRD metric, and has no target. Channel-level measures (email open and click, LinkedIn reach) have no baseline: [NEED PROOF: channel baselines]. They are diagnostics, not success measures.

### Risks and dependencies
- **GA date unknown.** No dated line in any asset until product supplies it. Checklist items key off L.
- **Plan names and pricing unknown.** Email, in-app, release note and sales assets can only say "a specific plan tier." The expansion goal cannot be worked without the name. This is the largest dependency.
- **Attachment wording conflict.** PRD says up to 24 hours old. `context/` says recovery points under 24 hours. Use the PRD wording and never pair Agent Rollback with "under 24 hours" until a human decides.
- **Unsourced Atlassian claim.** Say native works at the site level. Do not say it has no actor-based rollback.
- **No competitor check.** No claim about other third-party backup tools, and no "only," "first" or "unique."
- **No customer evidence.** All three pillars rest on PRD facts. No names, quotes, benchmarks or speeds.
- **Engineering unknowns.** Actor-type detection, data types covered, conflicts with later human edits, limits and permissions. Copy stays to "issues and fields" and "AI agent, automation rule or integration" as examples.
- **Audit log wording.** Legal review pending. Say "exportable for auditors" and nothing more.
- **Confluence roadmap line.** Needs sign-off before any public mention.
- **Pipeline metric tracking.** Needs revenue operations to confirm a field or process, or the metric cannot be read.
- **Marketplace and partner listing.** Listing and partner communication are owned by the marketplace and channel owner. Not in the Tier 2 asset matrix, so this plan does not produce them. Confirm whether the listing needs a change at L.
- **Short assets dropping limits.** The most likely failure. See the rules above.

### What we are not doing
- No blog post, blog hero image or Sales FYI. Tier 2 matrix.
- No claims about other third-party backup tools until the competitor check is done.
- No "AI governance product" framing. The sources support a recovery plan and an exportable audit log only.
- No fear-led copy and no framing of AI or automation owners as the problem.
- No plan-based promotion to lower-tier customers until the tier and price are named.
- No Confluence segment, copy or date.
- No paid media, events or press push.
- No targets invented to fill the metrics table.
