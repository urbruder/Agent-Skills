---
name: brand-voice-cloner
description: analyze writing samples to create a reusable brand voice profile, then rewrite or draft business content in that voice across emails, newsletters, social posts, landing pages, ads, scripts, sales copy, executive posts, and thought leadership. use when the user wants content to sound like a person, founder, executive, company, creator, or established brand based on pasted samples. prioritize authentic voice capture, repeatable voice rules, business clarity, tone consistency, and ethical imitation with user-provided samples.
---

# Brand Voice Cloner

Capture a brand or personal voice from writing samples, then apply it consistently to new business content.

## Core workflow

When the user provides writing samples, content examples, transcripts, posts, emails, landing pages, or newsletters:

1. Analyze the samples for:
   - tone
   - sentence rhythm
   - vocabulary
   - level of formality
   - humor or seriousness
   - opinion strength
   - structure patterns
   - preferred hooks
   - CTA style
   - recurring phrases
   - taboo words or avoided styles
   - business positioning signals

2. Create a concise voice profile before writing if the user has not already provided one.

3. Write or rewrite the requested content using that profile.

4. Preserve meaning and business intent. Do not copy sample text verbatim unless the user explicitly asks.

5. When samples conflict, infer the dominant voice and mention any uncertainty briefly.

6. Use `references/voice-profile-framework.md` for deeper analysis, voice cards, before-and-after rewrites, or ongoing voice system setup.

## Default output for voice analysis

Use this when the user asks to clone, capture, lock, or define a voice:

```markdown
## Brand Voice Profile

### Voice Summary
[2-4 sentence description of the voice]

### Tone
- [Trait]
- [Trait]
- [Trait]

### Sentence Rhythm
[Short notes on sentence length, pacing, punctuation, and cadence]

### Vocabulary
**Use often:**
- [word/style]
- [word/style]

**Avoid:**
- [word/style]
- [word/style]

### Structure Patterns
- [Pattern]
- [Pattern]

### Signature Moves
- [Distinctive writing habit]
- [Distinctive writing habit]

### CTA Style
[How this voice asks people to act]

### Voice Rules
1. [Rule]
2. [Rule]
3. [Rule]
4. [Rule]
5. [Rule]
```

## Default output for writing in the voice

When the user asks for new content in the voice, use this format:

```markdown
## Voice Applied

[Finished content]

## Notes
- Voice matched through: [specific traits]
- Assumptions: [only if needed]
```

Omit notes if the user asks for only final copy.

## Content types supported

Apply the voice to:

- social posts
- newsletters
- emails
- landing pages
- ad copy
- short-form video scripts
- founder posts
- executive thought leadership
- sales pages
- website copy
- product announcements
- event promotions
- internal memos
- pitch copy
- personal brand content

## Voice matching rules

Do:

- preserve the user's intended message
- match cadence, level of directness, and emotional range
- keep content useful and business-relevant
- use the audience and platform to adjust format without losing voice
- make the final draft sound natural, not like a parody
- ask for or infer audience and format when missing

Do not:

- exaggerate quirks until the voice becomes a caricature
- invent beliefs, credentials, life events, client results, or personal stories
- imitate a living public figure unless the user is that person or provides authorized brand samples
- copy full phrases from the samples unless they are generic brand taglines provided for reuse
- preserve unclear writing when clarity would help the business goal

## Business priority

For business use, voice should never override:

1. clarity
2. credibility
3. offer accuracy
4. compliance-sensitive claims
5. audience relevance
6. conversion goal

If the original voice is unclear, rambling, or too insider-heavy, lightly improve readability while preserving recognizable style.

## Quick voice extraction

If the user provides only a small sample, create a provisional voice profile and label it:

```markdown
## Provisional Voice Profile
Based on the available sample, this voice appears to be...
```

Suggest the user provide 3-5 more samples for a stronger clone only after delivering the best possible result.

## Rewrite modes

Use these modes when requested:

### Light voice pass
Keep the original structure and message. Adjust phrasing, cadence, and tone.

### Strong voice pass
Rewrite more deeply to sound like the voice while preserving the goal.

### Clean business pass
Keep the voice but improve clarity, specificity, and conversion focus.

### Platform adaptation
Adjust structure for the platform while preserving the voice.

## Final quality check

Before responding, verify that:

- the content sounds natural
- the voice is recognizable but not exaggerated
- business claims remain accurate
- the CTA fits the voice
- the output is ready to publish or edit
