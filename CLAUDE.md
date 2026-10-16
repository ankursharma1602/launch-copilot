# Launch CoPilot

An agentic launch system for product marketing. A release note or PRD goes in. A complete, tier-appropriate launch kit comes out, reviewed against the company's positioning and voice before anyone sees it.

## Ground rules for every run

1. **Context first.** Before writing anything, read everything in `context/` and `learnings/lessons.md`. Every claim, message and asset must trace back to those files or to the input. Never invent customer names, metrics, quotes, prices or dates.
2. **Missing proof gets flagged, not faked.** If an asset needs a proof point that isn't in `context/proof-points.md` or the input, write `[NEED PROOF: what is needed]` in its place.
3. **Tier decides scope.** The tier is decided first, by the `strategy-agent` using `context/tiering.md`. Downstream agents only produce what that tier calls for. Doing less, on purpose, is part of the job.
4. **Nothing ships unreviewed.** Every run ends with the `review-agent`. Assets that fail the review get one revision pass. Anything still failing is listed in the run report as needing a human.
5. **The system learns.** After review, recurring issues are added to `learnings/lessons.md` so the next run avoids them.
6. **Write like a person.** Plain words, short sentences, no em dashes, no hype words listed in `context/voice.md`.

## How to run

```
/launch inputs/<file>.md
```

Outputs land in `outputs/<launch-slug>/`. The run report (`00-run-report.md`) is the first file to read.

## Map of the system

- `context/` : the source of truth. Company, personas, voice, tiering rubric, proof points.
- `.claude/commands/launch.md` : the orchestrator. Sequences the agents and owns the run report.
- `.claude/agents/` : specialist agents, each with one job.
- `.claude/skills/` : the playbooks and templates the agents follow.
- `learnings/lessons.md` : what past runs taught the system.
- `.github/workflows/launch-copilot.yml` : optional trigger so a launch kit generates when a new input is pushed.
