# Launch CoPilot

An agentic launch system for product marketing. A closed beta handoff goes in. A complete, tier-appropriate launch kit comes out, built on real positioning and messaging, and reviewed against the company's voice before anyone sees it. One agent, the Sales Enablement Lead, stays on after the launch to answer reps and prepare their calls.

## Ground rules for every run

1. **Context first.** Before writing anything, read everything in `context/` (the marketing brain) and `learnings/lessons.md`. Every claim, message and asset must trace back to those files or to the closed beta handoff. Never invent customer names, metrics, quotes, prices or dates.
2. **Missing proof gets flagged, not faked.** If an asset needs a proof point that isn't in `context/proof-points.md` or the closed beta handoff, write `[NEED PROOF: what is needed]` in its place. Closed beta stats and quotes are internal evidence, not approved proof: they shape the audience and positioning, and need approval before any customer-facing use.
3. **Each step builds on the last.** The chain runs in order: launch brief, product context, audience, positioning, messaging, campaign strategy. Copy, design, sales and ops assets build from messaging and campaign strategy. Nothing downstream may contradict what is upstream.
4. **Positioning before copy.** Positioning follows April Dunford's method (Obviously Awesome), in order, with no fill-in-the-blank statement. Messaging derives from positioning. Copy derives from messaging.
5. **Tier decides scope.** The `campaign-strategy-agent` scores the release with `context/tiering.md` and decides the tier. Downstream agents only produce what that tier calls for. Doing less, on purpose, is part of the job.
6. **Nothing ships unreviewed.** Every run ends with the `reviewer-agent`. Assets that fail get one revision pass and a re-review. Anything still failing is listed in the run report as needing a human.
7. **The system learns.** After review, recurring issues are added to `learnings/lessons.md`. Questions reps ask that nobody could answer go to `learnings/field-feedback.md`, which the Sales Enablement Lead reads on every run.
8. **Write like a person.** Plain words, short sentences, no em dashes, no hype words listed in `context/voice.md`.

## How to run

```
/launch inputs/<file>.md
```

Outputs land in `outputs/<launch-slug>/`. The run report (`00-run-report.md`) is the first file to read.

After a launch, reps can use the Sales Enablement Lead at any time:

```
/ask-enablement "How do I handle the objection that Atlassian already has native backup?"
/call-prep "Mid-size fintech, Jira Cloud, rolling out AI agents, IT Director on the call"
```

## Map of the system

- `context/` : the marketing brain and source of truth. Company, personas, voice, brand, tiering rubric (the GTM playbook), proof points.
- `.claude/commands/launch.md` : the orchestrator. Sequences the agents and owns the run report.
- `.claude/commands/ask-enablement.md`, `.claude/commands/call-prep.md` : on-demand modes of the Sales Enablement Lead.
- `.claude/agents/` : eleven specialist agents, each with one job.
- `.claude/skills/` : the method and output template each agent follows.
- `learnings/lessons.md` : what past runs taught the system.
- `learnings/field-feedback.md` : what reps asked and said.

## Agents and outputs

| Step | Agent | Output |
|---|---|---|
| 1 | `launch-brief-agent` | `01-launch-brief.md` |
| 2 | `product-context-agent` | `02-launch-context.md` |
| 3 | `audience-agent` | `03-audience.md` |
| 4 | `positioning-agent` | `04-positioning.md` |
| 5 | `messaging-agent` | `05-messaging.md` |
| 6 | `campaign-strategy-agent` | `06-campaign-strategy.md` |
| 7 | `copywriter-agent` | `07-channel-copy.md` |
| 7 | `design-director-agent` (after the copywriter) | `08-design-briefs.md`, `visuals/` (SVG and PNG) |
| 7 | `sales-enablement-agent` | `09-sales-enablement.md`, `09b-enablement-session.md`, `09c-readiness-quiz.md` |
| 8 | `launch-ops-agent` | `10-launch-checklist.csv`, `10-launch-checklist.md` |
| 9 | `reviewer-agent` | `11-review.md` |
| 10 | `/launch` | `00-run-report.md` |
