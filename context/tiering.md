# Launch tiering rubric (the GTM playbook)

Score every release on five criteria, 1 (low) to 5 (high). Explain each score in one line, citing the input or context.

| Criterion | What it measures | Weight |
|---|---|---|
| Customer reach | How much of the base can use it on day one | 25% |
| Commercial impact | Pipeline, expansion or retention it can move | 25% |
| Strategic fit | How directly it serves the company's stated growth drivers in `company.md` | 20% |
| Competitive weight | Whether it opens or closes a gap against the alternatives | 15% |
| Story value | Whether it gives the market a reason to pay attention now | 15% |

**Weighted score** = sum of (score x weight). Range 1.0 to 5.0.

## Tiers
| Tier | Weighted score | What it gets |
|---|---|---|
| Tier 1 | 4.0 and above | Full launch: full campaign strategy, all channel copy, all visuals, full sales enablement with rep session and quiz, external announcement, full checklist |
| Tier 2 | 2.8 up to, but not including, 4.0 | Targeted launch: campaign strategy, email, in-app, release note, LinkedIn post, four visuals, sales kit with rep session and quiz, checklist |
| Tier 3 | Below 2.8 | Quiet release: short campaign strategy, in-app message and banner, release note, a short Sales FYI, checklist |

## Overrides
The Campaign Strategy agent may move a release up or down one tier for a stated reason, such as a competitive event, a regulatory deadline or a dependency on another launch. Any override must be written in the campaign strategy and the run report.

## Asset matrix
| Asset | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| Launch brief, launch context, audience, positioning, messaging | Full | Full | Full |
| Campaign strategy | Full | Full | Short |
| Customer email | Yes | Yes | No |
| In-app message | Yes | Yes | Yes |
| Release note | Yes | Yes | Yes |
| Blog post outline | Yes | No | No |
| LinkedIn post | Yes | Yes | No |
| Sales one-pager | Yes | Yes | No |
| Talk track and objections | Yes | Yes | No |
| Enablement session plan (30 min) | Yes | Yes | No |
| Readiness quiz | Yes | Yes | No |
| Sales FAQ | Yes | Yes | No |
| Sales FYI (short) | No | No | Yes |
| Launch checklist CSV | Yes | Yes | Yes |
| **Visual assets** | | | |
| Email header | Yes | Yes | No |
| In-app banner | Yes | Yes | Yes |
| LinkedIn image | Yes | Yes | No |
| One-pager layout | Yes | Yes | No |
| Blog hero image | Yes | No | No |

Each visual gets a design brief (`08-design-briefs.md`) and is rendered as an SVG and a PNG in `visuals/`.
