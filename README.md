# GCC Job Scraper

Get current job listings from Bayt, Naukrigulf and GulfTalent across the six Gulf states in one run. Search by keyword, then narrow by city, monthly salary in US dollars or posting date. Each job flags likely duplicates posted on the other boards.

**[GCC Job Scraper on Apify →](https://apify.com/blackfalcondata/gcc-job-scraper?fpr=1h3gvi)**

---

## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.

## Key features

**Search with filters** — Search by keyword and location. Filter by 🌍 country, and more.

**Result cap** — Stop after N jobs (up to 100.000). Set to 0 for the full catalog.

**Export anywhere** — Download as JSON, CSV, or Excel. Stream via Apify API, webhooks, or integrations with Make, Zapier, Airbyte, Keboola.

**Structured data** — Every job returns the same schema with consistent field naming. All fields always present — `null` when unavailable, never omitted.

---

## Use cases

**Data pipeline automation**
Integrate with your ETL pipeline to collect structured jobs from the source on a schedule. Export to CSV, JSON, or directly to your database.

**Market research**
Monitor jobs, track trends, and analyze market dynamics with structured, deduplicated data from the source.

**Compensation benchmarking**
Aggregate salary ranges across roles, industries, and locations on the source to inform pricing decisions, hiring plans, or candidate negotiations.

**AI / LLM training data**
Structured JSON per job is ready for RAG pipelines, embeddings, and agent workflows.

---

## Quick start

```json
{
  "query": "accountant",
  "country": "AE",
  "maxResults": 100
}
```

---

## Input parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `query` | string | — | Words that must all appear in the job title, company or category, e.g. accountant or civil engineer. Leave empty for all jobs. |
| `country` | enum | — | One Gulf country. Leave empty for all six. |
| `maxResults` | integer | `100` | The most jobs to save. You pay per job saved, so this is also your spending cap for the run. |
| `city` | string | — | City name as the boards write it, e.g. Dubai, Riyadh or Doha. Leave empty for the whole country. |
| `postedWithinDays` | integer | — | Only jobs posted in the last N days (1-60). Leave empty for all current jobs. |
| `salaryMin` | integer | — | Only jobs whose stated salary reaches this many US dollars a month. Jobs without a stated salary are left out when this is set. |
| `excludeEmptyFields` | boolean | `false` | Drop fields that are empty for a job (no city, no salary, no likely duplicates) from its row. Off by default so every row has the same columns. |

---

## Output fields

Every job returns the same 15-field schema. Missing values are `null` — never omitted.

- `id`
- `board`
- `country`
- `title`
- `company`
- `location`
- `category`
- `industry`
- `postedAt`
- `url`
- `city`
- `salary`
- `summary`
- `salaryMonthlyUsd`
- `possibleDuplicates`

---

## Sample output

One object per job. Here is a real example from a production run:

```json
{
  "id": "naukrigulf-281026000025",
  "board": "naukrigulf",
  "country": "AE",
  "title": "Executive Accountant",
  "company": "Confidential Company",
  "location": "Ras Al Khaimah - United Arab Emirates (UAE)",
  "category": "Accounts / Taxation / Audit / Company Secretary",
  "industry": "Metals / Steel / Iron / Aluminium / Fabrication",
  "postedAt": "2026-10-28T04:58:23.000Z",
  "url": "https://www.naukrigulf.com/executive-accountant-jobs-in-ras-al-khaimah-uae-in-confidential-5-to-10-years-n-jid-281026000025",
  "city": "Ras Al Khaimah",
  "salary": "AED 4,100-5,500"
}
```

*Truncated — full records contain 15 fields. See Output fields for the complete schema.*

**[Try GCC Job Scraper now — $5 free credit, no credit card →](https://apify.com/blackfalcondata/gcc-job-scraper?fpr=1h3gvi)**

---

## Pricing

Pay only for what you extract. No subscription required — Apify's free $5 credit covers thousands of results.

| Event | Price (USD) |
| --- | --- |
| Job record | $0.0012 |

See the [actor on Apify](https://apify.com/blackfalcondata/gcc-job-scraper?fpr=1h3gvi) for current pricing.

---

## FAQ

**How much does it cost?**
Pay-per-event pricing — you only pay for ${NOUNS} extracted. Apify's free $5 credit is enough to run thousands of results before you pay anything.

**Do I need an API key or credentials?**
No. Just sign up for Apify, paste your input, and click Start. No credit card required.

---

## Related products by Black Falcon Data

[Browse all Black Falcon Data actors →](https://apify.com/blackfalcondata?fpr=1h3gvi)

---

## Getting started with Apify

New to Apify? [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=1h3gvi) — no credit card required.

1. Sign up — $5 platform credit included
2. Open [GCC Job Scraper](https://apify.com/blackfalcondata/gcc-job-scraper?fpr=1h3gvi) and configure your input
3. Click **Start** — export results as JSON, CSV, or Excel

Need more later? [See Apify pricing](https://apify.com/pricing?fpr=1h3gvi).

---

## About Black Falcon Data

Black Falcon Data builds production-grade web scrapers for job boards and marketplace data. Browse our full actor catalog at [www.blackfalcondata.com](https://www.blackfalcondata.com).

---

*Last updated: 2026 10*
