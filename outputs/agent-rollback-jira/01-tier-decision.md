# Tier decision: Agent Rollback for Jira

> Based on a HYPOTHETICAL PRD (`inputs/rewind-agent-rollback-jira.md`) and demo context. Not a real Rewind product.

| Criterion | Score (1-5) | Weight | Reason |
|---|---|---|---|
| Customer reach | 3 | 25% | Jira Cloud only, Confluence has no date (input, Availability). It is gated to one plan tier that isn't named yet, and it matters most to customers running AI agents or heavy automation (input, Who it's for). That is a real slice of the base, but only part of Rewind's 16 apps and 25,000+ organizations (company.md). |
| Commercial impact | 4 | 25% | It is built as an upgrade driver ("upgrades to the plan that includes Agent Rollback within 90 days") and a new pipeline source ("AI governance cited as a buying reason") (input, Success metrics). It also gives the IT or security leader, the economic buyer, a reason to approve AI rollouts (personas.md #2). Not a 5: plan names and pricing are unknown, so the size of the upgrade can't be judged yet. |
| Strategic fit | 5 | 20% | It hits two of the CEO's three named growth drivers at once: the Atlassian cloud migration (Jira Cloud) and AI agents acting directly on SaaS data, "which creates new rollback and recovery needs" (company.md). |
| Competitive weight | 4 | 15% | It opens a clear gap against Atlassian's native Backup and Restore, which "works at the site level and has no actor-based rollback" (input, Competitive notes). It extends Rewind's existing "restore a single ticket without touching anything else" position (company.md). Not a 5: the check on other third-party backup tools is still `[NEED PROOF: competitor capability check]`. |
| Story value | 4 | 15% | "AI agents now edit Jira at a scale no human does" gives the market a reason to pay attention now (input, Problem; company.md growth driver 3). It isn't a 5 yet: there's no GA date, no customer story and no approved metric to anchor an announcement (proof-points.md, Not yet approved). |

**Weighted score:** (3 x 0.25) + (4 x 0.25) + (5 x 0.20) + (4 x 0.15) + (4 x 0.15) = 0.75 + 1.00 + 1.00 + 0.60 + 0.60 = **3.95**

**Tier:** 2

3.95 is below the Tier 1 threshold of "4.0 and above." It also falls in a gap in the rubric, since Tier 2 is written as "2.8 to 3.9." I read the 4.0 floor as hard, so 3.95 maps to Tier 2. This is flagged for a human in the brief's Open questions.

**Override:** None.

I considered moving it up one tier because of how well it fits strategy. `context/tiering.md` allows overrides for "a competitive event, a regulatory deadline or a dependency on another launch." None of these is documented in the input or context. Strategic fit alone is already counted in the score, so counting it again through an override would be double counting.

## What this tier gets
- Launch brief (full)
- Customer email
- In-app message
- Release note
- LinkedIn post
- Sales one-pager
- Talk track and objections
- Sales FAQ
- Launch checklist CSV

## What it deliberately does not get
- **Blog post outline.** Without a GA date, a customer story or an approved metric, a long-form post would be built mostly on `[NEED PROOF]` gaps. Add it when there is a story to tell.
- **External announcement / press.** A Tier 1 item. With no third-party competitor check and no customer proof, a public "first" claim can't be backed up.
- **Sales FYI (short).** Tier 3 only. Sales gets the full one-pager, talk track and FAQ, because this feature opens a new conversation with the IT or security buyer.

## What would change the tier
- **Up to Tier 1:** a confirmed competitor capability check showing no third-party tool does actor-based rollback, or a named design-partner customer with an approved result. Either one lifts Competitive weight or Story value to 5, and the score clears 4.0. A documented competitive event (for example, a rival announcing something similar) would also justify an override.
- **Down toward the Tier 2 floor:** if the feature is gated to a top plan that only a small share of Jira customers hold, Customer reach drops to 2 (score 3.70). That is still Tier 2, but the launch should then lean more on the upgrade motion.
