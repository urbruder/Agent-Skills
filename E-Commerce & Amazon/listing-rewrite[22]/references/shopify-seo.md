# Shopify / Google Shopping SEO Reference

## How Shopify Products Get Found

Shopify products surface in two distinct search contexts:
1. **Google Search & Google Shopping** — organic and paid search results
2. **Shopify's own storefront search** — on-site product search (powered by Shopify Search & Discovery app or Predictive Search API)

Optimizing for both requires slightly different approaches, but they share the same foundation: keyword-rich, readable, well-structured product content.

---

## Google Shopping Optimization (Most Important)

Google Shopping pulls product data from your Shopify store via the Google & YouTube Sales Channel or a product feed. The fields it reads are:

### Product Title (Most Critical)
- Google uses the product title as the primary relevance signal for Shopping ads
- **Optimal structure varies by category:**
  - Apparel: `Brand + Gender + Product Type + Attributes (color, size, material)`
  - Electronics: `Brand + Product Type + Model + Key Spec`
  - Home goods: `Brand + Product Type + Material + Size/Color`
- Target length: 50–70 characters (Google truncates longer titles in ad display)
- Front-load the primary keyword — Google weights the beginning of the title more heavily
- Avoid: promotional text ("Free Shipping", "Best Price"), ALL CAPS, special characters

### Product Description (Used for Matching, Not Displayed)
- Google uses the description to match products to search queries
- Write the first 150–200 words keyword-rich — Google prioritizes the beginning
- Use natural language; avoid keyword lists
- Include: material, dimensions, use case, compatibility, target user
- Shopify's description field maps directly to Google's `description` attribute

### Product Type Field
- Often overlooked — maps to Google's `product_type` attribute
- Use Google's taxonomy when possible for better categorization
- Example: `Apparel & Accessories > Clothing > Activewear > Yoga Pants`

### Google Product Category
- Set this explicitly in your Google channel or metafields
- Correct categorization improves eligibility for Google Shopping features (ratings, price drops)

---

## Shopify Storefront SEO Fields

Every Shopify product has two SEO-specific fields (Edit website SEO section):

### SEO Title (Page Title)
- Different from the product title — optimized for Google organic search, not Shopping
- Target: 50–60 characters
- Format: `Primary Keyword | Product Name | Brand`
- This appears as the blue link in Google search results
- If left blank, Shopify uses the product title — usually suboptimal

### Meta Description
- 150–160 characters
- Not a ranking factor but affects click-through rate from organic search
- Include the primary keyword naturally in the first sentence
- End with a soft CTA: "Shop now", "Free shipping on orders over $X"
- Write for humans — this is your ad copy in organic results

---

## Product Description Best Practices (Shopify)

### Structure for SEO + Conversion
```
[Keyword-rich opening paragraph — 2–3 sentences, includes primary + 1 secondary keyword]

KEY FEATURES:
• Feature → Benefit (no more than 6 bullets)
• Keep each bullet under 20 words
• Use plain language

[Closing paragraph: use case, who it's for, or trust signal]
```

### Schema Markup
Shopify auto-generates basic product schema (JSON-LD). To improve rich results eligibility:
- Ensure price, currency, and availability are accurate
- Add review markup (use a reviews app like Okendo or Judge.me)
- Add product identifiers: MPN, GTIN/UPC/ISBN/EAN (enter in product metafields or variants)

### Image Alt Text
- Shopify does not auto-populate alt text — it must be added manually per image
- Format: `[Primary keyword] - [product variant] - [brand]`
- Example: `Stainless steel water bottle 32oz - Matte Black - HydroFlow`
- This is an easy win most sellers miss

---

## Shopify's On-Site Search

Shopify Search & Discovery indexes:
- Product title (weighted highest)
- Product tags
- Product type
- Vendor/brand name
- Variant options (size, color, material)
- Description (lower weight)

**Implication**: Tags are a stealth SEO lever for on-site search. Add 10–15 relevant tags per product covering synonyms, use cases, and customer language.

---

## URL Handle (Slug)
- Shopify auto-generates from product title but you can edit it
- Keep it short and keyword-rich: `/products/stainless-steel-water-bottle-32oz`
- Remove filler words: no "the", "a", "and" in URLs
- Don't change URLs on live products with backlinks — creates 404s unless redirects are set

---

## Collection Pages (Category SEO)
- Collection pages often rank better than individual product pages for broad terms
- Optimize collection page title and description with category-level keywords
- Example: the collection "Yoga Mats" should rank for "buy yoga mat" — the product page targets "6mm non-slip yoga mat with alignment lines"

---

## Quick Reference: Shopify SEO Checklist per Product

| Element | Target | Notes |
|---|---|---|
| Product Title | 50–70 chars | Keyword-first, structured by category |
| SEO Title | 50–60 chars | Different from product title if needed |
| Meta Description | 150–160 chars | CTA included |
| Description opening | 150–200 words | Keyword-rich, natural language |
| Image alt text | All images | [KW] - [variant] - [brand] |
| URL slug | Short + keyword | No stop words |
| Tags | 10–15 per product | Synonyms, use cases |
| Product type | Google taxonomy | Improves Shopping eligibility |
| GTIN/UPC | If available | Needed for Google Shopping trust |
| Reviews | 4.0+ rating | Affects Google Shopping CTR |
