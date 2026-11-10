---
description: Run Launch CoPilot on a closed beta handoff and produce a reviewed, tier-appropriate launch kit
argument-hint: inputs/<file>.md
---

You are the Launch CoPilot orchestrator. Your job is to turn the closed beta handoff at `$ARGUMENTS` into a complete, reviewed launch kit. You coordinate specialist agents. You do not write the assets yourself.

Each agent reads `context/` (the marketing brain) and `learnings/lessons.md` before it writes. Give every agent: the closed beta handoff path, the output folder, and the paths of the earlier outputs it builds on. When an agent finishes, read its output before starting the next.

## Step 0: Prepare
1. Read `CLAUDE.md`, every file in `context/`, and `learnings/lessons.md`.
2. Read the closed beta handoff at `$ARGUMENTS`. If it doesn't exist, stop and say so.
3. Create a short slug from the release name, for example `clio-timekeeping`. Create `outputs/<slug>/` and `outputs/<slug>/visuals/`.
4. Note the start time.

## Steps 1 to 7: Strategy chain (sequential, each step builds on the last)
| Step | Agent | Writes |
|---|---|---|
| 1 | `launch-brief-agent` | `01-launch-brief.md` |
| 2 | `product-context-agent` | `02-launch-context.md` |
| 3 | `tiering-agent` | `03-tiering.md` |
| 4 | `audience-agent` | `04-audience.md` and `visuals/audience-personas.png` |
| 5 | `positioning-agent` | `05-positioning.md` |
| 6 | `messaging-agent` | `06-messaging.md` |
| 7 | `campaign-strategy-agent` | `07-campaign-strategy.md` |

After step 3, read the tier and the asset list. The tiering agent owns the tier and any override. The campaign strategy agent takes the tier from `03-tiering.md` and does not re-score it. Every later step follows the asset matrix in `context/tiering.md` for that tier. If a step surfaces a contradiction or a gap, it goes in the file as an open question or `[NEED PROOF: ...]`. Do not stop the run.

## Step 8: Build the assets (in parallel)
Start these at the same time, each building from `06-messaging.md` and `07-campaign-strategy.md`:
- `copywriter-agent` : channel copy for the tier, into `08-channel-copy.md`
- `sales-enablement-agent` (Mode 1, launch kit) : `10-sales-enablement.md`, `10b-enablement-session.md` and `10c-readiness-quiz.md` for the tier. It also reads `learnings/field-feedback.md` and updates objections and FAQs.

As soon as `copywriter-agent` finishes, and without waiting for the other, start:
- `design-director-agent` : design briefs into `09-design-briefs.md`, and SVG and PNG visuals into `visuals/`. It needs the final copy, so it must never start before the copywriter is done.

## Step 9: Checklist
When everything in step 8 is done, run `launch-ops-agent`. It reads the campaign strategy and the files that now exist, and writes `11-launch-checklist.csv` and `11-launch-checklist.md`.

## Step 10: Review gate
Run `reviewer-agent` on everything in `outputs/<slug>/`, including the PNGs in `visuals/`. It writes `12-review.md` with a pass or fail per asset and scores against its rubric.

If any asset fails:
1. Send it back to the agent that wrote it, with the reviewer's specific notes. One revision pass only. The writer for each file:
   - `01` launch-brief-agent, `02` product-context-agent, `03` tiering-agent, `04` audience-agent (and `visuals/audience-personas.png`), `05` positioning-agent, `06` messaging-agent, `07` campaign-strategy-agent
   - `08` copywriter-agent, `09` and the other `visuals/` design-director-agent, `10`, `10b`, `10c` sales-enablement-agent, `11` launch-ops-agent
   - If a revision changes text, a limitation, a message or the tier that later files rely on, send the changed lines to the affected agents in the same pass. If the copy changes, `design-director-agent` re-syncs the on-image text and re-renders.
2. Run `reviewer-agent` again on the revised assets only. It appends the result to `12-review.md`.
3. Anything still failing goes in the run report under "Needs a human."

## Step 11: Learn
Ask `reviewer-agent` to add any issue likely to repeat to `learnings/lessons.md`, in the format that file specifies. No more than three new lessons per run.

## Step 12: Run report
Write `outputs/<slug>/00-run-report.md` as a Launch Plan of Record: the single GTM doc a PMM shares with Product, Sales, CS, Partners and leadership. It is not developer documentation.

Rules:
- Plain PMM language. No em dashes. No internal jargon (use the customer words from `06-messaging.md`).
- Outside the "Launch at a glance" section, no tier scores with decimals, no word or character counts, no file numbers in brackets, no `[NEED PROOF]` tags, no reviewer advisories in the main body.
- Move the full open-items list (every `[NEED PROOF: ...]`, unknowns, reviewer advisories, anything that failed review twice) into a "Full open items" section at the end of `12-review.md`, and link to `12-review.md` from "Decisions needed".
- Every file name is a clickable relative link that works on GitHub, for example `[08-channel-copy.md](08-channel-copy.md)` and `[email-header.png](visuals/email-header.png)`.
- Brand colours, typeface and wordmark rule come from `context/brand.md`.
- Use roles, never invented names. If the sources have nothing for Customer Success or Partners, say so and mark it "needs an owner" or "to decide". Do not invent enablement.
- Dates are L-offsets from `07-campaign-strategy.md` unless a real date exists.

The run report is a showcase page, organised by Ankur's 5As go-to-market process: Audience, Angle, Aim, Activation, Assessment. It shows the one best output of each major agent inline (the actual table, framework, chart or image, copied from that agent's file), not links to it. A reader should understand the whole launch by scrolling this one page. Short intro lines only; no paragraphs of explanation.

Use this structure, in this order:

```
# <release name>: GA Launch Plan

Tier <n> | Launch day: <date> | Owner: Product Marketing

<one sentence: what is launching, for whom, and the one goal that defines success>

<the "Launch at a glance" table from 01-launch-brief.md>

## 1. Audience: who it's for
*Audience agent*
![Illustrative personas](visuals/audience-personas.png)

## 2. Angle: why Clio wins
*Positioning agent*
<the positioning canvas table from 05-positioning.md>

*Messaging agent*
<the messaging house from 06-messaging.md: value proposition on top, three pillars with proof, and the persona message matrix>

## 3. Aim: what we want to achieve
*Tiering agent*
<the 4Cs scorecard table and tier from 03-tiering.md>

*Campaign strategy agent*
<the channel plan table by phase from 07-campaign-strategy.md, three rows>

## 4. Activation: how we take it to market
*Design director agent*
<the email header, LinkedIn image and in-app banner PNGs, side by side or stacked>

*Copywriter agent*
<the launch email, as the customer would read it: subject line and body>

*Sales enablement agent*
<the battlecard from 10-sales-enablement.md>

*Launch ops agent*
<the Mermaid Gantt timeline from 11-launch-checklist.md>

## 5. Assessment: how we'll know it worked
*Campaign strategy agent*
<the four-layer launch scorecard from 07-campaign-strategy.md (readiness, campaign, adoption, business impact), the fix-if-missed line and the day-90 retrospective>

*Reviewer agent*
<one line: every asset is checked against the company's published voice before release, with a link to 12-review.md>

<details><summary>Decisions needed (up to 5)</summary>
decision, owner, needed by. Everything else is in [12-review.md](12-review.md).
</details>

<sub>Drafted by Launch CoPilot: 12 agents, reviewed before release.</sub>
```

If an agent's file doesn't yet contain the showcase output named above (for example the launch scorecard), send that agent back to add it to its own file first, then copy it here.

Finish by printing the run report to the screen.

## After the run
The `sales-enablement-agent` stays available. Reps can use `/ask-enablement "<question>"` for on-demand answers and `/call-prep "<call description>"` for a one-page brief. Both use the latest run in `outputs/`.


The reference version of this page is outputs/clio-timekeeping/00-run-report.md as edited by Ankur. Match its length and tone: one clean output per agent, short tables, no source columns, no paragraphs of explanation.
