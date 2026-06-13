# Scraper Framework

## Method choice

Use official API or export first if available.
Use static HTML requests when data appears in page source.
Use Playwright when content is rendered by JavaScript or requires interaction.
Use browser extensions/no-code tools for one-off extraction.

## Ethical rules

Respect robots.txt and terms. Do not scrape private data without authorization. Do not bypass CAPTCHAs, paywalls, login protections, or rate limits. Do not overload sites.

## Common extraction targets

- product listings
- tables
- directories
- public event listings
- prices for authorized monitoring
- blog metadata
- public documentation
- search results from owned/internal tools

## Reliability checklist

- stable selectors
- pagination support
- retries
- timeout
- rate limit
- user agent
- deduplication key
- logging
- CSV schema
- sample validation

## Data cleanup

Trim whitespace, normalize dates, convert prices to numbers, strip currency symbols, remove duplicate rows, validate required fields.
