# Platform Rules Reference

Authoritative field-by-field requirements for each ecommerce platform. Read this before
finalizing any listing rewrite.

---

## AMAZON

### Title
- **Character limit**: 200 characters (recommended: 80–150 for mobile readability)
- **Formula**: `[Brand] + [Primary Keyword] + [Key Feature] + [Size/Color/Variant]`
- **Rules**:
  - Capitalize first letter of each major word (title case)
  - No ALL CAPS
  - No promotional phrases ("Best Seller", "Sale", "#1")
  - No special characters: `! @ $ ? _ ~ { } # < > | * ; ^ ¬ ¦`
  - No subjective claims ("Amazing", "Perfect")
  - No seller name unless it's part of the brand
  - Numbers: use numerals (5, not five)

**Example formula in action:**
`Liforme Yoga Mat – Non-Slip Natural Rubber, 4.2mm, 185x68cm, Alignment Markers Included`

---

### Bullet Points
- **Count**: Exactly 5 bullets (Amazon displays up to 5 in the feature section)
- **Character limit**: 255 characters per bullet (keep under 200 for mobile)
- **Format rules**:
  - Start each bullet with ALL CAPS lead-in: `SUPERIOR GRIP —`
  - Then the benefit statement in sentence case
  - No periods at end of bullets
  - No promotional language
  - No shipping/seller info
  - Don't repeat the title verbatim
- **Ordering strategy**:
  1. Most compelling differentiator (USP)
  2. Primary use case / target customer
  3. Key technical spec translated to benefit
  4. Trust signal (warranty, certifications, tested)
  5. Compatibility or "works with" / size/fit guidance

---

### Product Description
- **Character limit**: 2,000 characters (plain text if no A+ content)
- **A+ Content** (Brand Registered sellers): Replaces the text description with rich modules.
  If user mentions A+ / Enhanced Brand Content, note they need to build it in Seller Central —
  but write the copy blocks for them.
- **Format**: Use HTML-safe line breaks (`<br>`) or basic `<b>` tags in Seller Central.
  Do not use Markdown — it won't render.
- **Strategy**: Tell a story. Open with customer pain → introduce product as solution →
  key features → trust close with guarantee or brand promise.

---

### Backend Search Terms (Keywords)
- **Limit**: 250 bytes total (each character = 1 byte; special chars may be 2)
- **Format**: Space-separated, no commas needed, no repeating words already in title
- **Rules**:
  - Lowercase preferred
  - No competitor brand names (TOS violation)
  - No "amazon", "best", "sale"
  - Include common misspellings, synonyms, plurals/singulars
  - Include Spanish/French terms if bilingual market applies
  - Do NOT repeat keywords that appear anywhere in the listing

---

### Amazon-Specific Banned Words
```
best, cheapest, guaranteed, number one, #1, top seller, on sale, deal of the day,
free shipping, gift wrap, authentic (unless verified), organic (unless certified USDA),
FDA approved (unless actually approved), clinical (without study citation)
```

---

### Amazon Ranking Factors (A9 Algorithm Signals)
1. **Sales velocity** — Conversions from clicks matter most
2. **Click-through rate** — Title + main image drive this
3. **Relevance** — Keyword match across title, bullets, description, backend
4. **Reviews / ratings** — Social proof affects conversion which feeds ranking
5. **Price competitiveness** — Amazon factors buy box price
6. **Fulfillment method** — FBA gets preferential treatment

---

## SHOPIFY

### Product Title
- **Recommended length**: 50–75 characters (for clean display in collections + Google Shopping)
- **Format**: Clear, natural language. No ALL CAPS. Lead with primary keyword.
- **SEO note**: Title becomes `<h1>` on the product page and populates Google Shopping feed.

---

### SEO Meta Title
- **Character limit**: 60–70 characters (Google truncates at ~60)
- **Format**: `[Primary Keyword] | [Brand]` or `[Primary Keyword] – [Key Differentiator]`
- **Note**: Must differ from product title — this is what shows in Google SERPs.

### SEO Meta Description
- **Character limit**: 150–160 characters
- **Goal**: Click-through optimization, not keyword stuffing
- **Formula**: Pain point → solution → differentiator → implicit CTA
- **Example**: `Tired of slipping mid-pose? Liforme's alignment-marked mat grips even in hot
  yoga. Free shipping on orders over $50.`

---

### Product Description (Shopify)
- **Format**: Shopify uses a rich text editor — write in clean HTML or markdown-ish structure.
  Use `<h2>` for section headers, `<ul>/<li>` for bullet lists, `<p>` for paragraphs.
- **Length**: 200–400 words is ideal for SEO
- **Structure**:
  1. Hook paragraph (2–3 sentences, primary keyword in first sentence)
  2. Feature/benefit bullets (use `<ul>`)
  3. Who it's for / use case section
  4. Trust/guarantee section
  5. Optional: FAQ-style objection handling
- **Image alt text**: Remind user to fill in alt text for all product images using natural-
  language keyword descriptions, not just the filename.

---

### Shopify SEO Tips
- **URL/handle**: Shopify auto-generates from title, but the user can edit it. Recommend:
  `/products/non-slip-yoga-mat` not `/products/yoga-mat-183cm-nr-v2-blue`
- **Collections**: Products rank in part by being in well-named, keyword-rich collections.
  Suggest collection naming to user if relevant.
- **Structured data**: Shopify's default themes output Product schema markup automatically.
  Confirm the theme does this if user asks about rich snippets.

---

## ETSY

### Listing Title
- **Character limit**: 140 characters
- **Strategy**: Front-load the most important keywords. Etsy's search reads left-to-right
  and weights earlier words more.
- **Format**: Use commas to separate keyword phrases (Etsy's algorithm reads comma-separated
  phrases as distinct units)
- **Example**: `Non Slip Yoga Mat, Thick Cork Yoga Mat, Eco Friendly Exercise Mat, Pilates Mat`
- **Avoid**: Repeating the same keyword more than twice (diminishing returns)

---

### Etsy Tags (13 tags)
- **Count**: Exactly 13 tags — always use all 13
- **Character limit**: 20 characters per tag
- **Strategy**:
  - Mix single-word and multi-word phrase tags
  - Use long-tail buyer-intent phrases: "yoga mat for beginners" > "yoga mat"
  - Include gift occasion tags if applicable: "yoga gift for her", "birthday gift"
  - Include material/style tags: "cork yoga mat", "natural rubber mat"
  - Include use case tags: "hot yoga mat", "travel yoga mat"
  - Do NOT repeat title keywords verbatim — tags + title together form your keyword universe

---

### Etsy Description
- **Character limit**: 13,000 characters (first 160 show in search previews)
- **First 160 characters**: Treat like a meta description — hook + primary keyword
- **Format**: Plain text, line breaks render. No HTML.
- **Structure**:
  1. Keyword-rich opener (160 chars — what it is, who it's for)
  2. Features + benefits (bullets using dashes or arrows)
  3. Materials + dimensions (Etsy shoppers care about craft/materials)
  4. Personalization options (if applicable)
  5. Care instructions
  6. Shop policies teaser (shipping times, returns)

---

### Etsy Ranking Factors (Etsy Search Algorithm)
1. **Relevance**: Title + tags keyword match
2. **Listing quality score**: Conversion rate and favorites
3. **Recency**: New listings get a temporary boost — renewing helps
4. **Shipping price**: Free shipping preferred; Etsy's free shipping guarantee badge
5. **Shop score**: Reviews, dispatch times, response rate
6. **Customer + market experience score (CMES)**: Review average + recent reviews

---

## EBAY

### Item Title
- **Character limit**: 80 characters
- **Strategy**: Lead with the most-searched keywords. eBay Cassini algorithm weights title heavily.
- **Format**: No promotional text. Include: Brand + Model + Key Spec + Condition (if used)
- **Example**: `Sony WH-1000XM5 Wireless Noise Cancelling Headphones Black — Open Box`

---

### Item Description (eBay)
- **Format**: eBay supports HTML. Use clean HTML with inline styles (no external CSS).
- **Key sections**:
  - What's in the box
  - Key specifications (table format recommended)
  - Condition notes (especially for used items)
  - Compatibility (if applicable)
  - Seller policies (returns, combined shipping)
- **Mobile**: Over 60% of eBay purchases are on mobile. Keep HTML simple and stacked, not
  multi-column.

---

### Item Specifics (eBay)
- Fill out ALL available item specifics — eBay confirms these directly boost Cassini ranking.
- Include: Brand, MPN, Color, Size, Material, Compatible Models, Type, Style
- Do not leave optional fields blank if you have the information.

---

### eBay Cassini Ranking Factors
1. **Relevance to search query** — Title keyword match
2. **Seller performance** — Positive feedback %, dispatch time
3. **Price + shipping** — Competitive pricing, free shipping preferred
4. **Item specifics completeness** — More = better ranking
5. **Return policy** — 30-day free returns get a ranking boost
6. **Listing quality** — Views, watchers, conversion rate

---

## GENERAL PRINCIPLES (all platforms)

### Image Alt Text Template
For Shopify and Etsy, always suggest alt text for images using this pattern:
`[Color] [Material] [Product Type] [Key Feature] – [Brand Name]`
Example: `Black Natural Rubber Non-Slip Yoga Mat with Alignment Lines – Liforme`

### Mobile Optimization
- Assume 60–70% of shoppers are on mobile
- Titles should be readable in ~40 characters before truncation
- First bullet point / first 160 chars of description must stand alone as a complete pitch
- Avoid walls of text — break into short paragraphs and bullets

### Conversion Trust Signals (use at least one)
- Money-back guarantee language: "Try it for 30 days — return it if you're not in love"
- Volume social proof: "Trusted by 15,000+ customers"
- Certification: "OEKO-TEX certified", "Cruelty-free", "FSC-certified"
- Awards/Press: "As featured in Yoga Journal"
- Specificity as proof: "Tested to 10,000 rolls without delamination"
