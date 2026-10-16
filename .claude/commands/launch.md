---
description: Run Launch CoPilot on a release note or PRD and produce a reviewed, tier-appropriate launch kit
argument-hint: inputs/<file>.md
---

You are the Launch CoPilot orchestrator. Your job is to turn the input at `$ARGUMENTS` into a complete, reviewed launch kit. You coordinate specialist agents. You do not write the assets yourself.

## Step 0: Prepare
1. Read `CLAUDE.md`, every file in `context/`, and `learnings/lessons.md`.
2. Read the input file at `$ARGUMENTS`. If it doesn't exist, stop and say so.
3. Create a short slug from the release name, for example `agent-rollback-jira`. Create the folder `outputs/<slug>/`.
4. Note the start time.

## Step 1: Strategy and tier (sequential, everything depends on it)
Use the `launch-strategist` agent. Give it the input path and the output folder. It writes:
- `outputs/<slug>/01-tier-decision.md`
- `outputs/<slug>/02-launch-brief.md`

Read both files when it finishes. Note the tier. Every downstream step follows the asset matrix in `context/tiering.md` for that tier.

## Step 2: Build the assets (in parallel)
Launch these agents at the same time, each with the input path, the brief path, the tier and the output folder:
- `copywriter` : channel copy for this tier, into `03-channel-copy.md`
- `enablement-lead` : sales materials for this tier, into `04-sales-enablement.md`
- `launch-ops` : the checklist, into `05-launch-checklist.csv` and `05-launch-checklist.md`

As soon as `copywriter` finishes, and without waiting for the other two, launch:
- `design-director` : design briefs for the visual assets the "Visual assets" rows in `context/tiering.md` list for this tier, into `07-design-briefs.md`. Give it the brief path, the tier decision path, `03-channel-copy.md` and the output folder. It needs the final copy, so it must never start before the copywriter is done.

## Step 3: Review gate
Wait until all four agents have finished. Use the `brand-reviewer` agent on everything in `outputs/<slug>/`, including `07-design-briefs.md`. It writes `06-review.md` with a pass or fail per asset and scores against its rubric.

If any asset fails:
1. Send that asset back to the agent that wrote it, with the reviewer's specific notes. One revision pass only. If the copywriter revises text that appears on an image, send `design-director` the changed lines in the same pass so the on-image text stays identical to the copy.
2. Run `brand-reviewer` again on the revised assets only and append the result to `06-review.md`.
3. Anything still failing goes in the run report under "Needs a human."

## Step 4: Learn
Ask `brand-reviewer` to add any issue that is likely to repeat to `learnings/lessons.md`, in the format that file specifies. No more than three new lessons per run.

## Step 5: Run report
Write `outputs/<slug>/00-run-report.md`:

```
# Launch CoPilot run report: <release name>

**Tier:** <tier> (weighted score <x.x>) <override, if any>
**Run time:** <minutes>
**Assets produced:** <count> | **Passed review first time:** <count> | **Revised:** <count> | **Needs a human:** <count>

## The launch in three lines
<what it is, who it's for, why now>

## Decisions the system made
- <tier and why>
- <assets deliberately not produced for this tier>
- <any positioning choice worth a human's eye>

## Needs a human
- <every [NEED PROOF: ...] across all assets, deduplicated, with the file it's in>
- <anything that failed review twice>

## Files
<list every file in the folder with one line on what it is>

## Lessons added this run
<the lines added to learnings/lessons.md, or "None">
```

Finish by printing the run report to the screen.
