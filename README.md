# Product Launch CoPilot

A GTM launch team in a repo. Twelve agents take a closed beta handoff to a full, reviewed launch: brief, tiering, audience, positioning, messaging, a tiered campaign plan, copy, visuals, sales enablement and a launch checklist.

**Demo:** **a full launch for a mock Clio (https://www.clio.com/) release, Clio Timekeeping, starting with `outputs/clio-timekeeping/00-run-report.md`.**

---

## Setup (about 10 minutes)

1. Install Claude Code if you haven't: `npm install -g @anthropic-ai/claude-code`
2. Clone the repo and open it: `git clone https://github.com/ankursharma1602/launch-copilot.git && cd launch-copilot`
3. Run `claude`
4. Type: `/launch inputs/closed-beta-handoff-clio-timekeeping.md`
5. Approve file writes when asked. The kit lands in `outputs/clio-timekeeping/`. Start with `00-run-report.md`.

To try another launch, drop a new closed beta handoff into `inputs/` and run `/launch` on it.

---

## How it works

```
                    inputs/<handoff>.md
                           |
                  /launch (orchestrator)
                           |
       every agent reads context/ + learnings/lessons.md first
                           |
              [ Launch Brief agent ]          01-launch-brief
                           |
              [ Product Context agent ]        02-launch-context
                           |
              [ Tiering agent ]               03-tiering
              scores the 4Cs, decides tier
                           |
              [ Audience agent ]              04-audience
                           |
              [ Positioning agent ]           05-positioning
              (Obviously Awesome method)
                           |
              [ Messaging agent ]             06-messaging
                           |
              [ Campaign Strategy agent ]     07-campaign-strategy
              plans the campaign for the tier
                           |
         --------------------------------------------
         |                                          |
  [ Copywriter agent ]                [ Sales Enablement Lead agent ]
  08-channel-copy                     10 kit, 10b rep session,
         |                            10c readiness quiz
         | final copy                              |
         v                                         |
  [ Design Director agent ]                        |
  09-design-briefs                                 |
  visuals/ (SVG + PNG)                             |
         |                                         |
         --------------------------------------------
                           |
              [ Launch Ops agent ]            11-launch-checklist
                           |
              [ Reviewer agent ] --- fail? ---> one revision pass,
              scores every asset                then re-review
                           |
              lessons back to learnings/lessons.md
                           |
                   00-run-report.md
```

### The Sales Enablement Lead is always on

```
                [ Sales Enablement Lead agent ]

   Mode 1                   Mode 2                    Mode 3
   Launch kits              On-demand Q&A             Call prep
   /launch                  /ask-enablement "..."     /call-prep "..."
   10, 10b, 10c             short spoken answer       one-page call brief
        ^                          |                        |
        |                          |                        |
        |     unanswered questions and rep feedback         |
        +----------- learnings/field-feedback.md <---------+
        (read on every launch run; objections and FAQs updated)
```

- **Launch kits:** the one-pager, a talk track under 150 words, discovery questions, objections, FAQ with every limitation, a competitive quick take, a 30-minute rep training plan with three role-plays, and an 8-question readiness quiz.
- **On-demand Q&A:** `/ask-enablement "How do I handle the objection that our practice management tool already tracks time?"` gives a short answer in spoken language, grounded only in `context/`, the latest positioning and messaging, and the enablement files. If it can't back the answer up, it says so and logs the question.
- **Call prep:** `/call-prep "Mid-size personal injury firm, managing partner on the call, associates lose billable time"` returns one page: likely pains, discovery questions, the message angle, likely objections and the proof to use.

### The agents
| Step | Agent | What it does | Output |
|---|---|---|---|
| 1 | Launch Brief | Frames the launch: what, why it matters, goals, timeline, stakeholders, open questions. Opens with a "Launch at a glance" table | `01-launch-brief.md` |
| 2 | Product Context | Turns the closed beta handoff into launch-ready context, keeping what is built separate from what closed beta customers said | `02-launch-context.md` |
| 3 | Tiering | Scores the release on the 4Cs, decides the tier and owns any override. Shows a scorecard | `03-tiering.md` |
| 4 | Audience | Best-fit segments and personas, tested against who got the most value in closed beta. Shows an illustrative persona table and PNG | `04-audience.md`, `visuals/audience-personas.png` |
| 5 | Positioning | Positioning built in order: alternatives (starting with what beta customers compared it to), attributes, value and proof, best-fit customers, category, trends. Opens with an April Dunford canvas | `05-positioning.md` |
| 6 | Messaging | A messaging framework: value proposition, three pillars with proof, message matrix, what to avoid saying | `06-messaging.md` |
| 7 | Campaign Strategy | Takes the tier and plans the campaign for it. Shows a channel plan with a KPI per phase | `07-campaign-strategy.md` |
| 8 | Copywriter | Channel copy for the tier | `08-channel-copy.md` |
| 8 | Design Director | A design brief per visual, rendered as SVG and PNG | `09-design-briefs.md`, `visuals/` |
| 8 | Sales Enablement Lead | Battlecard, kit, rep session, readiness quiz | `10-sales-enablement.md`, `10b`, `10c` |
| 9 | Launch Ops | Owned, dated checklist as CSV for monday.com or a similar project tool, with a Mermaid Gantt | `11-launch-checklist.csv`, `.md` |
| 10 | Reviewer | Scores every asset and showcase output, one revision, re-review, lessons | `12-review.md` |

### The four layers
| Layer | Where | What it does |
|---|---|---|
| **Context** | `CLAUDE.md`, `context/` | The marketing brain: company, personas, voice, tiering rubric (the GTM playbook), approved proof. Every output is grounded in it. |
| **Skills** | `.claude/skills/` | One playbook per agent, with method and output template. Consistent quality on every run. |
| **Agents** | `.claude/agents/` | Twelve specialists with one job each, limited tools and rules. Each step builds on the one before. |
| **Workflow** | `.claude/commands/` | `/launch` sequences the agents, runs the build step in parallel, enforces the review gate and writes the run report. `/ask-enablement` and `/call-prep` put the Sales Enablement Lead in front of reps. |

### Design choices that matter
- **Positioning before copy.** Copy comes from messaging, and messaging comes from a positioning analysis built on evidence, so the words aren't invented at the end.
- **It decides, not just drafts.** The tiering agent scores the release on the 4Cs and sets the tier. A Tier 3 release deliberately gets less.
- **It can't make things up.** Claims must trace to approved proof points. Anything missing becomes a visible `[NEED PROOF: ...]`, collected in the run report for a human.
- **Nothing ships unreviewed.** A reviewer agent scores every asset, runs mechanical checks (banned words, length limits, CSV structure), looks at the rendered images, and sends failures back for one revision.
- **Visuals come from the final copy.** On-image text is copied from the approved channel copy, never rewritten. Brand colors are placeholders until real ones are supplied.
- **It learns twice.** Recurring review issues go to `learnings/lessons.md`. What reps ask goes to `learnings/field-feedback.md`, which shapes the next launch's objections and FAQs. Field feedback shows what reps need. It is never proof.
- **It hands off.** The checklist exports as CSV for direct import into monday.com or a similar project tool.

---

## Demo script (4 minutes)

1. **Show the input** (20 sec): open `inputs/closed-beta-handoff-clio-timekeeping.md`. "A closed beta handoff: epic, release notes, demo notes, beta stats and mock customer feedback."
2. **Run it** (30 sec, or show a finished run): `/launch inputs/closed-beta-handoff-clio-timekeeping.md`. Point out the strategy chain running in order, then copy and sales enablement in parallel.
3. **Open the positioning** (40 sec): `05-positioning.md`. Alternatives first, then attributes, value, customers, category, trends. No slogan.
4. **Open the run report** (40 sec): tier and why, what it chose not to produce, and the "Needs a human" list of proof gaps.
5. **Open the visuals** (30 sec): the PNGs in `visuals/`, with the exact text from the copy.
6. **Open the review** (30 sec): rubric scores, a fail it caught, and the fix.
7. **Be a rep** (50 sec): `/ask-enablement "How do I handle the objection that our practice management tool already tracks time?"`, then `/call-prep "Mid-size personal injury firm, managing partner on the call, associates lose billable time"`. Ask something it can't back up and show it land in `learnings/field-feedback.md`.

---

## What I'd build next
- **Automatic trigger on GitHub:** a GitHub Actions workflow that runs `/launch` when a new closed beta handoff is pushed into `inputs/` (or on demand from the Actions tab), then commits the kit back to the repo. It needs an `ANTHROPIC_API_KEY` repository secret.
- **Event trigger from the project tool:** fire on a release status change via webhook.
- **Win/loss feed:** pipe call transcripts into a synthesizer agent so the proof points and objections update themselves.
- **Performance loop:** at L+30, pull adoption data and have the Campaign Strategy agent compare results against the brief's success metrics, feeding back into the tiering rubric.
