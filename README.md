# Launch CoPilot

A multi-agent launch system for product marketing, built in Claude Code.

A PRD or release note goes in. Out comes a tier decision, a launch brief, channel copy, design briefs for the visuals, sales enablement and an importable launch checklist, each reviewed against positioning, proof and voice rules before a human sees it. The system records what it gets wrong so the next run is better.

Demo input: a hypothetical Rewind release, Agent Rollback for Jira. It is a mock-up for demonstration, not a real product.

---

## Setup (about 10 minutes)

1. Install Claude Code if you haven't: `npm install -g @anthropic-ai/claude-code`
2. Unzip this folder and open a terminal in it.
3. Run `claude`
4. Type: `/launch inputs/rewind-agent-rollback-jira.md`
5. Approve file writes when asked. The kit lands in `outputs/agent-rollback-jira/`. Start with `00-run-report.md`.

To try another launch, drop a new PRD into `inputs/` and run `/launch` on it.

---

## How it works

```
                   inputs/<prd>.md
                          |
                 /launch (orchestrator)
                          |
      reads context/ + learnings/lessons.md
                          |
               [ launch-strategist ]
          tier decision  +  launch brief
                          |
         ---------------------------------------
         |                  |                  |
   [ copywriter ]  [ enablement-lead ]   [ launch-ops ]      (run in parallel)
   channel copy     one-pager, talk       checklist CSV
   sized to tier    track, objections,    for monday.com
         |          FAQ                   or Jira
         | final copy        |                  |
         v                   |                  |
 [ design-director ]         |                  |
 design briefs for           |                  |
 Claude Design or Canva      |                  |
         |                   |                  |
         ---------------------------------------
                          |
                 [ brand-reviewer ]  ---- fail? ----> one revision pass
          scores every asset on a rubric
                          |
              writes lessons back to
             learnings/lessons.md
                          |
                  00-run-report.md
```

### The four layers
| Layer | Where | What it does |
|---|---|---|
| **Context** | `CLAUDE.md`, `context/` | Single source of truth: company, personas, voice, tiering rubric, approved proof. Every output is grounded in it. |
| **Skills** | `.claude/skills/` | One playbook per PMM job, with method, specs and templates. Consistent quality on every run. |
| **Agents** | `.claude/agents/` | Specialists with one job each, limited tools, and rules. The strategist decides the tier, and that decision shapes everything downstream. |
| **Workflow** | `.claude/commands/launch.md` | The orchestrator sequences agents, runs three in parallel (the design-director starts once the copywriter is done), enforces the review gate and writes the run report. |

### Design choices that matter
- **It decides, not just drafts.** Tiering comes first, and a Tier 3 release deliberately gets less. Saying no to work is part of the system.
- **It can't make things up.** Claims must trace to approved proof points. Anything missing becomes a visible `[NEED PROOF: ...]`, collected in the run report for a human.
- **Nothing ships unreviewed.** A reviewer agent scores every asset on a five-part rubric, runs mechanical checks (banned words, length limits), and sends failures back for one revision.
- **It learns.** Recurring review issues are written to `learnings/lessons.md`, which every future run reads first.
- **Visuals come from the final copy.** The design-director writes paste-ready prompts for Claude Design or Canva. On-image text is copied from the approved channel copy, never rewritten, so the picture and the message can't drift apart.
- **It hands off.** The checklist exports as CSV for direct import into monday.com or Jira.

---

## Demo script (3 minutes)

1. **Show the input** (20 sec): open `inputs/rewind-agent-rollback-jira.md`. "A PRD, nothing more."
2. **Run it** (30 sec, or show a finished run): `/launch inputs/rewind-agent-rollback-jira.md`. Point out the strategist running first, then three agents in parallel.
3. **Open the run report** (45 sec): tier and why, what it chose not to produce, and the "Needs a human" list of proof gaps.
4. **Open the review** (45 sec): rubric scores, a fail it caught, and the fix.
5. **Show the learning loop** (20 sec): the new line in `learnings/lessons.md`.
6. **Show the hand-off** (20 sec): the checklist CSV, ready for monday.com or Jira.

---

## What I'd build next
- **Automatic trigger on GitHub:** a GitHub Actions workflow that runs `/launch` when a new PRD is pushed into `inputs/` (or on demand from the Actions tab), then commits the kit back to the repo. It needs an `ANTHROPIC_API_KEY` repository secret.
- **Event trigger from Jira:** fire on a Jira release status change via webhook.
- **Win/loss feed:** pipe call transcripts into a synthesizer agent so the proof points and objections update themselves.
- **Performance loop:** at L+30, pull adoption data and have the strategist compare results against the brief's success metrics, feeding back into the tiering rubric.
