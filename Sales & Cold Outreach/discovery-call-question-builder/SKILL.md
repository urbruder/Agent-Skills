---
name: discovery-call-question-builder
description: >
  Use this skill whenever a user is preparing for a sales discovery call, intro call, or prospect meeting and wants a tailored question list. Trigger on: "discovery call questions", "what to ask on a sales call", "prep for a prospect call", "call prep", "question list for my call", "preparing for discovery", "sales call prep", "what should I ask", "I have a call with [prospect]", "discovery questions for [industry/role]", "how to run a discovery call", "tailored questions before my call", "SPIN questions", "MEDDIC questions", "qualification questions", "call with a [title] at [company]", "need questions for my demo". Also trigger when a user shares prospect context — company name, role, industry, deal size — and implies they have a call coming up, even without saying "discovery". If someone is preparing to talk to a prospect and wants to know what to ask, this is the skill. Output is a structured, ready-to-use question list personalized to their specific prospect.
---

# Discovery Call Question Builder

Walk into every sales call knowing exactly what to ask — a tailored question list built from your prospect's context before you dial.

## Core Philosophy

Most salespeople ask the same 5 questions on every discovery call. The best salespeople do 20 minutes of research and walk in with questions that make prospects say "that's a really good question" — which is code for "you actually understand my world."

Discovery is not interrogation. It's a structured conversation that accomplishes four things simultaneously:
1. **Qualifies** the opportunity (is this worth pursuing?)
2. **Diagnoses** the real problem (not the stated one — the one underneath)
3. **Builds trust** (great questions prove you did your homework)
4. **Surfaces the buying criteria** (what does "yes" actually look like?)

The question list this skill builds is:
- **Prioritized** — the 5 questions you must ask are not the same as the 15 you could ask
- **Sequenced** — questions that build on each other, not a random inventory
- **Tailored** — specific to the prospect's company, role, industry, and deal context
- **Balanced** — situation, problem, implication, and value questions in the right ratio

---

## Step 1: Gather Prospect Context

The more context provided, the more tailored the output. Ask for what's missing — but only once, consolidated.

**Collect (from the user or by inference):**

| Signal | Why it matters |
|---|---|
| Prospect's job title | Shapes language, priorities, and what they care about vs. what their boss cares about |
| Company name | Enables research hooks and company-specific questions |
| Company size / stage | SMB vs. enterprise changes the buying process and objections |
| Industry | Industry-specific pain points, regulations, competitors |
| What you're selling | Defines which problems are relevant to diagnose |
| Deal stage | First call vs. further along changes the depth and tone of questions |
| What you already know | Avoids re-asking things already covered in email threads or LinkedIn |
| Inbound vs. outbound | Inbound = they already see a need; outbound = you may be creating awareness |

**If the user gives minimal context** ("I have a call with the VP of Ops at a logistics company"), proceed — good enough to build a solid list. Note what's inferred.

**If zero context:** Ask one question: "Tell me who you're calling and what you're selling — even a sentence or two is enough."

---

## Step 2: Research the Prospect (Internal Simulation)

Before building questions, simulate what a good rep would research in 20 minutes. Use whatever context is provided to infer:

- **Company context:** Stage, growth trajectory, recent news (funding, launches, expansions, layoffs), business model
- **Role context:** What a [title] at a [size] [industry] company typically owns, worries about, and is measured on
- **Industry context:** Common pain points, regulatory pressures, competitive dynamics, seasonal patterns
- **Deal context:** Why they might be talking to you — what trigger likely prompted this (inbound = known pain, outbound = implied pain)

Use this simulation to generate **company-specific and role-specific questions** rather than generic ones.

If web search is available, search for the company and prospect before building the list.

---

## Step 3: Build the Question List

Structure the output in five layers. Each layer has a different purpose.

---

### LAYER 1: OPENING QUESTIONS (2–3 questions)
**Purpose:** Set the tone. Get them talking. Establish that this is a conversation, not a pitch.

These questions are warm, open-ended, and ego-safe — they let the prospect feel like the expert.

**Principles:**
- Start with context, not pain — jumping straight to "what's broken" feels like an interrogation
- Reference something specific about them — shows you did homework
- Should generate 2–5 minutes of unprompted talking if they engage

**Templates to customize:**
- "Before we dive in — [specific thing about company/recent news]. What was the thinking behind that?"
- "I read a bit about [company] before this call — can you give me your version of what you're building/solving for right now?"
- "How did this call come about from your end — what made you [agree to take it / reach out]?"

---

### LAYER 2: SITUATION QUESTIONS (3–4 questions)
**Purpose:** Map the current state. Understand what they're working with today.

These are factual — they establish the landscape before diagnosing problems. Don't skip them even if you think you know the answers; hearing them say it matters.

**Principles:**
- One question per topic — don't bundle
- Aim to understand: current tools/processes, team structure, volume/scale, decision process
- Avoid questions Google can answer (looks lazy)

**Templates to customize:**
- "Walk me through how you currently [handle the thing your product addresses] — what does that look like day to day?"
- "How big is the team responsible for [relevant function]?"
- "What tools are you using today for [relevant area]?"
- "How long have you been running it this way?"

---

### LAYER 3: PROBLEM QUESTIONS (4–5 questions) ← The Core
**Purpose:** Surface the pain. Get them to articulate the problem in their own words.

These are the most important questions on the call. The prospect's own words about their pain become the language of the proposal. A problem they articulate themselves is a problem they own — and are more motivated to solve.

**Principles:**
- Ask about friction, not failure — "what slows you down" is easier to answer than "what's broken"
- Dig one level deeper than the first answer — "what's the impact of that?"
- Look for the problem-behind-the-problem — stated problem is often a symptom

**Templates to customize:**
- "What's the biggest friction point in [process/workflow] right now?"
- "Where does [process] break down most often — or where does it require the most manual effort?"
- "What are you having to work around that you wish just worked?"
- "If you could change one thing about how you [handle X] today, what would it be?"
- "What does [the problem] cost you — in time, in money, in headcount?"

---

### LAYER 4: IMPLICATION QUESTIONS (2–3 questions)
**Purpose:** Expand the pain. Connect the problem to business consequences.

Most prospects understate the cost of their problems — they've normalized the pain. Implication questions help them calculate the real cost, which justifies action.

**Principles:**
- These questions should feel like you're helping them think, not interrogating them
- Link the problem to revenue, headcount, customer experience, or competitive position
- Never answer the implication yourself — let them surface it

**Templates to customize:**
- "What happens downstream when [problem] occurs — who else does it affect?"
- "If [problem] stays unsolved for another year, where does that leave you?"
- "What's the impact on [team/customers/revenue] when [problem] happens?"
- "How much time is your team spending on [workaround] each week?"

---

### LAYER 5: BUYING PROCESS QUESTIONS (3–4 questions)
**Purpose:** Qualify the opportunity and map the path to close.

These questions separate serious buyers from tire-kickers. Asked naturally, they don't feel pushy — they feel like you're being organized.

**Principles:**
- Ask about decision process, not just decision-maker — there are usually multiple stakeholders
- Surface timeline and budget without leading with those words
- Find out what "good" looks like — their success criteria become your proposal's language

**Templates to customize:**
- "If you decided this was the right solution, what would the process look like to get it approved?"
- "Who else would be involved in a decision like this?"
- "What's driving the timing on your end — is there a forcing function?"
- "What does success look like for you in 90 days if you moved forward?"
- "Have you looked at other solutions? Where are you in that process?"
- "Is there a budget allocated for this, or would that need to be established?"

---

## Step 4: Add the Tailored Layer

After the standard five layers, add **3–5 prospect-specific questions** drawn from research on the company, role, or industry.

These are the questions that make prospects say "how did you know about that?" They're built from:

- **Company news:** Recent funding, product launches, expansions, executive hires, press
- **Industry trends:** Regulatory changes, market shifts, competitive pressure specific to their sector
- **Role-specific concerns:** What a [title] at a [stage] company is typically measured on / anxious about right now
- **Inferred pain from context:** If they're a fast-growing logistics company, ask about the operational strain of growth; if they're a Series B SaaS, ask about go-to-market efficiency

**Label these clearly in the output** so the seller knows they're the differentiated questions.

---

## Step 5: The Must-Ask Five

After the full list, distill to the **5 questions the seller must ask** — the non-negotiables if the call goes short or gets derailed.

These should cover:
1. The main problem (in their words)
2. The cost or consequence of the problem
3. What success looks like
4. Who else is involved in the decision
5. What's driving the timing

Present these separately so the seller can keep them visible during the call.

---

## Step 6: Questions NOT to Ask

For each call context, include 3–5 questions to actively avoid — either because they're lazy, insulting, or kill trust.

**Universal avoid list:**
- ❌ "What keeps you up at night?" — cliché, been asked a thousand times
- ❌ "What's your budget?" as the first or second question — premature and transactional
- ❌ "Can you tell me about your company?" — they'll wonder if you Googled them at all
- ❌ "Are you the decision-maker?" — condescending; ask about process instead
- ❌ Questions that can be answered with "yes" or "no" — they end conversations
- ❌ Multi-part questions — "Can you tell me about X, Y, and Z?" — only the last one gets answered
- ❌ Leading questions — "You'd agree that [your product's value prop], right?" — obvious and off-putting

Add context-specific avoid questions based on their industry or role.

---

## Step 7: Call Flow Note

Append a brief note on how to use the list during the call:

```
HOW TO USE THIS LIST

Don't read it. Know it.
Print or open it before the call. Pick your 5 must-ask questions. 
The rest are backup if the conversation goes somewhere unexpected.

The goal is not to ask all 20 questions. The goal is to have 
enough questions that you're never grasping for what to say next.

Listen for the answer behind the answer. When they say something 
unexpected, follow that thread — even if it means leaving a 
planned question behind. The best discoveries happen off-script.

Take notes on their exact words. The language they use to describe 
their problem is the language your proposal should mirror back.
```

---

## Output Format

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DISCOVERY CALL PREP: [Prospect Name/Role] @ [Company]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

WHAT YOU KNOW GOING IN:
[2–4 bullet summary of what the skill inferred about the prospect 
and their likely context — shows the seller the homework was done]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⭐ THE 5 YOU MUST ASK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[5 questions, numbered, no explanation needed — these are obvious]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
FULL QUESTION BANK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

OPENING (set the tone)
1. [Question]
2. [Question]

SITUATION (map the current state)
3. [Question]
4. [Question]
5. [Question]

PROBLEM (surface the pain — most important)
6. [Question]
7. [Question]
8. [Question]
9. [Question]

IMPLICATION (expand the pain)
10. [Question]
11. [Question]
12. [Question]

BUYING PROCESS (qualify and map the close)
13. [Question]
14. [Question]
15. [Question]
16. [Question]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎯 TAILORED TO [COMPANY/ROLE]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[3–5 questions specific to their company, role, or industry moment]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
❌ DON'T ASK THESE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[3–5 questions to avoid for this specific context, with brief reason]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
HOW TO USE THIS LIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Brief usage note]
```

---

## Quality Check

Before delivering:
- [ ] Are the Must-Ask Five genuinely the most essential — not just the easiest?
- [ ] Are all problem questions open-ended, not yes/no?
- [ ] Is there at least one question that would surprise the prospect — proving research was done?
- [ ] Does no question repeat information they've already shared (from email/context)?
- [ ] Are the tailored questions actually tailored — not generic questions with the company name pasted in?
- [ ] Is the "Don't Ask" list specific and honest — not just filler?
- [ ] Is the full list under 20 questions (more than that becomes paralyzing)?
- [ ] Does the sequence flow naturally — would it feel like a conversation, not a survey?
