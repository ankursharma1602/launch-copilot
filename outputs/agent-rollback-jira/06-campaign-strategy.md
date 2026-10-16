# Campaign strategy: Agent Rollback for Jira

**Builds on:** 01-launch-brief.md to 05-messaging.md | **Rubric:** context/tiering.md | **Launch day:** L ([NEED PROOF: GA date])

> Agent Rollback is a hypothetical product from a mock handoff. Closed beta numbers are mock, internal and from 11 enabled accounts. In this file they inform the reach and story reasoning only. They are not proof, they do not set a target, and they do not appear in any customer-facing asset. [NEED PROOF: approval to use closed beta results or quotes]

## Tier decision

| Criterion | Score (1-5) | Weight | Reason |
|---|---|---|---|
| Customer reach | 3 | 25% | Jira Cloud only, and only customers with Rewind backup running can use it (02, limitations 1 and 3). It sits at "a specific plan tier", so not every Jira customer gets it on day one. [NEED PROOF: plan names and pricing] [NEED PROOF: number of Rewind Jira Cloud customers on that tier] Rewind covers Jira, Confluence, GitHub and Shopify (`context/proof-points.md`), so Jira Cloud is one slice of the base. |
| Commercial impact | 4 | 25% | The handoff ties it to expansion (upgrades to the plan that includes it) and to pipeline (AI governance as a buying reason), section 1. Held at 4, not 5: there is no baseline or target, the plan and price are not set, and revenue operations cannot yet capture the pipeline signal (Slack thread). |
| Strategic fit | 5 | 20% | Direct answer to growth driver 3, "AI usage: AI agents now act directly on SaaS data, which creates new rollback and recovery needs" (`context/company.md`). It is built in Jira, where Rewind already sells backup. |
| Competitive weight | 3 | 15% | `context/company.md` supports the gap between site-level recovery and a targeted restore. But "no actor-based rollback" in Atlassian's tool has no source, and the competitor check is not done (02, disagreements 2). A closed gap in the story, not yet a proven one. [NEED PROOF: source for native tool capability] [NEED PROOF: competitor capability check] |
| Story value | 5 | 15% | AI agents editing SaaS data is the company's own reason to pay attention now (`context/company.md`, driver 3). The demo opened with an agent reclassifying 4,000 issues and the preview got the room's reaction (handoff section 3). In the closed beta, 5 of 11 accounts ran a rollback (mock, small sample), which supports that the story lands. It does not prove it. |

**Weighted score:** (3 x 0.25) + (4 x 0.25) + (5 x 0.20) + (3 x 0.15) + (5 x 0.15) = 0.75 + 1.00 + 1.00 + 0.45 + 0.75 = **3.95**

**Boundary check:** Tier 1 is 4.0 and above. Tier 2 is 2.8 up to, but not including, 4.0. Tier 3 is below 2.8. 3.95 is below 4.0 and above 2.8, so it lands in exactly one tier: Tier 2. It is 0.05 under the Tier 1 line. Sensitivity: one more point on Customer reach (4) gives 4.20, which would be Tier 1. One less point on Story value (4) gives 3.80, still Tier 2. Reach is the swing score. It is scored 3 because the size of the eligible base is unknown, and the rubric asks how much of the base can use it on day one.

**Tier:** 2 (targeted launch)

**Override:** None. `context/tiering.md` allows an override only for a stated reason such as a competitive event, a regulatory deadline or a dependency on another launch. None applies. The handoff names no competitive event or deadline. The dependencies (pricing, Legal, Support wording) block copy, but they are not another launch. A near-miss on the Tier 1 threshold is not a listed reason, so the score stands.

### What this tier gets
- Full strategy (this file) on top of the full upstream set, 01 to 05.
- Customer email, in-app message, release note and LinkedIn post.
- Sales kit: one-pager, talk track and objections, sales FAQ, a 30 minute enablement session plan and a readiness quiz.
- Four visuals: email header, in-app banner, LinkedIn image, one-pager layout.
- Launch checklist (CSV and a readable version).

### What it deliberately does not get
- **Blog post outline and blog hero image.** Tier 1 only. The proof the story needs (outcomes, customer evidence, a sourced competitor claim) does not exist yet, so a long-form piece would be forced to rely on claims we cannot make. The email and LinkedIn post carry the story at the size the evidence supports.
- **Sales FYI (short).** Tier 3 only. Reps need the full kit: this release comes with seven Must say items that reps need to say out loud (05, Must say), and an FYI cannot carry them.
- **External press or analyst announcement.** Not in the Tier 2 matrix, and no approved customer proof or outcome measure exists to back one.
- **Any use of closed beta numbers or quotes in external assets.** Not approved (`context/proof-points.md`). Customers have not agreed.

### What would change the tier
- **Up to Tier 1:** the eligible base turns out to be large (Customer reach to 4 gives 4.20), or Commercial impact moves to 5 once pricing is set and a baseline and target exist (gives 4.20). Either would need evidence we do not have today.
- **Up to Tier 1 by override:** a competitive event or regulatory deadline tied to AI agents in Jira that Product or Legal can name.
- **Down to Tier 3:** the plan tier turns out to cover a very small share of the base and Story value drops to 3 (gives 3.65, still Tier 2), so a drop would need several scores to fall together. Not expected.
- **Slip, not a tier change:** if the go/no-go gates below are not met, the launch date moves. The tier does not.

## Campaign plan

### Goals
Restated from 01-launch-brief.md for a Tier 2 launch. None has a baseline or target yet.

1. **Adoption.** Existing Rewind Jira Cloud customers on the eligible plan open Actor view in the first 30 days.
2. **Expansion.** Customers upgrade to the plan that includes Agent Rollback within 90 days.
3. **Pipeline.** Sales conversations where AI governance comes up as a buying reason. This goal cannot be measured at L until revenue operations can capture it in the CRM.
4. **Sales readiness (supporting goal for this tier).** Reps can state the value in one breath and say every limit without being asked, before L.

### Audience
From 03-audience.md.
- **Primary:** the Atlassian admin. Runs the rollback, makes the case. Lead with the moment of failure and the two bad options (restore the whole site or fix it by hand), then the way out.
- **Secondary:** the IT or security leader. Approves the plan tier and the AI rollout. Gets the recovery plan and audit log framing. No separate campaign: the admin carries the message to them.
- **Segments to reach first:** existing Rewind Jira Cloud backup customers; Jira Cloud sites with heavy automation; teams rolling out AI agents; regulated industries on Jira Cloud. Do not target sites above Atlassian's size limits or needing data types beyond issues and fields until those answers exist.
- **Not targeted:** Confluence-only admins, teams without Rewind backup on Jira Cloud, buyers who want ROI proof.
- **Message rule:** name the actor broadly: a rule, an integration or an AI agent. AI is the reason the safety net matters, never the problem.

### Channels
Timing is relative to launch day L.

| Channel | Job | Asset | Owner (role) | When |
|---|---|---|---|---|
| Customer email | Tell existing Jira Cloud backup customers what they get back and what the limits are. Main route to the admin. | Customer email + email header | Product marketing (lifecycle) | L |
| In-app message and banner | Reach admins inside Rewind where they already manage backup. Points to the feature. | In-app message + in-app banner | Product marketing, Product manager (Jira) | L |
| Release note | Plain record of what shipped and its known limits. | Release note | Product marketing | L |
| LinkedIn post | Reach admins and IT leaders beyond the customer list. Carries the "two bad options" story. | LinkedIn post + LinkedIn image | Product marketing, Social | L+1 |
| Sales (one to one) | Move the secondary persona: the approver. Rep walks the admin and approver through the preview and audit log. | One-pager, talk track and objections, FAQ | Sales, Sales Engineering | Kit delivered L-10, used from L |
| Sales enablement | Get reps ready before customers ask. | Session plan (30 min) + readiness quiz | Sales enablement lead | Session L-7, quiz L-5 |

Every customer-facing asset carries the Must say items from 05-messaging.md in its copy: after your first Rewind backup only, attachments (handoff wording only), Jira Cloud, specific plan tier. Short assets write these first (lessons.md).

### Assets in scope
Exactly the Tier 2 column of the asset matrix in `context/tiering.md`.

| Asset | In scope? | File |
|---|---|---|
| Launch brief, launch context, audience, positioning, messaging | Yes (done) | 01-launch-brief.md, 02-launch-context.md, 03-audience.md, 04-positioning.md, 05-messaging.md |
| Campaign strategy (full) | Yes | 06-campaign-strategy.md |
| Customer email | Yes | 07-channel-copy.md |
| In-app message | Yes | 07-channel-copy.md |
| Release note | Yes | 07-channel-copy.md |
| LinkedIn post | Yes | 07-channel-copy.md |
| Sales one-pager | Yes | 09-sales-enablement.md |
| Talk track and objections | Yes | 09-sales-enablement.md |
| Sales FAQ | Yes | 09-sales-enablement.md |
| Enablement session plan (30 min) | Yes | 09b-enablement-session.md |
| Readiness quiz | Yes | 09c-readiness-quiz.md |
| Launch checklist CSV | Yes | 10-launch-checklist.csv (readable copy: 10-launch-checklist.md) |
| **Visual assets** | | |
| Email header | Yes | Brief in 08-design-briefs.md, render in `visuals/` as SVG and PNG |
| In-app banner | Yes | Brief in 08-design-briefs.md, render in `visuals/` as SVG and PNG |
| LinkedIn image | Yes | Brief in 08-design-briefs.md, render in `visuals/` as SVG and PNG |
| One-pager layout | Yes | Brief in 08-design-briefs.md, render in `visuals/` as SVG and PNG |

**Not produced (Tier 2):** blog post outline, blog hero image, Sales FYI (short). Downstream agents must not create these.

**Rules for the visuals (for the design director and copywriter):**
- Limitations and disclaimers go in the accompanying copy (email body, in-app message body, LinkedIn post text). They never appear on the email header, the in-app banner or the LinkedIn image.
- The one-pager layout is the only visual that may carry a limits line, and only one small line.
- On-image text stays within the word cap and is written in 07-channel-copy.md so design renders it unchanged (lessons.md).
- No beta numbers, quotes or percentages on any visual. Brand hex codes and typeface are unconfirmed (`context/brand.md`), so no visual leaves the team until the brand team confirms. [NEED PROOF: confirm brand hex codes and typeface]
- Because the image cannot hold the limits, no image headline may claim "every change", "everything", speed, or an "only" or "first" position.

### Timeline
One set of offsets, used by every downstream file, including the checklist. Copy these word for word. GA date is unknown, so all dates are relative to L.

| Phase | Window | What happens |
|---|---|---|
| Build window | L-28 to L-18 | Copy (07), design briefs and visuals (08), sales kit (09, 09b, 09c) and checklist (10) are drafted. Open questions are chased to owners. |
| Final review | L-17 to L-14 | Reviewer agent pass, then one revision pass. Legal reviews "exportable for auditors" and any Confluence mention. Support confirms attachment wording. Brand team confirms visual identity. |
| Kit delivery | L-10 | Sales kit delivered to Sales and Sales Engineering: one-pager, talk track and objections, FAQ. |
| Enablement session | L-7 | 30 minute live session for reps (09b). |
| Readiness quiz | L-5 | Quiz (09c) due from reps. Gaps feed `learnings/field-feedback.md`. |
| Go/no-go | L-3 | Decision meeting against the gates below. |
| Launch | L | Email, in-app message and banner, and release note go live. |
| Launch +1 | L+1 | LinkedIn post and image go live. |
| Adoption check | L+30 | Read Actor view opens. |
| Expansion check | L+90 | Read upgrades to the plan that includes Agent Rollback. |

**Go/no-go gates (all must be met at L-3, or the date moves):**
1. GA date confirmed. [NEED PROOF: GA date]
2. Plan tier wording settled. Either the plan name and price are confirmed, or the approved line is "a specific plan tier". [NEED PROOF: plan names and pricing]
3. Legal has cleared "exportable for auditors" and any Confluence line, or both are removed from copy. [NEED PROOF: Legal approval]
4. Support, Product manager (Jira) and Engineering lead have decided the attachment wording. [NEED PROOF: plain wording for the attachment limitation, including the 24-hour phrase]
5. Brand team has confirmed colours and typeface. [NEED PROOF: confirm brand hex codes and typeface]
6. Product analytics can count Actor view opens for the L+30 read.

Not a gate: approval to use beta numbers and quotes. The kit does not use them, so the launch does not wait for it.

### Success metrics
From the handoff, section 1 (proposed). None has a baseline or target. Leading metrics are added by this plan and are marked as such.

| Metric | Type | Baseline | Target | Source |
|---|---|---|---|---|
| % of active Jira customers who open Actor view within 30 days of L | Leading (adoption), read at L+30 | [NEED PROOF: baseline] | [NEED PROOF: target] | Handoff section 1 |
| Upgrades to the plan that includes Agent Rollback within 90 days of L | Lagging (expansion), read at L+90 | [NEED PROOF: current upgrade rate] | [NEED PROOF: target] | Handoff section 1 |
| New opportunities where AI governance is cited as a buying reason | Lagging (pipeline), read at L+90 | [NEED PROOF: baseline; not captured in CRM today] | [NEED PROOF: target] | Handoff section 1; Slack thread (revenue operations) |
| Reps who complete the readiness quiz by L-5 | Leading (sales readiness). Added by this plan, not in the handoff. | Not applicable, new | [NEED PROOF: pass mark and target share of reps] | This plan |
| Email click-through to the feature, and in-app banner clicks | Leading (reach). Added by this plan, not in the handoff. | [NEED PROOF: current Rewind email and in-app benchmarks] | [NEED PROOF: target] | This plan |

Notes on the numbers:
- The closed beta (9 of 11 accounts opened Actor view, 5 of 11 ran a rollback) is mock, from a small internal group. It must not be used as a baseline or a target. The sample is 11 accounts and the handoff does not say how they were chosen.
- The adoption metric needs a denominator: "active Jira customers" may mean all Jira customers or only those on the eligible plan. [NEED PROOF: definition of "active Jira customers" for the adoption metric]
- The pipeline metric cannot be read until revenue operations can capture the buying reason. If that is not fixed by L, the L+90 read is reported as "not measurable".

### Risks and dependencies

| Risk or dependency | Effect | Mitigation | Owner (role) |
|---|---|---|---|
| GA date not set | No date can be committed, every offset floats | All dates are L-offsets. Go/no-go at L-3 | Product manager (Jira) |
| Plan name and price not set | Email and in-app have no clear next step, expansion goal cannot be read | Use "a specific plan tier". Call to action points to the account team or release note until set. [NEED PROOF: how a customer turns the feature on, and whether it needs setup] | Pricing and packaging |
| Attachment wording conflict ("up to 24 hours old" against "recovery points under 24 hours") | Reads as a contradiction, or overclaims | Handoff wording only. No "under 24 hours" next to Agent Rollback. Decision is a go/no-go gate | Support lead, Product manager (Jira), Engineering lead |
| No source for "Atlassian native has no actor-based rollback" | A competitive claim that cannot ship, and a risk of implying Atlassian is unreliable | Say native works at the site level and Rewind sits on top. No "no actor-based rollback" in any asset | Sales Engineering |
| No customer proof or outcome measure | Story rests on capability only. Email and LinkedIn read thinner | Lead with the failure moment and the two bad options. No faster, no minutes, no ROI | Product marketing |
| Limits get lost in short assets | Overclaim, and reps are surprised by customers | Limits written first in every asset. Images carry none, so the paired copy must carry all | Copywriter, Reviewer |
| Customers misread the first-backup limit | Two beta accounts (mock) did not understand it at first | State it plainly in email, in-app body, one-pager line, FAQ and talk track | Support lead, Product marketing |
| Permission model undecided | IT and security buyers ask first | Do not state one. FAQ answer is "being decided", with [NEED PROOF: who can run a rollback] | Customer success, Product manager (Jira) |
| Unknown behavior: same-field edits, large sites, data types beyond issues and fields | Keep-human-work and scale claims could overreach | Keep to what the demo showed. Do not carry the backup large-site claim over | Engineering lead |
| Legal review late | Audit and Confluence wording blocks copy | Review runs L-17 to L-14. Fallback: remove both phrases | Legal |
| Brand identity unconfirmed | Visuals cannot leave the team | Brand team confirms by final review. Wordmark is set in type, not the logo file | Brand team |
| Rules outnumbered agents in the closed beta (12 and 8 of 23, mock) | An AI-only story would miss many admins | Name the actor broadly. Treat AI as the growing case. Small sample, not a finding | Product marketing |
| Pipeline metric cannot be captured in the CRM | Goal 3 unmeasurable at L+90 | Ask revenue operations for a field before L | Revenue operations |
| Reach is the swing score (3.95 against a 4.0 line) | A larger eligible base could justify more | Re-score at go/no-go if the eligible base is sized. Do not add assets mid-build without a re-score | Campaign strategy |

### What we are not doing
- No blog post outline, blog hero image or Sales FYI (tier matrix).
- No customer logos, quotes, beta numbers or percentages in any asset. Not approved.
- No claim that Atlassian's native tool lacks anything. No "only", "first" or "no other tool" claim. No claim about other third-party tools.
- No time saved, restore time or ROI claim.
- No Confluence date, quarter or "coming soon". Only the Legal-approved roadmap line, if cleared.
- No permission model, no explanation of how Actor view tells actor types apart, no claim about large sites.
- No limitations or disclaimers on the email header, in-app banner or LinkedIn image. They live in the paired copy. Only the one-pager layout carries one small limits line.
- No separate campaign for the IT or security leader or the AI owner. The admin carries the message, and Sales handles the approver one to one.
- No paid media. It is not in the Tier 2 matrix and there is no budget or target to size it. [NEED PROOF: budget and paid media targets]
