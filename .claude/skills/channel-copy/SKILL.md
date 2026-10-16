---
name: channel-copy
description: Write launch copy for email, in-app, release notes, blog outline and LinkedIn, sized to the launch tier and grounded in the launch brief. Use when turning a brief into customer-facing copy.
---

# Channel copy

## Method
1. Check the asset matrix in `context/tiering.md`. Produce only the assets this tier gets. List the skipped ones at the top so a reader knows it was deliberate.
2. Every asset leads with the primary persona's moment of failure or desired outcome, then the capability, then proof.
3. Reuse the brief's key messages. Adapt length and tone to the channel, not the meaning.
4. Check `learnings/lessons.md` and apply every relevant lesson.

## Channel specs
| Asset | Spec |
|---|---|
| Customer email | Subject under 50 characters, 2 subject options. Preview text under 90 characters. Body under 150 words. One CTA. |
| In-app message | Headline under 8 words. Body under 25 words. One button label under 4 words. |
| Release note | Title, 2-3 sentence summary, "What's new" bullets, "How to get started" steps, availability line. |
| Blog post outline | Working title (2 options), hook paragraph written in full, H2 outline with one line per section, CTA. |
| LinkedIn post | Under 120 words. First line works as a standalone hook. No hashtags beyond 2. No emojis. |

## Output template

```
# Channel copy: <release name> (Tier <x>)

**Produced for this tier:** <list>
**Deliberately skipped:** <list>

## Customer email
**Subject A:** ...
**Subject B:** ...
**Preview:** ...
<body>
**CTA:** ...

## In-app message
...

(one section per asset)
```
