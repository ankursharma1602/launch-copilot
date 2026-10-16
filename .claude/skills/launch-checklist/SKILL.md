---
name: launch-checklist
description: Build a dated, owned launch checklist with dependencies and export it as CSV for monday.com or Jira. Use when turning a launch plan into tasks.
---

# Launch checklist

## Method
1. Build tasks in four phases: Prepare (L-21 to L-8), Enable (L-7 to L-1), Launch (L-day), Measure (L+1 to L+90).
2. Only include tasks for assets this tier gets.
3. Every task has: a role owner, a due date or L-offset, a dependency (or "none"), and a definition of done.
4. Always include: final brand review, Sales enablement session, go/no-go check at L-2, and measurement checkpoints at L+30, L+60 and L+90 tied to the brief's success metrics.
5. If the launch date is unknown, use L-offsets and add a first task: "Confirm GA date."

## CSV format
Columns, in this order, with a header row:
`Task,Phase,Owner,Due,Depends On,Definition of Done,Status`

- `Status` is always `Not started`.
- Quote any field that contains a comma.
- This imports directly into monday.com (Import from Excel/CSV) and Jira (CSV importer).

## Readable version
Group by phase. One line per task: `- [ ] <Due> | <Owner> | <Task>`
