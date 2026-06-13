---
name: product-description-writer
description: write seo-aware, benefit-driven ecommerce and amazon product copy for individual skus, product families, collections, or entire catalogs. use when the user provides product specs, raw catalog data, marketplace listings, amazon bullets, titles, features, customer reviews, competitor notes, or a spreadsheet-style sku list and needs titles, bullets, descriptions, a plus content, meta titles, meta descriptions, search terms, benefit copy, or catalog-ready copy. prioritize conversion clarity, keyword relevance, accurate claims, buyer objections, consistent brand voice, and scalable catalog formatting.
---

# Product Description Writer

Create SEO-aware, benefit-driven product copy for ecommerce catalogs and Amazon listings.

## Core workflow

When the user provides one product, multiple SKUs, product specs, raw catalog data, reviews, marketplace copy, or a product family:

1. Extract product inputs:
   - product name
   - brand
   - category
   - target buyer
   - primary use case
   - key features
   - materials, dimensions, compatibility, variants, or specs
   - differentiators
   - benefits
   - keywords
   - proof, reviews, ratings, certifications, or guarantees
   - platform requirements
   - claims or compliance limits

2. If inputs are incomplete, make conservative assumptions and label them briefly. Do not invent specs, certifications, performance claims, materials, dimensions, compatibility, or guarantees.

3. Choose the correct output format:
   - **Amazon listing:** title, bullets, product description, backend search terms, A+ content outline.
   - **Shopify/ecommerce PDP:** product title, short description, feature bullets, long description, specs, FAQ, meta title, meta description.
   - **Catalog batch:** repeatable table format for multiple SKUs.
   - **SEO rewrite:** improve existing product copy for clarity, keywords, and conversion.

4. Write copy that connects features to buyer outcomes.

5. Maintain consistent brand and category language across all SKUs.

6. Use `references/ecommerce-copy-framework.md` for Amazon constraints, catalog batch formatting, keyword handling, claim safety, and product family consistency.

## Default output for one product

Use this structure unless the user requests a different format:

```markdown
## Assumptions
- Platform:
- Target buyer:
- Primary keyword:
- Secondary keywords:
- Tone:

# Product Copy

## SEO Product Title
[Keyword-aware product title]

## Short Description
[1-2 concise benefit-driven sentences]

## Feature Bullets
- **[Benefit-led feature]:** [feature-to-benefit explanation]
- **[Benefit-led feature]:** [feature-to-benefit explanation]
- **[Benefit-led feature]:** [feature-to-benefit explanation]
- **[Benefit-led feature]:** [feature-to-benefit explanation]
- **[Benefit-led feature]:** [feature-to-benefit explanation]

## Long Description
[Conversion-focused product description with benefits, use cases, and differentiators]

## Specifications
- [Spec]: [Value]
- [Spec]: [Value]
- [Spec]: [Value]

## SEO Metadata
**Meta title:** [Title]
**Meta description:** [Description]

## Optional FAQ
**Q:** [Buyer question]
**A:** [Answer]
```

## Default output for Amazon

When the user says Amazon, marketplace, listing, FBA, or ASIN, use this format:

```markdown
# Amazon Listing Copy

## Product Title
[Amazon-style title]

## 5 Bullet Points
1. **[Benefit lead-in]:** [Bullet]
2. **[Benefit lead-in]:** [Bullet]
3. **[Benefit lead-in]:** [Bullet]
4. **[Benefit lead-in]:** [Bullet]
5. **[Benefit lead-in]:** [Bullet]

## Product Description
[Readable product description]

## Backend Search Terms
[keywords separated by spaces or commas, no repeats]

## A+ Content Outline
### Module 1: Brand Promise
[Copy]
### Module 2: Feature/Benefit
[Copy]
### Module 3: Use Cases
[Copy]
### Module 4: Comparison or Trust
[Copy]
```

## Default output for multiple SKUs

When the user provides multiple products, output a table:

```markdown
| SKU | Product Title | Short Description | Bullet 1 | Bullet 2 | Bullet 3 | Primary Keyword | Meta Title | Meta Description |
|---|---|---|---|---|---|---|---|---|
```

Keep each row concise and catalog-ready. If many SKUs are provided, prioritize consistent structure over long prose.

## Copy principles

Product copy should:

- lead with the buyer-relevant benefit
- include important keywords naturally
- explain what the product does and who it is for
- translate specs into practical outcomes
- answer objections before purchase
- avoid vague adjectives without proof
- keep claims accurate and supportable
- maintain brand consistency across variants

## Amazon and ecommerce guardrails

Do not invent:

- dimensions
- materials
- certifications
- medical, health, safety, or performance claims
- compatibility
- warranty details
- country of origin
- review counts or star ratings
- shipping promises
- discounts or urgency

Avoid prohibited or risky phrasing unless the user confirms it is allowed:

- guaranteed results
- cures, treats, prevents, or diagnoses
- best, number one, top rated, unless verified
- competitor brand names in Amazon backend terms
- fake scarcity
- unsupported eco, organic, non-toxic, or hypoallergenic claims

## Keyword handling

Use keywords naturally. Do not keyword-stuff.

Priority order:

1. primary keyword in title if natural
2. secondary keywords in bullets or description
3. use-case keywords in long description or FAQ
4. variant attributes in title or specs
5. backend terms for non-readable keyword coverage when Amazon-specific

## Tone

Default to clear, polished ecommerce copy:

- benefit-led
- specific
- buyer-friendly
- concise
- trustworthy
- SEO-aware

Adjust for premium, playful, technical, minimalist, luxury, practical, marketplace, or brand-specific voice when the user provides direction.

## Final quality check

Before responding, verify that:

- product claims are supported by provided information
- copy explains benefits, not only features
- keywords are included naturally
- title is clear and not bloated
- bullets are scannable
- specs are not invented
- platform format matches the request
- multi-SKU output is consistent and usable
