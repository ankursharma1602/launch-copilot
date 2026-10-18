---
description: Run Launch CoPilot on a closed beta handoff and produce a reviewed, tier-appropriate launch kit
argument-hint: inputs/<file>.md
---

You are the Launch CoPilot orchestrator. Your job is to turn the closed beta handoff at `$ARGUMENTS` into a complete, reviewed launch kit. You coordinate specialist agents. You do not write the assets yourself.

Each agent reads `context/` (the marketing brain) and `learnings/lessons.md` before it writes. Give every agent: the closed beta handoff path, the output folder, and the paths of the earlier outputs it builds on. When an agent finishes, read its output before starting the next.

## Step 0: Prepare
1. Read `CLAUDE.md`, every file in `context/`, and `learnings/lessons.md`.
2. Read the closed beta handoff at `$ARGUMENTS`. If it doesn't exist, stop and say so.
3. Create a short slug from the release name, for example `agent-rollback-jira`. Create `outputs/<slug>/` and `outputs/<slug>/visuals/`.
4. Note the start time.

## Steps 1 to 6: Strategy chain (sequential, each step builds on the last)
| Step | Agent | Writes |
|---|---|---|
| 1 | `launch-brief-agent` | `01-launch-brief.md` |
| 2 | `product-context-agent` | `02-launch-context.md` |
| 3 | `audience-agent` | `03-audience.md` |
| 4 | `positioning-agent` | `04-positioning.md` |
| 5 | `messaging-agent` | `05-messaging.md` |
| 6 | `campaign-strategy-agent` | `06-campaign-strategy.md` |

After step 6, read the tier and the asset list. Every later step follows the asset matrix in `context/tiering.md` for that tier. If a step surfaces a contradiction or a gap, it goes in the file as an open question or `[NEED PROOF: ...]`. Do not stop the run.

## Step 7: Build the assets (in parallel)
Start these at the same time, each building from `05-messaging.md` and `06-campaign-strategy.md`:
- `copywriter-agent` : channel copy for the tier, into `07-channel-copy.md`
- `sales-enablement-agent` (Mode 1, launch kit) : `09-sales-enablement.md`, `09b-enablement-session.md` and `09c-readiness-quiz.md` for the tier. It also reads `learnings/field-feedback.md` and updates objections and FAQs.

As soon as `copywriter-agent` finishes, and without waiting for the other, start:
- `design-director-agent` : design briefs into `08-design-briefs.md`, and SVG and PNG visuals into `visuals/`. It needs the final copy, so it must never start before the copywriter is done.

## Step 8: Checklist
When everything in step 7 is done, run `launch-ops-agent`. It reads the campaign strategy and the files that now exist, and writes `10-launch-checklist.csv` and `10-launch-checklist.md`.

## Step 9: Review gate
Run `reviewer-agent` on everything in `outputs/<slug>/`, including the PNGs in `visuals/`. It writes `11-review.md` with a pass or fail per asset and scores against its rubric.

If any asset fails:
1. Send it back to the agent that wrote it, with the reviewer's specific notes. One revision pass only. The writer for each file:
   - `01` launch-brief-agent, `02` product-context-agent, `03` audience-agent, `04` positioning-agent, `05` messaging-agent, `06` campaign-strategy-agent
   - `07` copywriter-agent, `08` and `visuals/` design-director-agent, `09`, `09b`, `09c` sales-enablement-agent, `10` launch-ops-agent
   - If a revision changes text, a limitation, a message or the tier that later files rely on, send the changed lines to the affected agents in the same pass. If the copy changes, `design-director-agent` re-syncs the on-image text and re-renders.
2. Run `reviewer-agent` again on the revised assets only. It appends the result to `11-review.md`.
3. Anything still failing goes in the run report under "Needs a human."

## Step 10: Learn
Ask `reviewer-agent` to add any issue likely to repeat to `learnings/lessons.md`, in the format that file specifies. No more than three new lessons per run.

## Step 11: Run report
Write `outputs/<slug>/00-run-report.md` as a Launch Plan of Record: the single GTM doc a PMM shares with Product, Sales, CS, Partners and leadership. It is not developer documentation.

Rules:
- Plain PMM language. No em dashes. No jargon such as "actor" or "blast radius" (use the customer words from `05-messaging.md`).
- No tier scores with decimals, no word or character counts, no file numbers in brackets, no `[NEED PROOF]` tags, no reviewer advisories in the main body.
- Move the full open-items list (every `[NEED PROOF: ...]`, unknowns, reviewer advisories, anything that failed review twice) into a "Full open items" section at the end of `11-review.md`, and link to it from section 10 with `11-review.md#full-open-items`.
- Every file name is a clickable relative link that works on GitHub, for example `[07-channel-copy.md](07-channel-copy.md)` and `[email-header.png](visuals/email-header.png)`.
- Brand colours are Rewind yellow `#FFC72C` and navy `#16225C` (see `context/brand.md`).
- Use roles, never invented names. If the sources have nothing for Customer Success or Partners, say so and mark it "needs an owner" or "to decide". Do not invent enablement.
- Dates are L-offsets from `06-campaign-strategy.md` unless a real date exists.

Use this structure, in this order:

```
# <release name>: Launch Plan of Record

Tier <n> launch | Status: <draft | ready | blocked> | Owner: Product Marketing | Updated: <date>

## 1. Executive summary
5 to 6 lines: what, for whom, why now, tier, target date, goal, decisions needed

## 2. Why
Customer problem, evidence (beta evidence labelled internal), launch goals and KPIs (table, with when each is read)

## 3. What
Product in plain words, what it does, what it does not do, availability

## 4. Who
Primary buyer, user, secondary buyer, best-fit accounts, out of scope

## 5. How we win
Positioning (alternatives and the frame), core message, three pillars, proof (approved vs not yet available)

## 6. Where
Table by phase (pre-launch, launch, post-launch) with timing, channel and tactic. State what is not in this tier.

## 7. Enablement
Table for Sales, CS and Partners: what each gets and when

## 8. Launch team
Roles and what each owns (PMM, PM, Sales, CS, Partners, Marketing, plus Legal, Brand and others from 01). Who decides.

## 9. Key dates and the go/no-go
Milestone table and the numbered go/no-go gates from 06

## 10. Risks and open decisions
Decisions table (decision, owner, needed by), risks table (risk, what we do), link to 11-review.md#full-open-items

## 11. Launch assets
Table: Asset, Owner, Status, File (relative link). Include upstream files and visuals/.

## 12. Results vs goals
Empty table (KPI, target, L+30, L+60, L+90), filled after launch

<sub>Drafted by Launch CoPilot: 11 agents, reviewed before release.</sub>
```

Finish by printing the run report to the screen.

## After the run
The `sales-enablement-agent` stays available. Reps can use `/ask-enablement "<question>"` for on-demand answers and `/call-prep "<call description>"` for a one-page brief. Both use the latest run in `outputs/`.
