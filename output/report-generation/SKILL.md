---
name: report-generation
description: >
  Master audit report compilation. Activates when compiling final audit
  report, creating deliverables, producing action plans, building roadmaps,
  or summarizing audit findings.
---

# Master Audit Report Structure

## Required Sections
1. Executive Summary (3-5 paragraphs)
2. Overall Site Health Score: X/100
   - Technical: X/100, On-Page: X/100, Content: X/100
   - Local SEO: X/100, Authority: X/100, AI Visibility: X/100
   - UX/CRO: X/100, Reputation: X/100
3. **Proprietary Framework Scores**
   - LOCAL-IMPACT Score: X/100 (Grade) — 60-item local presence assessment
   - SERP-TRUST Score: X/100 (Grade) — 50-item search trust assessment
   - SEO Health Index: X/100 — Combined weighted score
   - Dimension breakdowns for both frameworks
   - Veto check results
4. Critical Issues — Fix Immediately
5. Priority Matrix (Impact × Effort quadrant)
6. Quick Wins — Implement Today
7. 30-Day Action Plan (weekly breakdown)
8. 90-Day Strategic Plan (monthly focus areas)
9. 6-Month Roadmap
10. 12-Month Vision
11. KPI Tracking Framework
12. Resource & Budget Recommendations
13. Competitor Summary (including framework score comparisons)
14. Full Phase-by-Phase Details

## Scoring Framework Integration

After all audit phases complete, run both proprietary scoring frameworks:

1. **LOCAL-IMPACT** (`/score-local-impact`) — Scores local presence across 8 dimensions (60 items)
2. **SERP-TRUST** (`/score-serp-trust`) — Scores search trust across 5 dimensions (50 items)
3. **SEO Health Index** — Combined: `(LOCAL-IMPACT × 0.55) + (SERP-TRUST × 0.45)`

Load scoring data from:
- `audit/local-impact-scores.md`
- `audit/serp-trust-scores.md`
- `references/scoring-methodology.md`

Include in the report:
- Framework score gauges (SVG circular charts)
- Dimension breakdown bar charts
- Veto check status indicators
- Competitor framework score comparison table
- Score improvement projections (30/90/180 day targets)

## PDF Report Export

After compiling the master report in the conversation, offer the user a
professionally designed PDF version:

- Use `/generate-pdf` to create a visually stunning PDF with SVG gauge charts,
  color-coded issue cards, CSS bar charts, timeline roadmaps, and professional tables.
- Use `/export-html` if the user wants to customize the report before converting.
- The PDF is generated using headless Chrome (zero dependencies) and saved to `reports/`.

Always ask: "Would you like me to generate a professional PDF report with visual
charts and scoring dashboards?"
