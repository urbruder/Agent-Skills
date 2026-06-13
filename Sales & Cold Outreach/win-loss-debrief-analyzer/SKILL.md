---
name: win-loss-debrief-analyzer
description: >
  Use this skill whenever someone wants to analyze why they're winning or losing deals. Triggers include: "why am I losing deals", "win loss analysis", "lost deal patterns", "sales debrief", "deal post-mortem", "analyze my lost deals", "why did we lose", "win rate is dropping", "paste lost deal notes", "CRM notes analysis", "sales patterns", "competitor losing deals", "objection patterns", "churn analysis", or any request to find patterns across sales outcomes. Also trigger when someone pastes a batch of deal notes, CRM exports, call transcripts, or loss reason data and wants insight. This skill turns messy, unstructured deal notes into prioritized patterns and concrete fixes — use it proactively whenever sales outcomes are being discussed.
---

# Win/Loss Debrief Analyzer

Turns raw deal notes, CRM exports, or free-text loss reasons into clear patterns — and translates each pattern into a specific, actionable fix.

---

## Step 1: Intake & Triage

Accept input in any of these forms:
- Pasted free-text notes (one deal or many)
- Bullet lists of loss reasons
- CRM field exports (CSV-style or formatted)
- Call/email transcript excerpts
- A mix of the above

**If input is thin (fewer than 3 deals or very sparse notes):**  
Work with what's there, but flag it: "With [N] deals, these patterns are directional — the more data you add, the more confident we can be."

**If input has no outcome labels (win vs. loss):**  
Ask: "Are all these losses, or is this a mix of wins and losses?" — knowing both makes the analysis more powerful.

**Infer context when possible.** If someone pastes 8 notes full of "went with competitor" and "budget cut", don't ask clarifying questions — start analyzing.

---

## Step 2: Normalize & Tag Each Deal

Before pattern analysis, mentally normalize each deal into:

| Field | What to extract |
|---|---|
| **Outcome** | Won / Lost / Ghosted / No decision |
| **Stated reason** | What they said (the surface reason) |
| **Inferred reason** | What actually likely happened (read between the lines) |
| **Stage lost** | Discovery / Demo / Proposal / Legal / Closed-Lost |
| **Signals** | Keywords: competitor named, price mentioned, timing, champion left, internal politics, feature gap, trust/credibility issue, etc. |
| **Deal size / segment** | If mentioned |

You won't always have all fields — fill what you can, note what's missing.

---

## Step 3: Pattern Detection

Group deals into pattern clusters. Look for:

### Loss Pattern Categories

**1. Competitive Loss**
- Same competitor named repeatedly
- "Went with someone else" without reason (often competitive)
- "More established", "bigger brand", "already using X"

**2. Price / Budget**
- Distinguish: genuine budget constraint vs. perceived value gap vs. price used as an excuse
- "Too expensive" after a demo = often value, not price
- "Budget frozen" mid-cycle = timing/economic issue

**3. Champion / Stakeholder Issues**
- Champion left, changed role, lost internal support
- Decision escalated to someone you never met
- "Internal alignment issues", "politics", "committee"

**4. Timing / Not Now**
- "Not a priority right now"
- Deals that stalled vs. deals that went to a competitor
- Stalls at same stage repeatedly = friction in that stage

**5. Feature / Product Gap**
- Specific feature named repeatedly
- "Doesn't integrate with X"
- "Not enterprise-ready", "missing Y"

**6. Discovery / Fit Failure**
- Wrong ICP — deals that should never have been qualified
- Misaligned use case that surfaced late
- "Not what we were looking for" (often a discovery miss)

**7. Trust / Credibility Gap**
- "Too new", "haven't seen proof", "don't have customers like us"
- Social proof gap, case study gap
- Referenced a bad review or word-of-mouth

**8. Process / Internal Friction**
- Legal/security review killed deal
- Procurement delays lost urgency
- Champion couldn't get budget approved

---

## Step 4: Output Structure

Deliver the analysis in this format:

```
WIN/LOSS DEBRIEF ANALYSIS
─────────────────────────────────
Deals analyzed: [N]  
Outcomes: [X lost / Y won / Z ghosted]  
Data quality: [Strong / Moderate / Thin — and why]

─────────────────────────────────
TOP PATTERNS (ranked by frequency/impact)

PATTERN #1: [Name]
Frequency: [X of N deals]
Summary: [2–3 sentence description of what's actually happening]
Root cause: [What's really driving this — not just the surface symptom]
Fix: [Specific, actionable recommendation — not generic advice]

PATTERN #2: [Name]
...

[Continue for all significant patterns — typically 3–6]

─────────────────────────────────
QUICK WINS (highest leverage, lowest effort)
- [Specific action]
- [Specific action]

DEEPER FIXES (structural changes worth considering)
- [Specific action]

─────────────────────────────────
QUESTIONS TO INVESTIGATE
[Things the data hints at but doesn't confirm — worth digging into]

WHAT'S MISSING FROM YOUR DATA
[Fields or context that would sharpen the analysis if collected going forward]
```

---

## Step 5: Fix Quality Standards

Every fix must be:

**Specific, not generic.**  
❌ "Improve your discovery process"  
✅ "Add a question in discovery that explicitly surfaces budget authority — 'Who else needs to sign off on something like this?' — you're losing 3 deals at proposal stage to people you never met"

**Matched to the pattern's root cause, not its surface symptom.**  
If "price objections" are actually a value articulation problem, say so — and fix that, not discounting.

**Staged appropriately:**
- Quick wins = changes a rep can make in their next call
- Deeper fixes = process, collateral, product, or positioning changes

---

## Step 6: Win Pattern Analysis (if wins are included)

If won deals are in the data, run the same analysis for wins and add a section:

```
WIN PATTERNS — WHAT'S WORKING
[Same pattern format]

REPLICATION OPPORTUNITIES
[How to engineer more of these conditions into the sales process]
```

Compare win vs. loss patterns to surface the actual differentiators — not just what reps think is working.

---

## Step 7: Offer Follow-Ups

After delivering the analysis, offer:

- **Competitive counter-cards** — if a specific competitor keeps appearing, offer to draft a competitive battlecard
- **Objection handling scripts** — for the top 1–2 objection patterns
- **Discovery question rewrites** — if discovery failure is a pattern
- **A template for capturing better loss data** — if the input was thin or inconsistent
- **A rep coaching brief** — a short version of findings formatted for a 1:1 or team meeting

---

## Analyst Mindset: What to Watch For

### "Price" is rarely just price
When "too expensive" appears without context, probe or note: was this after a demo? After proposal? Did they buy a competitor at a similar price point? Price objections at proposal stage almost always mean value wasn't established earlier.

### Ghosting is data
Deals that go dark without a stated reason are usually: (a) competitive losses the prospect was too polite to say, (b) champion lost internal support, or (c) urgency was never real. Don't ignore them.

### Stage-of-loss concentration is a signal
If 60% of losses happen at the same stage, that stage has a specific problem — don't spread fixes across the whole process.

### Stated reason ≠ real reason
Prospects are polite. "Budget" often means "not a priority." "Going with someone else" often means "we didn't trust you enough." "Not the right time" often means "your champion couldn't sell it internally." Read between the lines and flag when you're doing so.

### Small N, big patterns
Even 5–10 deals can reveal clear directional patterns. Be honest about confidence levels but don't refuse to find patterns just because the sample is small.

---

## Reference Files

See `references/pattern-library.md` for:
- Extended pattern descriptions and sub-types
- Industry-specific loss patterns (SaaS, services, enterprise, SMB)
- Example analysis outputs for different data quality levels
