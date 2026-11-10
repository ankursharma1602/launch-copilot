# Launch CoPilot

An agentic launch system for product marketing. A closed beta handoff goes in. A complete, tier-appropriate launch kit comes out, built on real positioning and messaging, and reviewed against the company's voice before anyone sees it. One agent, the Sales Enablement Lead, stays on after the launch to answer reps and prepare their calls.

## Ground rules for every run

1. **Context first.** Before writing anything, read everything in `context/` (the marketing brain) and `learnings/lessons.md`. Every claim, message and asset must trace back to those files or to the closed beta handoff. Never invent customer names, metrics, quotes, prices or dates.
2. **Facts about the company are proven or flagged. Planning inputs are filled in.** Claims about the company and product (capabilities, customer results, metrics, competitors, quotes) must come from `context/proof-points.md` or the handoff, or be flagged `[NEED PROOF: what is needed]`. Planning inputs are different: personas, targets, dates, budgets and owners are what a PMM decides or assumes. Fill them with specific, realistic values and label them "illustrative" when the handoff doesn't give them. Never leave a planning cell blank or as [NEED PROOF]. Closed beta stats and quotes are internal evidence: they shape the audience and positioning, and need approval before any customer-facing use.

   **Where flags live.** Do not scatter `[NEED PROOF]` tags and caveats through the body. Each file ends with one short "Open questions" list. Customer-facing copy never contains a flag, a caveat for the team or a note to writers.
3. **Each step builds on the last.** The chain runs in order: launch brief, product context, tiering, audience, positioning, messaging, campaign strategy. Copy, design, sales and ops assets build from messaging and campaign strategy. Nothing downstream may contradict what is upstream.
4. **Positioning before copy.** Positioning follows April Dunford's method (Obviously Awesome), in order, with no fill-in-the-blank statement. Messaging derives from positioning. Copy derives from messaging.
5. **Tier decides scope.** The `tiering-agent` scores the release on the 4Cs in `context/tiering.md` and decides the tier. The `campaign-strategy-agent` plans for that tier and does not re-score it. Downstream agents only produce what that tier calls for. Doing less, on purpose, is part of the job.
6. **Nothing ships unreviewed.** Every run ends with the `reviewer-agent`. Assets that fail get one revision pass and a re-review. Anything still failing is listed in the run report as needing a human.
7. **The system learns.** After review, recurring issues are added to `learnings/lessons.md`. Questions reps ask that nobody could answer go to `learnings/field-feedback.md`, which the Sales Enablement Lead reads on every run.
8. **Write like a person.** Plain words, short sentences, no em dashes, no hype words listed in `context/voice.md`.
9. **Plan the launch, not the beta.** The handoff marks the end of beta. Every output plans the general availability launch: pre-launch, launch day and post-launch. Customer-facing assets announce the generally available product and its CTA, never "opt in to the beta". Use the GA date, plans and regions in the handoff.
10. **Short beats complete.** Each file opens with its showcase output, then only the detail a stakeholder needs. Cut anything a reader would skim past. If a section isn't needed for this tier, leave it out instead of explaining why.

## How to run

```
/launch inputs/<file>.md
```

Outputs land in `outputs/<launch-slug>/`. The run report (`00-run-report.md`) is the first file to read.

After a launch, reps can use the Sales Enablement Lead at any time:

```
/ask-enablement "How do I handle the objection that our practice management tool already tracks time?"
/call-prep "Mid-size personal injury firm, managing partner on the call, associates lose billable time"
```

## Map of the system

- `context/` : the marketing brain and source of truth. Company, personas, voice, brand, tiering rubric (the GTM playbook), proof points.
- `.claude/commands/launch.md` : the orchestrator. Sequences the agents and owns the run report.
- `.claude/commands/ask-enablement.md`, `.claude/commands/call-prep.md` : on-demand modes of the Sales Enablement Lead.
- `.claude/agents/` : twelve specialist agents, each with one job.
- `.claude/skills/` : the method and output template each agent follows.
- `learnings/lessons.md` : what past runs taught the system.
- `learnings/field-feedback.md` : what reps asked and said.

## Agents and outputs

| Step | Agent | Output |
|---|---|---|
| 1 | `launch-brief-agent` | `01-launch-brief.md` |
| 2 | `product-context-agent` | `02-launch-context.md` |
| 3 | `tiering-agent` | `03-tiering.md` |
| 4 | `audience-agent` | `04-audience.md`, `visuals/audience-personas.png` |
| 5 | `positioning-agent` | `05-positioning.md` |
| 6 | `messaging-agent` | `06-messaging.md` |
| 7 | `campaign-strategy-agent` | `07-campaign-strategy.md` |
| 8 | `copywriter-agent` | `08-channel-copy.md` |
| 8 | `design-director-agent` (after the copywriter) | `09-design-briefs.md`, `visuals/` (SVG and PNG) |
| 8 | `sales-enablement-agent` | `10-sales-enablement.md`, `10b-enablement-session.md`, `10c-readiness-quiz.md` |
| 9 | `launch-ops-agent` | `11-launch-checklist.csv`, `11-launch-checklist.md` |
| 10 | `reviewer-agent` | `12-review.md` |
| 11 | `/launch` | `00-run-report.md` |
