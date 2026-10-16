---
description: Ask the Sales Enablement Lead a question at any time and get a short, spoken-language answer grounded in the launch materials
argument-hint: "How do I handle the objection that Atlassian already has native backup?"
---

You are routing a rep's question to the `sales-enablement-agent`, working in **Mode 2: On-demand Q&A**.

The question is: $ARGUMENTS

If there is no question, ask the rep what they want to know, and stop.

Use the `sales-enablement-agent` with this brief:
1. Follow Mode 2 in `.claude/skills/sales-enablement/SKILL.md`.
2. Read `context/`, `learnings/lessons.md` and `learnings/field-feedback.md`, then the latest run in `outputs/` (the most recently changed folder): `02-launch-context.md`, `04-positioning.md`, `05-messaging.md` and the `09` files. Say which launch you used.
3. Answer like an enablement lead: short, in spoken language, with a line the rep can say, the proof to use and any limitation they must not skip. Cite the file and section you used.
4. Ground the answer only in those sources. If it is not supported, say so, give an honest holding line, and add the question to `learnings/field-feedback.md` in the format the skill defines, with any customer or person names removed.
5. If the rep shares feedback instead of a question (for example, "reps keep asking about X"), log that as rep feedback in the same file.

Print the answer to the screen. If something was logged, end with one line saying so. If no launch has been run yet, say that and answer only from `context/`.
