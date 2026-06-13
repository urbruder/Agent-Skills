# Amazon A9 / A10 Algorithm Reference

## How Amazon Ranks Listings

Amazon's search algorithm (A9, now evolving toward A10) ranks products based on two axes:
**relevance** and **performance**. A listing must win on both to reach page one.

---

## Relevance Signals (Can Be Controlled in Listing Copy)

### Title Weight
The title carries the heaviest keyword weight of any field. Amazon indexes every word.
- Primary keyword must appear **within the first 5 words** of the title for maximum relevance
- Format that consistently ranks: `Brand | Primary Keyword | Key Feature | Variant (size/color/count)`
- 150–200 characters is the sweet spot (mobile truncates at ~80 chars — make those first 80 count)
- No keyword stuffing — Amazon suppresses listings that look like keyword strings

### Bullet Points
- Amazon indexes bullet text for search
- Each bullet should contain exactly one secondary or long-tail keyword, placed naturally
- Bullets that lead with customer benefits (not product features) convert better
- Mobile shows only the first 2–3 bullets above the fold — make those the strongest

### Product Description
- Indexed for search but weighted lower than title and bullets
- Use it to capture long-tail terms and use-case variations that didn't fit in bullets
- HTML formatting (bold, line breaks) is allowed in standard descriptions
- A+ Content replaces the standard description and is NOT indexed for search — it's a conversion tool only

### Backend Search Terms (Subject & Keywords Field)
- 250 bytes max (not characters — special characters cost more bytes)
- No commas (Amazon ignores them, they just waste bytes)
- No repetition of words already in title, bullets, or description (Amazon already indexes those)
- Good candidates: misspellings, abbreviations, Spanish/bilingual terms, synonyms, use cases
- Example for a yoga mat: `exercise mat thick non slip pilates workout floor gym meditation stretching kids

### Category & Browse Nodes
- Correct category selection dramatically affects discoverability
- Wrong category = invisible to customers browsing that section
- Use Amazon's category tree; never force a product into a slightly wrong node to avoid competition

---

## Performance Signals (Affect Ranking Over Time)

### Click-Through Rate (CTR)
- Driven primarily by: main image quality, price, review count, review rating, title clarity
- Amazon tests different listings against each other — higher CTR wins more impressions
- **Implication for listing rewrites**: the title must be compelling in search results, not just keyword-rich

### Conversion Rate (CVR)
- % of sessions that result in a purchase
- Affected by: images, bullets, price, reviews, A+ content, video
- Amazon rewards high-converting listings with better placement
- **Implication**: every bullet and the description must reduce friction and handle objections

### Sales Velocity
- How many units sell per day/week
- New listings have no history — this is why PPC and external traffic matter for new products
- Amazon tracks whether sales are organic or ad-driven — organic sales carry more weight
- **Note to sellers**: listing quality gets you indexed; sales velocity gets you ranked

### Return Rate
- High return rates signal product/listing mismatch
- If your listing promises something the product doesn't deliver, returns spike and ranking drops
- **Implication**: accurate listings outperform exaggerated ones in the long run

---

## Suppression & Listing Health

Amazon suppresses (makes unsearchable) listings that:
- Are missing a main image
- Have pricing errors or no active offer
- Contain prohibited words in the title (check Amazon's restricted keywords list)
- Exceed title character limits in certain categories
- Have duplicate content from another ASIN

Check listing health in Seller Central > Inventory > Fix Stranded Inventory.

---

## A10 Updates (Post-2021 Shifts)

A10 places increased weight on:
- **Organic sales over PPC sales** — ads help but don't replace organic performance
- **External traffic** — sending traffic from social/email to your listing boosts ranking
- **Seller authority** — account health, feedback score, fulfillment method (FBA ranks higher)
- **Relevance matching** — stuffing irrelevant keywords now hurts more than it helps

---

## Quick Reference: Keyword Placement Priority

| Field | Search Weight | Char Limit | Notes |
|---|---|---|---|
| Title | Highest | 150–200 | Primary + 1–2 secondary KWs |
| Bullets | High | 500 each | 1 KW per bullet, naturally placed |
| Description | Medium | 2,000 | Long-tail terms, use cases |
| Backend Terms | Medium | 250 bytes | Leftovers: synonyms, misspellings |
| A+ Content | Not indexed | N/A | Conversion only |
| Brand Name | Indexed | — | Appears separately in search |
