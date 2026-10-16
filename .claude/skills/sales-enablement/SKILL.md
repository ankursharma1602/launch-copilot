---
name: sales-enablement
description: The Sales Enablement Lead playbook in three modes. Launch kit (one-pager, talk track, discovery questions, objections, FAQ, competitive take, a 30-minute rep session and a readiness quiz). On-demand Q&A for reps. Call prep for a specific call. Use when preparing Sales for a release or answering a rep.
---

# Sales enablement

Reps read this in the two minutes before a call. Write for that. The same lead runs three modes. All three use the same sources and the same honesty rules.

## Sources, in order of trust
1. `context/` (company, personas, proof points, voice)
2. The latest `04-positioning.md` and `05-messaging.md`
3. `02-launch-context.md` (what ships, limitations, availability)
4. The enablement files already written (`09`, `09b`, `09c`)
5. `learnings/field-feedback.md`: tells you what reps ask and where they struggle. It is not proof. A rep's claim is never a source for a customer-facing fact.

If an answer is not supported by these, say so. Never invent customer names, metrics, quotes, prices, dates or competitor weaknesses.

## Mode 1: Launch kit

### Method
1. Check the asset matrix for the tier. Tier 3 gets only a short Sales FYI (5 lines: what it is, who cares, one line to say, the limits, where to learn more). No session and no quiz.
2. Read `learnings/field-feedback.md` first. For every open entry that fits this release or earlier ones, decide: add an objection, add an FAQ, sharpen a talk track line, or leave it open because the sources cannot support an answer. Mark the entry as addressed, with the file and section, or leave it open and list it under "Needs a human".
3. Discovery questions come before the pitch. A rep should find the pain before naming the feature.
4. Objections come from the persona fears in `context/personas.md`, the known limitations, and any matching field feedback.
5. The FAQ includes every known limitation, stated plainly.
6. The one-pager has a "Limits to state up front" line with the most important limitations.
7. Competitive lines only from `04-positioning.md`, `context/company.md` or the closed beta handoff.
8. Write `09-sales-enablement.md`, `09b-enablement-session.md` and `09c-readiness-quiz.md`.

### 09 Output template

```
# Sales enablement: <release name> (Tier <x>)

## One-pager
**Headline:** <customer outcome>
**The problem:** <2 lines>
**What it does:** <3 bullets>
**Why Rewind:** <2 bullets, proof-backed>
**Who to call about it:** <segment or trigger from 03-audience.md>
**Limits to state up front:** <the key limitations>
**Do not say:** <claims to avoid, such as "first" or "only">

## Talk track (under 150 words)
<what a rep actually says, in plain spoken sentences>

## Discovery questions
1. ...
2. ...
3. ...
4. ...

## Objection handling
| They say | You say | Proof |
|---|---|---|

## FAQ
**Q:** ...
**A:** ...
(include every known limitation)

## Competitive quick take
| Alternative | Where they stop | Where we go further |
|---|---|---|

## Field feedback applied
| Entry | What changed | Where |
|---|---|---|
```

### 09b Output template: 30-minute rep session

```
# Enablement session: <release name>

**Length:** 30 minutes | **Audience:** <reps and SEs> | **Prep for reps:** <what to read first>

## Agenda
| Time | Block | What happens | Who leads |
|---|---|---|---|
(Blocks add up to exactly 30 minutes.)

## Talking points
- <5 to 7 points the trainer says, in plain words, each traced to the messaging>

## Role-play 1: <persona 1, from context/personas.md>
- **Setup:** ...
- **The rep's goal:** ...
- **The buyer says:** <three lines to use>
- **What good looks like:** ...
- **Common mistake:** ...

## Role-play 2: <persona 2>
(same fields)

## Role-play 3: <persona 3>
(same fields)

## Wrap-up
- <what reps do next, and the readiness quiz>
```

### 09c Output template: readiness quiz

```
# Readiness quiz: <release name>

8 questions. Pass mark: 7 of 8. Covers positioning, the top objections, and the limitations.

1. <question> (positioning)
2. ...
(3 on positioning, 3 on objections, 2 on limitations, 8 in total)

## Answer key
1. <answer> | Source: <file and section>
2. ...
```

## Mode 2: On-demand Q&A (`/ask-enablement`)

### Method
1. Find the latest run: the most recently changed folder in `outputs/`. Say which launch you used.
2. Search the sources above for support. Quote the file and section.
3. If supported, answer like an enablement lead would on a quick call: short, in spoken language, with a line the rep can say. Keep it under about 120 words unless the question needs more. Add a one-line "proof to use" and any limitation they must not skip.
4. If only partly supported, answer the supported part and say what is missing.
5. If not supported, say so plainly, tell the rep what to say in the meantime (for example, "I'll find out and come back to you"), and log the question.
6. Log in `learnings/field-feedback.md` every question you could not fully answer. Remove customer and person names from the entry.

### Answer template

```
**Short answer:** <one or two spoken sentences>
**Say this:** "<talk track line>"
**Proof to use:** <approved proof or "none approved yet">
**Don't skip:** <limitation, if one applies>
**Source:** <file and section>
```

For an unsupported question:

```
**I can't back that up yet.** <what is missing>
**Say this for now:** "<honest holding line>"
**Logged for the team:** yes
```

## Mode 3: Call prep (`/call-prep`)

### Method
1. Read the call description. Pick the persona from `03-audience.md` and `context/personas.md` that fits the person on the call. Never invent facts about the prospect. Use only what the rep said.
2. Find the right message angle in `05-messaging.md` for that persona.
3. Return the one-page brief below. It must fit on one page.
4. Anything the sources cannot support is marked `[NEED PROOF: ...]`. Do not log call details or customer names.

### Call brief template

```
# Call prep: <the rep's one-line description>

**Persona on the call:** ...
**Launch used:** <release and run>

## Likely pains
- <3 bullets, in the persona's words>

## Discovery questions
1. ... (4 questions, in the order to ask them)

## Message angle
<the lead message and which pillar, in two or three sentences>

## Say this
"<a 3 to 4 sentence spoken opener>"

## Likely objections
| They say | You say |
|---|---|
(top 3)

## Proof to use
- <approved proof, or "none approved yet">

## Limits to state
- ...

## Don't say
- ...
```

## Field feedback format
Entries in `learnings/field-feedback.md` are one line each:
`- YYYY-MM-DD | <unanswered question | rep feedback> | <launch slug or "general"> | <text, no customer or person names> | <open | addressed: file, section>`
