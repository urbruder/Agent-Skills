---
name: csv-executive-summary
description: >
  Use this skill whenever a user uploads or pastes a CSV, spreadsheet export, or raw tabular data
  and wants to understand what matters, get a summary, find key insights, or produce an executive
  summary, brief, or report. Triggers include: "what does this data tell me", "summarize this CSV",
  "what are the key numbers", "give me the highlights", "analyze this data", "what should I tell
  my boss", "make sense of this", "top insights", "what's important here", "pull out the key
  metrics", "executive summary from this data". Also triggers when the user shares a data dump
  with no clear ask — assume they want the 5 things that matter. Use this skill even if the user
  doesn't say "executive summary" explicitly — if they hand you raw data and want meaning, this is
  the skill.
---

# CSV → Executive Summary

Turn a raw data dump into the 5 numbers (or insights) your boss actually wants.

## The Core Principle

Skip the spreadsheet. Skip the 47-column table. Skip the "interesting" observations that don't
drive decisions. Give the reader exactly what they need to act — no more, no less.

**Target output: 5 findings. Each one answerable in a sentence. Each one decision-relevant.**

---

## Step 1: Ingest & Understand the Data

### Read the file
```python
import pandas as pd

# For CSV
df = pd.read_csv('/mnt/user-data/uploads/file.csv')

# For Excel exports or TSV
df = pd.read_csv('/mnt/user-data/uploads/file.tsv', sep='\t')
# or
df = pd.read_excel('/mnt/user-data/uploads/file.xlsx')

# Always start here
print(df.shape)          # How big is this thing?
print(df.dtypes)         # What kinds of columns?
print(df.head(3))        # What does a row look like?
print(df.describe())     # Basic stats across numeric columns
print(df.isnull().sum()) # Missing data situation
```

### Orient yourself fast
- **How many rows?** (10? 10k? 10M? — changes what's meaningful)
- **Time dimension?** (Is there a date column? This is often the most important thing.)
- **What is one row?** (One sale? One customer? One day? One event?)
- **What's the main numeric outcome?** (Revenue, quantity, score, count — find the "north star" column)

---

## Step 2: Find the 5 Things That Matter

Not every dataset has the same 5 things. Use this framework to find yours:

### The Finding Hierarchy (work top-down, stop when you have 5)

**Tier 1 — The headline number**
> What is the single most important aggregate? Total revenue, total users, average score, etc.
> Always lead with this. It orients everything else.

**Tier 2 — The trend**
> Is it going up or down? If there's a time column, compute period-over-period change.
> If no time column, skip this tier.

**Tier 3 — The biggest winner / biggest loser**
> Which segment, category, region, product, or person is #1? Which is last?
> Sort by the north-star metric and look at both ends.

**Tier 4 — The unexpected / the outlier**
> What is surprising? Something that breaks the pattern. An unusually high or low value.
> Use `.describe()` to find things 2+ standard deviations from the mean.
> Boxplots in your head: what's outside the whiskers?

**Tier 5 — The actionable gap or opportunity**
> What would change if someone acted on this data? A segment underperforming vs. average.
> A category with high volume but low margin. A time period that consistently underdelivers.

### Python patterns for finding each tier

```python
# Tier 1: Headline
total = df['revenue'].sum()
avg = df['score'].mean()

# Tier 2: Trend (if date column exists)
df['date'] = pd.to_datetime(df['date'])
df_monthly = df.groupby(df['date'].dt.to_period('M'))['revenue'].sum()
growth = (df_monthly.iloc[-1] - df_monthly.iloc[-2]) / df_monthly.iloc[-2] * 100

# Tier 3: Best/worst
top = df.groupby('category')['revenue'].sum().sort_values(ascending=False)
best = top.index[0], top.iloc[0]
worst = top.index[-1], top.iloc[-1]

# Tier 4: Outliers
mean = df['value'].mean()
std = df['value'].std()
outliers = df[df['value'] > mean + 2*std]

# Tier 5: Gaps (e.g., below-average segments)
segment_avg = df.groupby('region')['margin'].mean()
grand_avg = df['margin'].mean()
underperformers = segment_avg[segment_avg < grand_avg].sort_values()
```

---

## Step 3: Write the Executive Summary

### Format

```
EXECUTIVE SUMMARY
[One sentence: what is this data, and what time period / scope does it cover]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
THE 5 THINGS THAT MATTER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. [HEADLINE]
   [One sentence with the most important number. No qualifications.]

2. [TREND]
   [Direction + magnitude + timeframe. "Revenue grew 12% MoM in March."]

3. [BIGGEST WINNER / BIGGEST LOSER]
   [Name the best and worst performer. Be specific.]

4. [SURPRISE / OUTLIER]
   [The thing that breaks the pattern. Why it matters.]

5. [THE GAP / OPPORTUNITY]
   [What someone could do with this information.]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DATA NOTES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
• [Rows analyzed, date range, key column used]
• [Any data quality issues worth flagging — missing values, outliers excluded, etc.]
```

### Writing rules

- **No hedge words.** Not "it appears" or "it seems like." State findings as facts.
- **Numbers always have units.** Not "grew 12%" — "grew 12% ($240K → $269K)."
- **One sentence per finding.** If you need two sentences, you're explaining, not finding.
- **Active voice.** "Product A drove 60% of revenue" not "60% of revenue was driven by Product A."
- **Avoid percentages without anchors.** "Up 300%" means nothing if base is 1. Show both.

---

## Step 4: Calibrate by Audience

If the user gives you context about their audience, adjust accordingly:

| Audience | Emphasis | Tone |
|---|---|---|
| C-suite / board | Financial impact, strategic direction | Crisp, confident |
| Operations / managers | Process gaps, efficiency, action items | Specific, prescriptive |
| Sales / marketing | Pipeline, conversion, customer behavior | Upbeat, competitive |
| Technical / analysts | Methodology, data quality, edge cases | Precise, qualified |
| Investors | Growth, retention, unit economics | Forward-looking |

If no audience is specified, default to **"smart non-expert"** — someone who understands business
but didn't look at the raw data.

---

## Handling Edge Cases

### Data is too messy to analyze
Describe what you found before cleaning, then clean and proceed:
```python
# Flag obvious issues
print("Duplicates:", df.duplicated().sum())
print("Missing >50%:", df.columns[df.isnull().mean() > 0.5].tolist())
df_clean = df.dropna(subset=['revenue'])  # or however appropriate
```
Note in "DATA NOTES" what was excluded and why.

### Data has no date column
Skip Tier 2 (trend). Use a 4-finding structure and add a note: *"No time dimension — trend analysis unavailable."*

### Dataset is tiny (<50 rows)
Be honest about statistical significance. Findings are observations, not conclusions.
Add: *"Small sample — [N] rows. Treat as directional, not definitive."*

### Dataset is huge (>100K rows)
Sample intelligently for exploration, but compute summary stats on the full dataset:
```python
df_sample = df.sample(10000, random_state=42)  # For exploration
# But always report totals from full df, not sample
```

### All columns are categorical (no numeric north star)
Count distributions become the story. Find the most common, the rarest, and any surprising combos.

---

## Quality Checklist Before Delivering

- [ ] Does Finding #1 stand alone? (Could someone read only #1 and take action?)
- [ ] Are all numbers specific? (Amounts, not just percentages)
- [ ] Is every finding decision-relevant? (Would an exec care about this?)
- [ ] Is the "Data Notes" section honest about limitations?
- [ ] Did you avoid jargon the user didn't introduce?
- [ ] Is the whole summary under 250 words? (If not, cut.)

---

## Example Output

> **EXECUTIVE SUMMARY**
> Sales data for 12,847 transactions across 6 product lines, Jan–Mar 2024.
>
> **THE 5 THINGS THAT MATTER**
>
> 1. **HEADLINE — $3.2M total revenue, beating Q1 target by 8% ($240K above plan)**
>
> 2. **TREND — Revenue accelerated in March: up 22% vs. February ($1.4M → $1.7M)**
>
> 3. **WINNER/LOSER — "Pro Subscription" drove 61% of revenue ($1.95M); "Starter" contributed just 4% ($128K) despite being 31% of transactions**
>
> 4. **SURPRISE — Weekend transactions outperform weekdays by 34% per order ($87 vs. $65 avg), suggesting an untapped consumer segment**
>
> 5. **OPPORTUNITY — The West region is 18% below company average margin (42% vs. 51%). If brought to average, that's ~$190K in recovered margin**
>
> *Data notes: 12,847 rows, Jan 1–Mar 31 2024. 143 rows excluded (missing product code). Refunds not included in transaction totals.*
