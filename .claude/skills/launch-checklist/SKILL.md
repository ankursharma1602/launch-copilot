---
name: launch-checklist
description: Build a dated, owned launch checklist with dependencies and export it as CSV for a project tool such as monday.com. Use when turning a launch plan into tasks.
---

# Launch checklist

## Method
1. Build tasks in four phases: Prepare (L-21 to L-8), Enable (L-7 to L-1), Launch (L-day), Measure (L+1 to L+90).
2. Only include tasks for the assets in `07-campaign-strategy.md` and the files that exist in the output folder.
3. Every task has: a role owner, a due date or L-offset, a dependency (or "none"), and a definition of done.
4. Always include:
   - Final review
   - The enablement session (from `10b-enablement-session.md`) at about L-5 and the readiness quiz (`10c-readiness-quiz.md`) by L-3, when the tier produces them
   - Go/no-go check at L-2
   - Measurement checkpoints at L+30, L+60 and L+90 tied to the success metrics in `07-campaign-strategy.md`
   - A field-feedback review (`learnings/field-feedback.md`) at about L+14 and L+30, so the Sales Enablement Lead agent can update objections and FAQs
   - A lessons review after the launch
5. Every `[NEED PROOF: ...]` and open question in the earlier outputs becomes a task with an owner and a dependency.
6. If the launch date is unknown, use L-offsets and make the first task "Confirm GA date."

## CSV format
Columns, in this order, with a header row:
`Task,Phase,Owner,Due,Depends On,Definition of Done,Status`

- `Status` is always `Not started`.
- Quote any field that contains a comma or a double quote. Double any quote inside a quoted field.
- Keep Task names short. Put detail in Definition of Done.
- Every "Depends On" entry must match a Task name exactly. Separate several with `; `.
- Every row has exactly 7 columns.
- This imports into monday.com (Import from Excel/CSV) and most other project tools with a CSV importer.

## Showcase output: Mermaid Gantt
Open `11-launch-checklist.md` with a Mermaid `gantt` block, with owners and milestones by week, so it renders on GitHub. Rules:
- One section per phase. Each bar names the owner role and the L-offset, for example `Legal: wording review (L-14)`.
- Mark milestones (go/no-go, kit ready, launch day) with `milestone`.
- If there is no real launch date, set an arbitrary anchor day for L, hide it behind L-offsets in the bar names, and add a note under the chart: "Illustrative calendar. L is not a date." Never present a real-looking date as fact.
- Take every offset from `07-campaign-strategy.md` word for word.
- Keep the syntax simple (`dateFormat YYYY-MM-DD`, `section`, task lines) so GitHub renders it.

## Readable version
Group by phase. One line per task: `- [ ] <Due> | <Owner> | <Task>`
End with a table that maps each open question to the task that resolves it.
