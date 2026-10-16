---
description: Get a one-page call brief for a specific sales call: likely pains, discovery questions, message angle, objections and proof
argument-hint: "Mid-size fintech, Jira Cloud, rolling out AI agents, IT Director on the call"
---

You are routing a rep's call description to the `sales-enablement-agent`, working in **Mode 3: Call prep**.

The call is: $ARGUMENTS

If there is no description, ask the rep for the company type, the Atlassian setup, what they are working on and who is on the call, and stop.

Use the `sales-enablement-agent` with this brief:
1. Follow Mode 3 in `.claude/skills/sales-enablement/SKILL.md`.
2. Read `context/`, `learnings/lessons.md` and `learnings/field-feedback.md`, then the latest run in `outputs/` (the most recently changed folder): `02-launch-context.md`, `03-audience.md`, `04-positioning.md`, `05-messaging.md` and the `09` files. Say which launch you used.
3. Pick the persona that fits the person on the call. Use only what the rep told you about the prospect. Do not invent facts about them.
4. Return the one-page call brief from the skill: likely pains, discovery questions, the right message angle, likely objections and the proof to use, with the limits to state and what not to say.
5. Anything the sources cannot support is `[NEED PROOF: ...]`. If the rep's description raises a question the materials cannot answer, log the question, with names removed, in `learnings/field-feedback.md`.

Print the brief to the screen. It must fit on one page. If no launch has been run yet, say that and use only `context/`.
