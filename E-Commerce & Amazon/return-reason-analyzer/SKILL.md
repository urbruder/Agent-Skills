---
name: return-reason-analyzer
description: analyze ecommerce return reasons, refund notes, support tickets, rma data, customer complaints, reviews, or post-purchase feedback to find root causes and recommend product, page, sizing, expectation-setting, packaging, shipping, quality, copy, merchandising, and operational fixes that reduce avoidable returns.
---

# Return-Reason Analyzer

Turn return and refund data into a prioritized roadmap for fewer returns and better customer expectations.

## Core workflow

When the user provides product, store, catalog, customer, competitor, campaign, review, return, or ecommerce context:

1. Cleanly group return reasons by theme.
2. Separate symptom from likely root cause.
3. Prioritize fixes by frequency, cost, preventability, and customer impact.
4. Recommend fixes across product page, product, operations, packaging, sizing, support, and post-purchase education.
5. Avoid overclaiming causality when data is thin.

If useful inputs are missing, make practical assumptions and label them briefly. Do not invent proof, reviews, metrics, claims, policies, or customer data.

Use `references/return-reason-analyzer-framework.md` for deeper analysis, variants, templates, and quality checks.

## Default output

```markdown
## Return Analysis Summary
- Product/category:
- Data source:
- Time period:
- Main return drivers:

## Return Reason Clusters
| Cluster | Example reasons | Likely root cause | Fix type | Priority |
|---|---|---|---|---|

## Root-Cause Findings
1. [Finding]
2. [Finding]
3. [Finding]

## Recommended Fixes
### Product Page / Copy
- [Fix]

### Images / Sizing / Expectations
- [Fix]

### Product / Quality
- [Fix]

### Fulfillment / Packaging / Shipping
- [Fix]

### Customer Support / Post-Purchase
- [Fix]

## Quick Wins
- [Action]
- [Action]

## Data Gaps
- [Missing data that would improve diagnosis]
```

## Ecommerce quality standards

Prioritize:

- conversion clarity
- customer language
- benefit-driven copy
- accurate product claims
- objection handling
- brand consistency
- marketplace or store-platform fit
- practical next actions
- ethical use of customer and competitor data

## Guardrails

Do not:

- invent product capabilities, guarantees, certifications, ingredients, materials, test results, or customer quotes
- make medical, financial, legal, or safety claims without user-provided substantiation
- use deceptive scarcity
- copy competitor language verbatim
- recommend manipulating reviews, creators, or customers
- ignore marketplace/platform compliance constraints

## Final quality check

Before responding, verify that the output is specific, commercially useful, grounded in the provided inputs, and ready for an ecommerce operator, marketer, founder, or copywriter to use.
