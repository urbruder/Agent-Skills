# Pattern Library: Win/Loss Analysis

Extended reference for pattern detection, sub-types, and industry-specific signals.

---

## Pattern Deep-Dives

### Competitive Loss — Sub-types

**Known competitor, repeated loss**
- Same name appearing in 3+ deals = systemic gap, not rep execution
- Ask: Are we losing at same stage each time? (positioning problem vs. demo problem vs. proof problem)
- Fix direction: Competitive battlecard, objection inoculation early in cycle, targeted social proof

**Unknown/unnamed "someone else"**
- "Went with another solution" with no name = prospect was too polite, or champion didn't know
- Treat as soft competitive loss
- Fix direction: Ask directly in loss call — "Would you be comfortable sharing who you went with?"

**Replaced by build-internally**
- "Decided to build it themselves" — often means: price too high, ROI unclear, or product not differentiated enough
- Fix direction: Total cost of ownership / build-vs-buy narrative, risk framing

**Status quo wins**
- "Decided not to move forward with anything" — urgency was never real
- Fix direction: Urgency creation earlier in cycle, better qualification of trigger events

---

### Price / Budget — Sub-types

**Genuine budget constraint**
- Signals: Budget mentioned in discovery, deal size above normal range, mid-market/SMB segment, economic headwinds
- Fix direction: Phased rollout offer, ROI calculator, flexible payment terms

**Value gap disguised as price**
- Signals: Price objection comes AFTER demo, not before; prospect bought a similar-priced competitor
- Fix direction: Value articulation in demo, quantify ROI earlier, case studies with specific numbers

**Price used as polite no**
- Signals: Price objection appears suddenly at close, champion went quiet before it
- Fix direction: This is a champion loss or competitive loss — fix the diagnosis, not the pricing

**Budget frozen / timing issue**
- Signals: "Not this quarter", fiscal year constraints, M&A situation
- Fix direction: Future-date the deal, nurture sequence, exec relationship maintenance

---

### Champion / Stakeholder Loss — Sub-types

**Champion left**
- One of the most common silent killers
- Fix direction: Multi-thread earlier — always know 2 internal champions; ask "Who else has a stake in this decision?"

**Champion couldn't sell internally**
- Signals: "We presented it but couldn't get approval", "my boss wanted something different"
- Fix direction: Champion enablement — provide decks, ROI models, and talking points for internal selling; executive sponsor introductions

**Decision escalated unexpectedly**
- Signals: "Turned out procurement/legal/CFO needed to be involved"
- Fix direction: Ask early — "What does your approval process look like for something at this investment level?"

**Wrong champion from the start**
- Signals: Champion was an influencer, not a decision-maker or budget owner
- Fix direction: Qualification framework — identify economic buyer by deal stage 2

---

### Discovery / Fit Failure — Sub-types

**Wrong ICP entered pipeline**
- Signals: Loss reasons like "not the right use case", "too complex for us", "actually we need X not Y"
- Fix direction: Tighten lead qualification criteria, add disqualification questions to SDR scripts

**Fit problem surfaced too late**
- Signals: Late-stage losses with fit-related reasons that should have been discoverable
- Fix direction: Add deal-killer questions earlier — "Do you currently have X? Without it, our solution doesn't work"

**Use case mismatch**
- Signals: Customer expected one thing, got another in demo
- Fix direction: Better needs discovery before demo; custom demo prep; discovery-to-demo handoff notes

---

### Trust / Credibility Gap — Sub-types

**Company too new / unproven**
- Signals: "We went with a more established vendor", "concerned about your longevity", "need a company we know will be around"
- Fix direction: Reference customers, funded/backing narrative, case studies from similar companies, executive relationships

**No proof for their industry/segment**
- Signals: "Don't have customers like us", "we're different from your typical customer"
- Fix direction: Industry-specific case studies, advisory board from their sector, targeted pilot offers

**Rep credibility gap**
- Signals: Feedback about rep being too junior, too pushy, not understanding their business
- Fix direction: SE/executive involvement in deals, rep coaching, industry knowledge training

**Negative word-of-mouth**
- Signals: "We heard from [company] that...", G2/Capterra reference
- Fix direction: Review management, reference customer program, proactive reputation building

---

## Industry-Specific Loss Patterns

### B2B SaaS

Common patterns:
- **Integration gap** — "Doesn't connect to [Salesforce/HubSpot/Slack/etc.]" — track which integrations are blocking deals
- **Security/compliance review** — Especially enterprise; SOC2, GDPR, enterprise SSO
- **Per-seat pricing sensitivity** — Large teams balk at per-seat; consider platform pricing
- **Free tier competitor** — Freemium competitor offering "good enough" for free

Watch for: Deals lost at legal/security stage cluster = need pre-built security questionnaire responses and faster compliance review process

### Professional Services / Agencies

Common patterns:
- **Price vs. offshore** — Lost to cheaper offshore alternative
- **Credibility gap** — "We went with a larger agency"
- **Chemistry/fit** — Subjective; hard to fix but real
- **Scope ambiguity** — Prospect wasn't clear on what they were buying; lost when reality set in

Watch for: High proposal-stage loss rate = proposals aren't converting; often means scope clarity or pricing structure issue

### Enterprise Sales

Common patterns:
- **Procurement/legal delays** — Urgency dies in legal review
- **Sponsor change** — Executive sponsors leave or get reorganized
- **IT/security veto** — Technical team blocks despite business champion
- **Rollout complexity** — "Too much change management risk"

Watch for: Long-cycle deals going dark = multi-thread failure; deals weren't spread across enough stakeholders

### SMB Sales

Common patterns:
- **"Do it ourselves"** — Owner-operated businesses often prefer DIY
- **Cash flow timing** — Not budget freeze, literally cash flow
- **Decision fatigue** — Too many tools being evaluated
- **No urgency** — Pain exists but not acute enough to buy now

Watch for: High ghosting rate in SMB = urgency was never real; improve trigger event qualification

---

## Example Analysis Outputs by Data Quality

### Thin Data (3–5 deals, sparse notes)

```
WIN/LOSS DEBRIEF ANALYSIS
─────────────────────────────────
Deals analyzed: 4
Outcomes: 4 lost
Data quality: Thin — notes are brief and loss reasons are surface-level. 
Treat these as directional signals, not confirmed patterns.

TOP PATTERNS

PATTERN #1: Competitive Loss (likely)
Frequency: 2 of 4 deals
Summary: Two deals reference "going with another vendor" without naming them. 
Without more context, this is probably competitive, though "not right now" can't 
be ruled out.
Root cause: Unclear — could be positioning, trust, or feature gap. 
Need more data to distinguish.
Fix: Start capturing competitor names in your CRM loss fields. 
Ask directly in every loss: "Would you mind sharing who you went with?"

QUESTIONS TO INVESTIGATE
- What stage did each deal reach before being lost?
- Were these inbound or outbound deals?
- Any common company size or industry?

WHAT'S MISSING FROM YOUR DATA
- Competitor names
- Stage at which deal was lost
- Deal size
- Stated vs. real reason (need a loss call habit)
```

### Rich Data (15+ deals, detailed notes)

```
WIN/LOSS DEBRIEF ANALYSIS
─────────────────────────────────
Deals analyzed: 18
Outcomes: 13 lost / 3 won / 2 no decision
Data quality: Strong — notes include stage, competitor names, deal sizes, 
and rep commentary.

TOP PATTERNS

PATTERN #1: Champion Enablement Failure
Frequency: 7 of 13 losses (54%)
Summary: In 7 deals, the internal champion expressed enthusiasm but 
couldn't get internal approval. Common phrases: "we loved it but couldn't 
get sign-off", "CFO wanted to see more ROI", "my manager preferred X".
Root cause: Champions are being sent to internal meetings without the tools 
to sell upward. You're winning the champion but losing the buying committee.
Fix: Build a champion toolkit — a 5-slide internal business case template, 
a one-page ROI calculator with their numbers pre-filled, and a short FAQ 
for executive objections. Deliver this before every proposal. 
Offer to join an internal call with the CFO or VP.

[continues...]
```
