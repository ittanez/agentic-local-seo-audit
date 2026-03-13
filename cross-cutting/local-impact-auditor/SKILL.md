---
name: local-impact-auditor
description: Score a local business using the proprietary 60-item LOCAL-IMPACT framework
triggers:
  - score local impact
  - local impact audit
  - local impact score
  - run local impact
  - local presence score
---

# LOCAL-IMPACT Auditor

You are executing the proprietary LOCAL-IMPACT scoring framework — a 60-item assessment of local business presence and visibility.

## Prerequisites

Before scoring, confirm you have:
- [ ] Business name and website URL
- [ ] Google Business Profile URL (or ability to search for it)
- [ ] At least 3 competitor names/URLs for comparison
- [ ] Target location(s)

If any are missing, collect them before proceeding.

## Framework Reference

Load the complete scoring rubric from `references/local-impact-benchmark.md` (also available at `../../references/local-impact-benchmark.md`).

**Framework:** LOCAL-IMPACT (Local Optimization, Consistency, Authority & Listing — Impact Performance Assessment & Competitive Tracking)
**Items:** 60 | **Scale:** 0-3 per item | **Max Raw:** 180 | **Normalized:** 0-100

## Scoring Dimensions

| Code | Dimension | Items | Max |
|------|-----------|-------|-----|
| L | Listing Quality | 10 | 30 |
| O | Online Reviews | 10 | 30 |
| C | Citation Consistency | 10 | 30 |
| A | Authority Signals | 10 | 30 |
| L2 | Local Content | 5 | 15 |
| I | Integrated Visibility | 5 | 15 |
| P | Performance | 5 | 15 |
| T | Tracking | 5 | 15 |

## Execution Process

### Step 1: Research Phase

For each dimension, gather evidence using available tools:

**Listing Quality (L):** Fetch GBP listing, check completeness of categories, photos, posts, Q&A, services, hours, attributes.

**Online Reviews (O):** Check Google review count, rating, velocity, response rate. Search for reviews on Yelp, Facebook, industry sites.

**Citation Consistency (C):** Search for business NAP across major directories. Check consistency of name, address, phone formatting.

**Authority Signals (A):** Check for local backlinks, Chamber of Commerce, BBB, industry associations. Assess domain signals.

**Local Content (L2):** Review location pages, neighborhood content, local blog posts, community involvement content.

**Integrated Visibility (I):** Check social media presence, Apple Maps, Bing Places, voice search readiness, AI platform mentions.

**Performance (P):** Check page speed, mobile usability, Core Web Vitals where observable.

**Tracking (T):** Check for GA4, GSC setup, call tracking, conversion tracking presence.

### Step 2: Score Each Item

For each of the 60 items, assign a score of 0-3 using the rubric:

| Score | Label | Meaning |
|-------|-------|---------|
| 0 | Absent | Not implemented at all |
| 1 | Weak | Partially implemented with significant gaps |
| 2 | Good | Implemented correctly with minor improvements needed |
| 3 | Excellent | Fully optimized, best-in-class implementation |

Record evidence for each score.

### Step 3: Veto Check

Check all 6 veto conditions:

| Veto | Condition | Score Cap |
|------|-----------|-----------|
| V01 | GBP not claimed or verified | 15 |
| V02 | Website not indexed by Google | 10 |
| V03 | Active Google penalty | 10 |
| V04 | NAP wrong on website + GBP + majority of citations | 20 |
| V05 | Zero Google reviews | 25 |
| V06 | No SSL certificate | 20 |

### Step 4: Calculate Final Score

```
Raw Score = Sum of all 60 item scores
Normalized = (Raw / 180) × 100
Final = min(Normalized, lowest triggered veto cap)
```

### Step 5: Score Competitors

Score each competitor on the same 60 items (abbreviated assessment is acceptable — focus on observable signals and key dimensions).

## Output Format

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 LOCAL-IMPACT SCORECARD
 Business: [Name]
 Date: [Date]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

 OVERALL SCORE: [X] / 100    Grade: [A-F]

 Dimension Breakdown:
 L  Listing Quality      [XX/30]  ████████░░  [X%]
 O  Online Reviews        [XX/30]  ███████░░░  [X%]
 C  Citation Consistency  [XX/30]  █████░░░░░  [X%]
 A  Authority Signals     [XX/30]  ████████░░  [X%]
 L2 Local Content         [XX/15]  ██████░░░░  [X%]
 I  Integrated Visibility [XX/15]  ███████░░░  [X%]
 P  Performance           [XX/15]  ████████░░  [X%]
 T  Tracking              [XX/15]  █████░░░░░  [X%]

 Veto Checks:
 [✅/❌] V01: GBP Claimed
 [✅/❌] V02: Site Indexed
 [✅/❌] V03: No Penalty
 [✅/❌] V04: NAP Correct
 [✅/❌] V05: Has Reviews
 [✅/❌] V06: SSL Active

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 COMPETITOR COMPARISON
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 | Metric    | Client | Comp 1 | Comp 2 | Comp 3 |
 |-----------|--------|--------|--------|--------|
 | Overall   |   XX   |   XX   |   XX   |   XX   |
 | Listing   |   XX   |   XX   |   XX   |   XX   |
 | Reviews   |   XX   |   XX   |   XX   |   XX   |
 | Citations |   XX   |   XX   |   XX   |   XX   |
 | Authority |   XX   |   XX   |   XX   |   XX   |
 | Position  |  X/4   |  X/4   |  X/4   |  X/4   |

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 TOP 5 IMPROVEMENT PRIORITIES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 1. [Item ID]: [Description] — Current: X/3, Impact: [High/Med]
 2. [Item ID]: [Description] — Current: X/3, Impact: [High/Med]
 3. [Item ID]: [Description] — Current: X/3, Impact: [High/Med]
 4. [Item ID]: [Description] — Current: X/3, Impact: [High/Med]
 5. [Item ID]: [Description] — Current: X/3, Impact: [High/Med]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 QUICK WINS (Items scoreable to 3 with <1hr effort)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 • [Item]: [What to do] — Expected gain: +X points
 • [Item]: [What to do] — Expected gain: +X points
 • [Item]: [What to do] — Expected gain: +X points
```

## Handoff

After scoring, save results to `audit/local-impact-scores.md` for use by:
- `output/report-generation` — integrates into master report
- `output/pdf-report` — renders score dashboard in PDF
- `cross-cutting/serp-trust-auditor` — combines for SEO Health Index

## Data Output for Report Integration

Write a structured data block that other skills can consume:

```yaml
framework: LOCAL-IMPACT
version: 1.0
date: [YYYY-MM-DD]
business: [name]
scores:
  overall: [0-100]
  grade: [A+-F]
  dimensions:
    L: { raw: X, max: 30, pct: X }
    O: { raw: X, max: 30, pct: X }
    C: { raw: X, max: 30, pct: X }
    A: { raw: X, max: 30, pct: X }
    L2: { raw: X, max: 15, pct: X }
    I: { raw: X, max: 15, pct: X }
    P: { raw: X, max: 15, pct: X }
    T: { raw: X, max: 15, pct: X }
  vetoes_triggered: []
  competitors:
    - name: [comp1]
      score: X
    - name: [comp2]
      score: X
    - name: [comp3]
      score: X
```
