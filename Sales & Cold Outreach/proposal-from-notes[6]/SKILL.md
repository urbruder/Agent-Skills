---
name: proposal-from-notes
description: >
  Use this skill whenever a user has just had a sales call, discovery call, or client meeting and wants to turn their notes into a proposal. Trigger on phrases like "just got off a call", "here are my call notes", "turn these notes into a proposal", "I have messy notes from a meeting", "client call recap", "discovery call notes", "help me write this up", "need a proposal from this", "post-call proposal", "I took some notes can you write the proposal", "summarize call into proposal". Also trigger when a user pastes anything that looks like unstructured call notes — bullet fragments, half-sentences, dollar amounts, names, action items — and implies they want a client-facing document. The notes can be rough, messy, or barely legible. This skill is optimized for speed: the user wants something send-ready before the momentum from the call dies. Do NOT use the winning-proposal skill for this — this skill is specifically about transforming raw call notes into a polished proposal, fast.
---

# Proposal from Notes

Drop messy call notes. Get a clean, send-ready proposal. Turn a 30-minute call into a proposal before your coffee's cold.

## Core Philosophy

The window between a great discovery call and a signed proposal is short. Every hour you spend writing is an hour the prospect is cooling off, comparing alternatives, or getting distracted. This skill is designed for speed without sacrificing quality.

The job is **translation**, not invention: take whatever the user captured during or after the call — fragments, bullets, prices scrawled mid-sentence, client quotes, half-formed ideas — and reconstruct it into a proposal the client will read and say "yes" to.

Key principles:
- **Extract signal from noise** — bad notes still contain the essentials if you know where to look
- **Fill gaps with intelligent assumptions** — flag them clearly so the user can verify before sending
- **Mirror the client's language back at them** — use words from the notes that the client said, not generic business language
- **Faster is better** — a good proposal sent in 20 minutes beats a perfect one sent tomorrow morning

---

## Step 1: Ingest the Notes

Accept anything:
- Bullet points, stream-of-consciousness, voice-to-text transcripts
- Messy shorthand ("wants site redone — hates current one, says boring. deadline = end of Q, budget prob 8-10k")
- Copied meeting summaries or CRM entries
- Just a few key facts ("budget $15k, wants email automation, current tool is Mailchimp, pain = manual work, deadline = before Black Friday")
- Combination of all of the above

**Do not ask the user to clean up their notes.** That's this skill's job.

**Do ask one question if truly critical info is missing** — only one, and only if the proposal cannot be written without it:
- If there's zero budget signal: "Any sense of their budget range, or should I write this without a price for now?"
- If the service being sold is completely unclear: "What are you selling them — [inferred guess]?"

Otherwise, proceed. Make assumptions. Flag them. Write fast.

---

## Step 2: Parse the Notes — Internal Extraction

Before writing a word of the proposal, silently parse the notes for these signals. Do not show this parsing to the user — use it to structure the output.

**Client signals to extract:**
- [ ] Client name / company name
- [ ] Decision-maker name and title (if mentioned)
- [ ] The problem they described (in their words if possible)
- [ ] What they've tried before that didn't work
- [ ] Their desired outcome / what success looks like
- [ ] Specific fears, frustrations, or risks mentioned
- [ ] Timeline / deadline
- [ ] Budget (stated, implied, or range)
- [ ] Competitors mentioned or being considered
- [ ] Anything they said they loved or hated
- [ ] Specific phrases or words the client repeated (use these in the proposal)

**Seller signals to extract:**
- [ ] What's being proposed / scope of work
- [ ] Any pricing discussed or floated
- [ ] Deliverables mentioned
- [ ] Anything promised or committed to on the call
- [ ] Proposed timeline or phases
- [ ] Any concerns the seller has about scope

**Missing signal inventory:**
Note what's absent. You'll fill gaps with reasonable assumptions and flag them.

---

## Step 3: Reconstruct the Proposal

Use the **Standard Proposal** structure below. Adapt length to project size:
- Under $5K or simple scope → Flash format (see Step 4)
- $5K–$50K → Standard (full structure below)
- $50K+ → Standard + recommend the user add a formal SOW appendix

### Standard Proposal Structure

---

#### OPENING: The Mirror (No header — this is the first thing they read)

1–3 sentences. Reflect back what the client said their problem was, in language close to theirs. Do not introduce yourself here. Do not say "thank you for your time." Do not say "following up on our conversation."

**Formula:**
> [Client/company] is dealing with [the real problem underneath the stated ask]. [The consequence of not fixing it]. This proposal outlines how [seller] will [specific outcome].

Pull the client's actual words when possible. If they said "our site looks like it was built in 2010," use that. If they said "we're losing deals to Acme because they look more credible," put that in.

---

#### WHAT WE HEARD

*Section header: "What We Heard" or omit header entirely for conversational proposals*

3–6 bullets. These should feel like a checklist of things the client said — proof you listened. Each bullet names a pain, goal, constraint, or fear from the call.

Format:
```
• You need [outcome] by [timeframe] — [reason they gave]
• Your current [situation] is causing [problem]
• You've tried [X] before; it [what happened]
• Your concern is [specific fear from the call]
• Success for you looks like [their definition]
• Budget: you're working with approximately [range]
```

Flag anything inferred vs. stated:
> *(Assumed — confirm before sending)*

---

#### THE APPROACH

*Section header: "How We'll Do This" or "The Approach"*

3–4 named phases. Each phase is a short paragraph (2–4 sentences) describing an outcome, not a task list. Name phases after what the client gets, not what you do.

If the call didn't include phase discussion, construct a logical sequence based on the scope discussed. This is fine — most clients don't think in phases during discovery; they appreciate seeing it organized.

**Phase naming by project type:**

| Project type | Phase names |
|---|---|
| Web/design | Discover → Design → Build → Launch |
| Strategy/consulting | Diagnosis → Direction → Execution → Measure |
| Marketing/content | Audit → Plan → Create → Optimize |
| Tech/dev | Scope → Build → Test → Deploy |
| Creative/branding | Research → Concept → Refine → Deliver |

---

#### WHAT YOU'LL RECEIVE

*Section header: "What You'll Receive" or "Deliverables"*

Bulleted list of specific deliverables. Be concrete. If the notes were vague ("do a website"), make reasonable assumptions about typical deliverables and flag them.

```
✓ [Specific deliverable]
✓ [Specific deliverable]
✓ [X] rounds of revisions included
✓ Delivery by [date from notes, or "target: [reasonable date]"]
```

Include a brief **Not Included** section if scope creep is likely:
```
Not included in this proposal:
× [Common assumption that would expand scope]
× [Adjacent work likely to be requested]
```

---

#### INVESTMENT

*Section header: "Investment"*

State price clearly. No hedging. If budget was discussed, anchor to it. If budget was unclear, write the price with a brief rationale.

**If budget was stated or strongly implied:**
> **[Project Name]: $[Amount]**
> 50% ($X) at signing · 50% ($X) at delivery

**If budget was a range:**
> Present two options named by outcome scope (not "Basic"/"Premium"):
> - **[Focused outcome]**: $[lower end]
> - **[Full outcome]**: $[upper end]

**If no budget signal at all:**
> Write `**[Project Name]: $[X]**` with a note to user: *(Placeholder — insert your price here before sending)*

Payment structure default: 50/50 split. Adjust if the notes suggest a different arrangement.

---

#### WHY US

*Section header: "Why [Seller Name/Company]" — or omit if proposal is very short*

If the user's notes mention past work, results, or client names: write 2–3 sentences of social proof.

If no proof points in the notes: write a placeholder:
> *(Add: one sentence about a relevant past project or result. A client name + outcome is ideal.)*

---

#### NEXT STEPS

*Section header: "Next Steps" or "Ready to Move Forward?"*

One clear action. Deadline if any timing was discussed. No multiple options — one path.

```
**Ready to move forward?**

Reply to this email and I'll send the agreement today. To lock in a [Month] start date, I'll
need a signed contract by [specific date — default: 5 business days from now].

Questions? Happy to jump on a quick call: [booking link or "just reply here"].

— [Sender name]
```

---

## Step 4: Flash Format (Fast / Small / Simple)

For projects under $5K, quick-turnaround freelance work, or when the user explicitly wants something short:

```
[Opening line: mirror their problem in one sentence]

Here's what I'd do: [2–3 sentences on approach]

You'd receive:
• [Deliverable 1]
• [Deliverable 2]
• [Deliverable 3]

Investment: $[Amount], split 50/50 at start and delivery.

To move forward, [one action]. I can start [date].

— [Name]
```

Target: under 200 words. Reads in 30 seconds.

---

## Step 5: Handling Specific Note Types

### Voice-to-text / transcripts
These are often stream-of-consciousness. Look for: dollar amounts, dates, proper nouns (client name, company, tools), and any sentence that starts with "they said" or "she mentioned." Those are gold. Ignore filler.

### Super sparse notes ("budget 10k, needs email automation, deadline Nov")
Write a full Flash Proposal. Fill in likely deliverables for that scope, flag them all as assumptions. Ask one question only if the service type is genuinely ambiguous.

### Notes with conflicts or ambiguity ("budget maybe 5k or could go higher", "wants it in 2 weeks but also said 'no rush'")
Use the more conservative interpretation and flag the conflict:
> *(Noted: budget range was unclear — adjust pricing before sending)*
> *(Noted: timeline was discussed as both 2 weeks and flexible — confirm with client)*

### Notes in another language
Write the proposal in the same language as the notes unless the user specifies otherwise.

### Notes that include red flags ("seems price-sensitive", "mentioned three other agencies", "not sure they have budget approved")
Don't ignore these. Add a brief note to the user at the end:
> **Heads up:** Your notes mention [X]. You may want to [suggested action] before sending.

---

## Output Format

Deliver three things, in this order:

**1. The proposal** — full copy, ready to paste into email or a doc. Clean formatting. No lorem ipsum or unexplained brackets.

**2. Flagged assumptions** — a short numbered list of things inferred from incomplete notes. Keep it tight: 3–6 items max.

Example:
```
Before sending, confirm:
1. Budget: I used $8,500 — adjust if this doesn't match what was discussed
2. Timeline: I assumed a 3-week delivery based on the Q3 deadline mentioned
3. Deliverables: I included a mobile version — confirm this is in scope
4. Social proof: I left a placeholder — add your best relevant case study here
```

**3. Subject line** — for the email that carries this proposal.

Good subject lines:
- `Proposal for [Client Company]: [Project Name]`
- `[Client Name] — here's how I'd approach [goal]`
- `[Your Name] × [Client]: [Project] Proposal`

---

## Quality Check (Run Before Outputting)

- [ ] Does the opening mirror the client's actual words, not generic problem language?
- [ ] Does "What We Heard" contain at least one thing that would make the client say "exactly"?
- [ ] Is pricing stated plainly, not buried or hedged?
- [ ] Is there exactly one next-step action?
- [ ] Are all gaps flagged — nothing silently wrong?
- [ ] Could this be sent as-is (minus flagged items) without embarrassment?
- [ ] Is the whole thing readable in under 3 minutes?

---

## Relationship to winning-proposal Skill

This skill is optimized for **speed and note translation**. If the user needs:
- A full formal SOW → suggest using the `winning-proposal` skill
- A live pitch deck → suggest using the `winning-proposal` skill's deck-pitch reference
- Pricing strategy advice → suggest using the `winning-proposal` skill's pricing-psychology reference

For everything else — call notes in, proposal out — this skill handles it.
