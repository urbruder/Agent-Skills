---
name: cold-email-writer
description: >
  Use this skill whenever a user wants to write cold outreach emails, sales emails, or prospecting emails — especially in volume. Trigger on phrases like "cold email", "outreach email", "sales email", "prospecting email", "write emails to leads", "email campaign", "B2B outreach", "founder outreach", "SDR emails", "email sequence", "email template for leads", "personalized email at scale". Also trigger when someone describes their role (sales rep, founder, agency owner, B2B consultant) and mentions reaching out to prospects or leads — even if they don't say "cold email" explicitly. This skill helps write emails that feel individually hand-typed, not templated — covering single emails, batch templates with variable slots, and personalization frameworks.
---

# Cold Email Writer

Write cold emails that sound hand-typed for one specific person — fast enough to send 100 a day.

## Core Philosophy

The cardinal sin of cold email is sounding like a cold email. Every tactic that "everyone knows" (the curiosity subject line, the PAS framework opener, the "just 15 minutes" CTA) has been so overused it now signals: *this was written by a tool*. 

The goal is to write something the recipient believes was typed specifically for them, in the moment, by a real human who did their homework. That means:

- **Specific over generic**: "I saw you just launched a Series A" beats "I noticed you're growing fast"
- **Short over complete**: Under 100 words usually wins. If you can say it in 3 sentences, do.
- **Curious over salesy**: Don't explain your whole offer. Create just enough intrigue that they want to reply.
- **Peer-to-peer tone**: Write like you're emailing a peer, not pitching a prospect. No buzzwords, no fluff.
- **One ask only**: A confused prospect does nothing. One CTA, always.

---

## Workflow

### Step 1: Gather Context

Before writing, collect (ask if missing):

1. **Who is the sender?** (role, company, what they sell/do)
2. **Who is the recipient?** (job title, company, industry — and any specific signal/trigger if known)
3. **What's the offer/value prop?** (what problem does the sender solve?)
4. **What's the goal of the email?** (book a call, get a reply, warm intro, etc.)
5. **Personalization signal** (optional but powerful): recent news, job change, LinkedIn post, company milestone, mutual connection, tool they use, content they published

If the user wants **batch/template mode** (many leads at once), ask for:
- The lead list columns available (e.g., First Name, Company, Title, Industry, Recent News)
- 1–3 example rows from their list

If the user wants a **single email**, you can proceed once you have items 1–4.

---

### Step 2: Choose the Email Type

Pick (or suggest) the right format based on context:

| Type | When to Use |
|------|-------------|
| **Hyper-personalized single** | High-value target, known signal/trigger |
| **Template with variable slots** | Batch outreach, consistent persona/ICP |
| **Multi-touch sequence** | Longer sales cycles, warm nurture needed |
| **Re-engagement / bump** | Following up on no-reply |

---

### Step 3: Write the Email

#### Structure (default)

```
Subject: [See subject line guidance below]

[Opening hook — 1 sentence, specific to them]

[Value bridge — 1–2 sentences connecting their world to your offer]

[Social proof or credibility — 1 sentence, optional]

[Single CTA — 1 sentence]

[Signature]
```

Keep total body under 100 words when possible. 150 max.

#### Subject Lines

The subject line should feel like an internal company email, not marketing:
- Keep under 6 words
- No title case ("Quick question" not "Quick Question")
- No emojis, no exclamation marks
- Formats that work well:
  - Question: "your content strategy?"
  - Name drop: "re: [their company] + [relevant topic]"
  - Curiosity gap: "something I noticed"
  - Specific observation: "[company] + [tool/tactic they use]?"

#### Opening Hook Patterns (use sparingly, vary them)

- Trigger-based: "Saw you just [specific event] — congrats."
- Observation: "Noticed [company] is [doing X thing] — interesting move."
- Content reference: "Read your post on [topic] — the part about [specific thing] stuck with me."
- Mutual context: "We both know [person] / We both use [tool]."
- Pattern interrupt: Start mid-thought. "Quick one —"

#### Value Bridge (keep it brief)

Don't explain the whole product. One sentence that connects their pain/context to an outcome:
> "We help [persona] [achieve outcome] without [common frustration]."

Or even more minimal:
> "We do X for companies like [relevant company they'd recognize]."

#### CTAs that get replies

- "Worth a quick chat?" (open)
- "Would it make sense to connect?" (low pressure)
- "Open to a 15-min call [day] or [day]?" (specific)
- "Curious if this is on your radar?" (soft, great for cold)
- Avoid: "Let me know if you'd like to learn more." (passive, weak)

---

### Step 4: Template Mode (Batch Output)

When the user needs templates for scale, output:

1. **The template** with `{{variable}}` placeholders (e.g., `{{first_name}}`, `{{company}}`, `{{trigger_line}}`)
2. **A variable guide** explaining what each placeholder should contain and how to fill it
3. **2–3 filled examples** using realistic example data to show how it reads when populated
4. **A "manual personalization" tip** — the one thing a rep can quickly research per lead to make each send feel bespoke (e.g., LinkedIn headline, recent company news via Google)

Example template structure:
```
Subject: {{subject_line}}

Hey {{first_name}},

{{trigger_line}} — thought it was worth a quick note.

{{value_bridge}}

{{social_proof_line}}

{{cta}}

[Sender name]
```

---

### Step 5: Multi-Touch Sequence (if requested)

For sequences, write 3–5 emails:

| Email | Timing | Goal | Tone |
|-------|--------|------|------|
| #1 | Day 1 | Open conversation | Curious, peer-like |
| #2 | Day 3–4 | Add value / new angle | Helpful, not pushy |
| #3 | Day 7 | Gentle bump | Casual, brief |
| #4 | Day 14 | Different value prop | New frame or use case |
| #5 | Day 21 | Breakup email | Honest, human |

The breakup email is powerful. Example:
> "Hey [name] — I've reached out a few times and haven't heard back. Totally get it if the timing's off or this isn't relevant. I'll leave it here — but if anything changes, happy to pick it up. Best, [name]"

---

## Anti-Patterns to Avoid

- ❌ "I hope this email finds you well"
- ❌ "I wanted to reach out because..."
- ❌ "We're the leading/premier/best-in-class..."
- ❌ "I'd love to learn more about your challenges"
- ❌ "Feel free to book time on my calendar" (as the *only* CTA)
- ❌ Opening with "My name is X and I work at Y"
- ❌ Long paragraphs. One idea per paragraph, max 2 sentences.
- ❌ Sounding like you used AI to write it (ironic but important — no em-dashes as stylistic flourishes, no overly polished phrasing)

---

## Quality Checklist (run before finalizing)

Before presenting the email(s), check:
- [ ] Under 120 words?
- [ ] No generic opener?
- [ ] Subject line under 6 words, lowercase?
- [ ] One and only one CTA?
- [ ] At least one specific detail (not generic to any prospect)?
- [ ] Would a human actually send this as-is?
- [ ] Does it sound like it was written for *this* person, not a persona?

---

## Output Format

**Single email:** Present cleanly with subject line labeled, then body. Offer 1–2 alternative subject lines or opening variations if useful.

**Batch template:** Subject template → body template → variable guide → 2–3 filled examples → personalization tip.

**Sequence:** Number each email, show send timing, include brief rationale for each angle.

Always offer to adjust tone, length, CTA, or angle after the first draft.
