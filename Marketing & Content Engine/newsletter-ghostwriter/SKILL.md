---
name: newsletter-ghostwriter
description: create high-quality business newsletters from rough ideas, notes, articles, links, transcripts, voice samples, offers, announcements, lessons, or personal stories. use when the user wants a newsletter people open and read, written in their voice, with subject lines, preview text, structure, narrative flow, practical takeaways, and a clear call to action. prioritize business relevance, audience value, credibility, retention, and voice fidelity over generic email copy or hype.
---

# Newsletter Ghostwriter

Turn a rough idea into a polished newsletter draft that sounds like the sender and gives the audience a reason to keep reading.

## Core workflow

When the user provides a topic, rough idea, notes, source material, voice sample, product update, announcement, article, or transcript:

1. Identify the newsletter job.
   - audience
   - sender role or brand
   - desired reader takeaway
   - desired action, if any
   - context or source material
   - newsletter type: story, insight, teardown, list, lesson, announcement, curated roundup, founder note, case study, opinion, how-to, or promotional email

2. Capture the voice.
   - If voice samples are provided, mirror sentence length, level of warmth, humor, directness, vocabulary, and pacing.
   - If no voice sample is provided, default to clear, conversational, credible, and business-useful.
   - Preserve the sender's point of view rather than writing like a generic brand account.

3. Choose the strongest structure.
   - Use `references/newsletter-frameworks.md` when structure, subject lines, or quality checks are needed.
   - Select the format that best fits the user's goal rather than forcing every newsletter into the same template.

4. Write the newsletter.
   - Open with a specific hook, tension, observation, story, or promise.
   - Build the body around one clear idea.
   - Use skimmable sections, short paragraphs, and natural transitions.
   - Include concrete examples, stakes, lessons, or implications.
   - End with a useful close and a clear CTA when appropriate.

5. Provide subject line options.
   - Include 5 to 10 subject lines by default.
   - Include 2 to 3 preview text options.
   - Prioritize curiosity plus clarity, not clickbait.

6. Quality check the draft.
   - Remove generic filler.
   - Replace vague claims with concrete value.
   - Avoid sounding overproduced or obviously AI-written.
   - Keep one main idea visible throughout.
   - Ensure the CTA matches the intent and does not feel bolted on.

## Default output format

Use this format unless the user asks for another format:

```markdown
## Newsletter Strategy
- Audience: [audience]
- Core idea: [one-sentence idea]
- Reader takeaway: [what the reader should understand or do]
- Angle: [story, insight, teardown, list, lesson, announcement, etc.]

## Subject Lines
1. [subject line]
2. [subject line]
3. [subject line]
4. [subject line]
5. [subject line]

## Preview Text Options
1. [preview text]
2. [preview text]
3. [preview text]

## Newsletter Draft
[newsletter body]

## Optional CTA Variations
1. Soft CTA: [cta]
2. Direct CTA: [cta]
3. Conversation CTA: [cta]
```

## Writing standards

Prioritize:

- a strong first line
- one clear idea
- useful business insight
- a human voice
- specific examples
- believable claims
- natural rhythm
- low-friction reading
- clear next step

Avoid:

- generic greetings like "hope you're doing well" unless requested
- bloated intros
- fake urgency
- empty thought leadership
- excessive emojis
- over-formatting
- clickbait subject lines
- motivational fluff with no substance
- sounding like a corporate press release unless the user requests that style

## Voice matching rules

When given a voice sample:

- Identify the 5 most important voice traits before drafting.
- Reuse cadence and tone, not exact phrases unless the user asks.
- Keep opinions, vocabulary, and level of polish consistent with the sample.
- If the sample is casual, keep the draft casual but still business-appropriate.
- If the sample is executive, keep the draft concise, confident, and strategic.

## Input handling

If the user gives very little context, make reasonable business assumptions and produce a useful draft anyway. Do not block on clarification unless the newsletter would be materially wrong without it.

If useful, ask at most one clarifying question, but only when the missing information is critical, such as audience, offer, or required tone.

## Variations

When requested, provide:

- shorter version
- more personal version
- more founder-led version
- more executive version
- more educational version
- more promotional version
- stronger subject lines
- more story-driven version
- LinkedIn adaptation
- plain-text email version
- section-by-section outline only

## Reference

Use `references/newsletter-frameworks.md` for newsletter structures, subject line patterns, CTA patterns, voice diagnostics, and final quality checks.
