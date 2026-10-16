---
name: launch-checklist
description: Build a dated, owned launch checklist with dependencies and export it as CSV for monday.com or Jira. Use when turning a launch plan into tasks.
---

# Launch checklist

## Method
1. Build tasks in four phases: Prepare (L-21 to L-8), Enable (L-7 to L-1), Launch (L-day), Measure (L+1 to L+90).
2. Only include tasks for the assets in `06-campaign-strategy.md` and the files that exist in the output folder.
3. Every task has: a role owner, a due date or L-offset, a dependency (or "none"), and a definition of done.
4. Always include:
   - Final review
   - The enablement session (from `09b-enablement-session.md`) at about L-5 and the readiness quiz (`09c-readiness-quiz.md`) by L-3, when the tier produces them
   - Go/no-go check at L-2
   - Measurement checkpoints at L+30, L+60 and L+90 tied to the success metrics in `06-campaign-strategy.md`
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
- This imports into monday.com (Import from Excel/CSV) and Jira (CSV importer).

## Readable version
Group by phase. One line per task: `- [ ] <Due> | <Owner> | <Task>`
End with a table that maps each open question to the task that resolves it.
