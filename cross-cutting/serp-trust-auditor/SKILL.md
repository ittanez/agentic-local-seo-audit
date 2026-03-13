---
name: serp-trust-auditor
description: Score a website using the proprietary 50-item SERP-TRUST framework
triggers:
  - score serp trust
  - serp trust audit
  - serp trust score
  - run serp trust
  - site trust score
---

# SERP-TRUST Auditor

You are executing the proprietary SERP-TRUST scoring framework — a 50-item assessment of search engine trust signals and authority.

## Prerequisites

Before scoring, confirm you have:
- [ ] Website URL (must be accessible)
- [ ] Target keywords (minimum 5)
- [ ] At least 3 competitor URLs for comparison
- [ ] Target location(s) for local context

If any are missing, collect them before proceeding.

## Framework Reference

Load the complete scoring rubric from `references/serp-trust-benchmark.md` (also available at `../../references/serp-trust-benchmark.md`).

**Framework:** SERP-TRUST (Search Engine Results Page — Technical Reliability, User Signals & Search Trust)
**Items:** 50 | **Scale:** 0-4 per item | **Max Raw:** 200 | **Normalized:** 0-100

## Scoring Dimensions

| Code | Dimension | Items | Max |
|------|-----------|-------|-----|
| T | Technical Foundation | 10 | 40 |
| R | Ranking Signals | 10 | 40 |
| U | User Experience & Performance | 10 | 40 |
| S | Search Authority | 10 | 40 |
| T2 | Trust & AI Readiness | 10 | 40 |

## Execution Process

### Step 1: Research Phase

For each dimension, gather evidence:

**Technical Foundation (T):** Fetch robots.txt, check sitemap, inspect SSL, test canonical tags, check structured data, assess mobile rendering, analyze URL structure.

**Ranking Signals (R):** Inspect title tags, meta descriptions, header hierarchy, content depth, internal linking patterns, image optimization, E-E-A-T signals, content freshness, keyword targeting.

**User Experience (U):** Check Core Web Vitals (LCP, INP, CLS), TTFB, page weight, navigation UX, mobile usability, accessibility, conversion paths, engagement indicators.

**Search Authority (S):** Assess referring domains, link quality, anchor text distribution, citations, topical authority, brand mentions, digital PR presence, competitor link gap, toxic links.

**Trust & AI Readiness (T2):** Search for business in AI Overviews, ChatGPT, Perplexity, Gemini. Check content citeability, entity recognition, schema completeness, brand SERP, review trust, content authenticity, cross-platform consistency.

### Step 2: Score Each Item

For each of the 50 items, assign a score of 0-4 using the rubric:

| Score | Label | Meaning |
|-------|-------|---------|
| 0 | Critical | Broken, missing, or actively harmful |
| 1 | Poor | Exists but significantly below standards |
| 2 | Fair | Partially implemented, notable gaps |
| 3 | Good | Correctly implemented, minor improvements possible |
| 4 | Excellent | Best-in-class, competitive advantage |

Record evidence for each score.

### Step 3: Veto Check

Check all 7 veto conditions:

| Veto | Condition | Score Cap |
|------|-----------|-----------|
| V01 | Site not indexed by Google | 10 |
| V02 | Active manual penalty in GSC | 15 |
| V03 | No HTTPS / expired SSL | 25 |
| V04 | LCP > 6s on mobile | 30 |
| V05 | Cloaked / hidden content served | 10 |
| V06 | >50% toxic backlinks | 20 |
| V07 | Zero structured data | 40 |

### Step 4: Calculate Final Score

```
Raw Score = Sum of all 50 item scores
Normalized = (Raw / 200) × 100
Final = min(Normalized, lowest triggered veto cap)
```

Optional weighted scoring:
```
Weighted = (T_pct × 0.20) + (R_pct × 0.25) + (U_pct × 0.20) + (S_pct × 0.20) + (T2_pct × 0.15)
```

### Step 5: Score Competitors

Score each competitor on the same 50 items (abbreviated assessment acceptable — focus on observable signals and key dimensions).

## Output Format

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 SERP-TRUST SCORECARD
 Website: [URL]
 Date: [Date]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

 OVERALL SCORE: [X] / 100    Grade: [A+-F]

 Dimension Breakdown:
 T  Technical Foundation   [XX/40]  ████████░░  [X%]
 R  Ranking Signals        [XX/40]  ███████░░░  [X%]
 U  User Experience        [XX/40]  █████░░░░░  [X%]
 S  Search Authority       [XX/40]  ████████░░  [X%]
 T2 Trust & AI Readiness   [XX/40]  ██████░░░░  [X%]

 Veto Checks:
 [✅/❌] V01: Site Indexed
 [✅/❌] V02: No Manual Penalty
 [✅/❌] V03: HTTPS Active
 [✅/❌] V04: LCP < 6s
 [✅/❌] V05: No Cloaking
 [✅/❌] V06: Toxic Links < 50%
 [✅/❌] V07: Has Structured Data

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 COMPETITOR COMPARISON
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 | Metric     | Client | Comp 1 | Comp 2 | Comp 3 |
 |------------|--------|--------|--------|--------|
 | Overall    |   XX   |   XX   |   XX   |   XX   |
 | Technical  |   XX   |   XX   |   XX   |   XX   |
 | Ranking    |   XX   |   XX   |   XX   |   XX   |
 | UX/Perf    |   XX   |   XX   |   XX   |   XX   |
 | Authority  |   XX   |   XX   |   XX   |   XX   |
 | AI Ready   |   XX   |   XX   |   XX   |   XX   |
 | Position   |  X/4   |  X/4   |  X/4   |  X/4   |

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 TOP 5 IMPROVEMENT PRIORITIES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 1. [Item ID]: [Description] — Current: X/4, Impact: [High/Med]
 2. [Item ID]: [Description] — Current: X/4, Impact: [High/Med]
 3. [Item ID]: [Description] — Current: X/4, Impact: [High/Med]
 4. [Item ID]: [Description] — Current: X/4, Impact: [High/Med]
 5. [Item ID]: [Description] — Current: X/4, Impact: [High/Med]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 QUICK WINS (Items scoreable to 3+ with <1hr effort)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 • [Item]: [What to do] — Expected gain: +X points
 • [Item]: [What to do] — Expected gain: +X points
 • [Item]: [What to do] — Expected gain: +X points
```

## SEO Health Index (Combined Score)

If LOCAL-IMPACT has also been scored, compute the combined index:

```
SEO Health Index = (LOCAL-IMPACT Score × 0.55) + (SERP-TRUST Score × 0.45)
```

Report this as the master metric in the final output.

## Handoff

After scoring, save results to `audit/serp-trust-scores.md` for use by:
- `output/report-generation` — integrates into master report
- `output/pdf-report` — renders score dashboard in PDF
- `cross-cutting/local-impact-auditor` — combines for SEO Health Index

## Data Output for Report Integration

Write a structured data block that other skills can consume:

```yaml
framework: SERP-TRUST
version: 1.0
date: [YYYY-MM-DD]
business: [name]
url: [url]
scores:
  overall: [0-100]
  grade: [A+-F]
  weighted: [0-100]
  dimensions:
    T: { raw: X, max: 40, pct: X }
    R: { raw: X, max: 40, pct: X }
    U: { raw: X, max: 40, pct: X }
    S: { raw: X, max: 40, pct: X }
    T2: { raw: X, max: 40, pct: X }
  vetoes_triggered: []
  competitors:
    - name: [comp1]
      url: [url]
      score: X
    - name: [comp2]
      url: [url]
      score: X
    - name: [comp3]
      url: [url]
      score: X
  seo_health_index: [0-100]  # only if LOCAL-IMPACT also scored
```
