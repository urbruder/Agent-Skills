---
name: ad-copy-variant-generator
description: create 10 distinct business-focused ad copy variants for split-testing from one offer, product, landing page, campaign idea, audience, or brief. use when the user needs multiple paid social, search, display, native, retargeting, or email ad angles instead of one ad. prioritize conversion clarity, credible differentiation, audience-message fit, platform adaptability, testing discipline, and compliance-aware copy over hype, vague claims, or repetitive rewrites.
---

# Ad Copy Variant Generator

Generate 10 meaningfully different ad variants so the user can test angles, not just wording.

## Default behavior

When the user provides an offer, product, service, audience, landing page summary, campaign idea, or rough ad concept:

1. Extract the campaign inputs:
   - product or offer
   - target audience
   - customer pain point or desired outcome
   - offer mechanism or differentiator
   - proof, credibility, or reason to believe
   - desired action
   - platform if specified
   - constraints such as character limits, claims, tone, or compliance needs

2. If key inputs are missing, make practical assumptions and label them briefly. Do not block on clarification unless the missing detail would make the ads misleading.

3. Create exactly 10 ad variants unless the user requests another number.

4. Make each variant a different strategic angle, not a minor rephrase.

5. Keep copy business-useful, clear, credible, and testable.

6. Avoid unsupported claims, fake urgency, exaggerated guarantees, and manipulative targeting language.

7. Use `references/ad-angle-framework.md` when the user asks for deeper angle strategy, more variants, platform-specific constraints, or a testing plan.

## Default output

Use this structure unless the user asks for a different format:

```markdown
## Assumptions
- Audience: [assumption or provided input]
- Offer: [assumption or provided input]
- Primary conversion goal: [assumption or provided input]
- Platform: [assumption or provided input]

## 10 Ad Variants

### 1. [Angle name]
**Primary text:** [ad copy]
**Headline:** [headline]
**Description:** [optional description if useful]
**CTA:** [call to action]
**Why test it:** [what this variant is testing]

### 2. [Angle name]
...
### 10. [Angle name]

## Recommended Test Setup
- Test variable: angle/message, not design and copy at the same time
- Suggested winner metric: [CTR, CVR, CPL, CPA, ROAS, demo rate, or pipeline quality]
- First-round recommendation: launch all 10 if budget allows, or start with variants [x], [y], and [z]
```

## Variant requirements

Each set of 10 should usually include:

1. Pain-point angle
2. Outcome or transformation angle
3. Differentiation angle
4. Proof or credibility angle
5. Speed or simplicity angle
6. Risk-reversal angle
7. Cost-of-inaction angle
8. Objection-handling angle
9. Aspirational or identity angle
10. Direct offer angle

Adapt the mix if another structure is better for the campaign.

## Platform adaptation

If a platform is provided, tune the format:

- **LinkedIn ads:** professional, problem-aware, business outcome-oriented, concise but not overly casual.
- **Meta ads:** sharper hooks, conversational language, benefit-led copy, clear CTA.
- **Google search ads:** keyword-aligned headlines and descriptions, strong intent match, no fluff.
- **YouTube ads:** first 5 seconds matter; lead with pain, surprise, or clear outcome.
- **Retargeting ads:** assume awareness; focus on proof, objections, offer, urgency, or next step.
- **Email sponsor ads:** native, credibility-led, audience-trust preserving.

## Copy quality standards

Good ad variants should:

- make the target buyer feel recognized
- present one clear reason to care
- make the next step obvious
- connect pain, outcome, proof, and CTA
- use concrete language instead of generic benefits
- create useful testing signal across different motivations
- be credible enough for a serious business audience

## Guardrails

Do not:

- invent statistics, awards, customer names, or performance claims
- imply guaranteed outcomes unless provided by the user
- use sensitive personal attributes in targeting language
- overuse hype words like revolutionary, game-changing, insane, secret, or guaranteed
- produce 10 near-identical rewrites
- hide weak assumptions

If the user provides regulated or high-risk subject matter, add a brief compliance note and keep claims conservative.

## Optional add-ons

When useful, include one of these sections after the variants:

```markdown
## Angle Map
| Variant | Funnel stage | Buyer motivation | Risk level | Best platform |
|---|---|---|---|---|
```

```markdown
## Creative Direction
- Visual idea:
- Hook overlay:
- Landing page alignment:
```

```markdown
## Search Ad Format
| Variant | Headlines | Descriptions | Keywords/Intent |
|---|---|---|---|
```

## Voice and tone

Default to polished, direct, business-oriented copy. Adjust to founder-led, premium, bold, conversational, technical, enterprise, SMB, or playful only when the user asks or the offer clearly requires it.

## Final check

Before responding, verify that:

- there are exactly 10 variants
- each variant tests a distinct angle
- every variant has a headline, primary text, CTA, and reason to test
- claims are supported by the provided input or framed cautiously
- the output is ready for a marketer to paste into an ad planning document
