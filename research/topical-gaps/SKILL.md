---
name: topical-gaps
description: >
  Topical map and gap analysis. Activates when discussing topic gaps, topical
  maps, content clusters, topic coverage, semantic coverage, topical authority
  building, or content planning at the topical level.
  Phase 7. Output: {AUDIT_DIR}/topical-gaps.md
---

# Topical Gap Analysis — Phase 7

## Executive Summary

Topical authority is the #1 long-term competitive moat in local SEO. Google's Helpful Content System (integrated into core algorithm March 2024) rewards businesses that comprehensively cover a topic cluster vs. those that superficially mention many topics. The 25-article threshold signal: sites with 25+ articles in a cluster receive significantly stronger topical authority signals than sites with 10 or fewer (SEMrush 2024). AI Overviews (AIO) cite topically authoritative sources 2–3× more than shallow coverage sites. This phase maps the client's topical universe, identifies coverage gaps vs. top competitors, and produces a prioritized content roadmap.

**2025 topical authority benchmarks:**
- Pillar pages: minimum 2,500 words; competitive 4,000–6,000 words
- Cluster pages: minimum 1,200 words; competitive 1,800–2,500 words
- Content decay: > 20% YoY click decline = refresh required (GSC comparison)
- AIO topical citation: 58% AIO surge for businesses with full topic cluster coverage (Amsive early 2026)
- ChatGPT freshness factor: pages updated within 30 days cited at 76.4% rate

---

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — business name, services, location.
Read `{AUDIT_DIR}/content-inventory.md` — current content map.
Read `{AUDIT_DIR}/content-gaps.md` — identified topic and format gaps.
Read `{AUDIT_DIR}/keyword-gaps.md` — keyword opportunities.

**Tools for this phase:**
| Tool | Purpose | Cost |
|------|---------|------|
| **Ahrefs Topics Explorer** | Discover topic clusters and subtopics | Paid |
| **Ahrefs Content Gap** | Find topics competitors rank for that client doesn't | Paid |
| **SEMrush Topic Research** | Visual topic cluster mapping | Paid |
| **SEMrush Keyword Gap** | Competitor topical coverage comparison | Paid |
| **AlsoAsked.com** | PAA-based question mapping per topic | Freemium |
| **AnswerThePublic** | Visualize question clusters around topics | Freemium |
| **Google PAA boxes** | Live "People Also Ask" questions per pillar | Free |
| **Surfer SEO** | NLP-based content brief with entity coverage | Paid |
| **Google Search Console** | Which topics drive clicks (existing authority) | Free |

**2025 Topical Authority Context:**
Google's Helpful Content system (2024+) and AI Overviews reward demonstrable expertise across a topic cluster. Surface-level coverage of many topics is penalized; deep coverage of fewer topics ranks. The goal is topic clusters where every subtopic links to a pillar, and every pillar is internally linked from cluster pages.

**Content Depth Thresholds (2025 benchmarks):**
| Page Type | Minimum Words | Target Words | Internal Links |
|-----------|-------------|-------------|---------------|
| Pillar page | 2,500 | 4,000–6,000 | 5–15 cluster links out |
| Cluster page | 1,200 | 1,800–2,500 | 1 pillar link + 2–3 cluster links |
| Supporting page | 700 | 1,000–1,500 | 1 cluster or pillar link |
| FAQ entry | 150 | 250–400 | 1 relevant service link |

---

## Section 1: Complete Topical Universe Mapping

### Define the Core Topical Universe
For this business, list ALL possible topics that could be relevant:

**Level 1 — Main Topics (Pillars):**
The broadest topics the business should be authoritative on.
Example (for a plumber): Emergency Plumbing, Drain Services, Water Heaters, Pipe Repair, Bathroom Plumbing, Kitchen Plumbing, Outdoor Plumbing, Commercial Plumbing

**Level 2 — Subtopics (Clusters):**
Under each pillar, the key subtopics.
Example under "Water Heaters": Types of Water Heaters, Water Heater Installation, Water Heater Repair, Water Heater Replacement, Tankless vs. Tank, Cost Guide, Troubleshooting

**Level 3 — Supporting Topics:**
Specific questions, comparisons, how-tos under each subtopic.
Example under "Water Heater Installation": How long does it take, What's included, DIY vs. Professional, Building permits needed, Cost breakdown

---

## Section 2: Client vs. Ideal Topical Coverage

### Coverage Map

```
PILLAR: [Main Topic]
├── CLUSTER: [Subtopic]
│   ├── Supporting: [specific angle] → Client: ✅ EXISTS / ❌ MISSING / ⚠️ THIN
│   ├── Supporting: [specific angle] → Client: ✅ / ❌ / ⚠️
│   └── Supporting: [specific angle] → Client: ✅ / ❌ / ⚠️
├── CLUSTER: [Subtopic]
│   └── [...]
Status: Not Started | Partial (X/Y pages) | Complete
Priority: 1-5 | Relevance: H/M/L | Competition: H/M/L
```

Repeat for each of the main service topic pillars.

---

## Section 3: Cluster Completeness Analysis

For each content cluster, score completeness:

| Cluster | Total Subtopics | Client Coverage | % Complete | Competitor Leader % | Priority |
|---------|---------------|----------------|-----------|--------------------|---------|
| [cluster] | [X] | [Y pages] | [X%] | [comp name X%] | H/M/L |

**Pillar Page Assessment:**
- Does a strong pillar page exist for each main topic?
- Pillar page quality: comprehensive? 2,000+ words? All subtopics linked?
- Cluster pages linked back to pillar?
- Pillar page receiving adequate internal links?

---

## Section 4: Semantic Coverage Analysis

### Missing Entities
Key entities that should appear in topic coverage but don't:
- [Entity type]: [specific entity missing and why it matters]

### Missing Concepts
Important concepts/terminology not covered:
- [concept]: [pages where it should appear but doesn't]

### Missing Questions (PAA Analysis)
For each main topic pillar, check PAA boxes and identify unanswered questions:
| Question | PAA Source | Client Answers This? | Content Needed |
|---------|-----------|---------------------|---------------|
| [question] | [Google PAA] | No | [blog post / FAQ entry] |

### Synonym and Variation Coverage
- Are common synonyms for services covered?
  Example: "water heater" vs. "hot water heater" vs. "boiler"
- Industry jargon vs. customer language — both covered?
- Regional naming variants (if applicable)?

---

## Section 5: Topical Authority Gap vs. Competitors

For each major topic, how does topical authority compare?

| Topic | Client Pages | Comp 1 Pages | Comp 2 Pages | Gap | Priority |
|-------|------------|------------|------------|-----|---------|
| [main service] | [X] | [Y] | [Z] | [+/-X] | H/M/L |
| [subtopic] | [X] | [Y] | [Z] | [+/-X] | H/M/L |

**Topical Dominance Opportunities:**
Which topics could this business fully dominate that competitors partially cover?
- [topic]: Client has [X] pages, competitors have [1-2 thin pages] → opportunity to dominate

---

## Section 6: AI Visibility Topical Gaps

AI Overviews and AI assistants increasingly look for topical depth. Gaps in topic coverage = missing from AI recommendations.

**AI Coverage Test:**
For each main topic pillar, ask: "If I asked ChatGPT/Gemini for comprehensive info on [topic] in [city], would this business's content support being cited?"

Identify which pillars need more depth for AI citation:
| Pillar | AI-Citable Content? | What's Needed |
|--------|-------------------|--------------|
| [topic] | No | [specific content types] |

---

## Section 7: Prioritized Topical Content Roadmap

### Priority Matrix (Impact × Feasibility)

| Gap Type | Impact (1–5) | Feasibility (1–5) | Priority Score | Effort Estimate |
|----------|-------------|-------------------|----------------|----------------|
| Missing pillar page (competitor has 3,000+ word guide, client has nothing) | 5 | 3 | 15 | 8–12 hrs |
| Missing cluster page (all competitors rank, client absent) | 4 | 4 | 16 | 3–5 hrs |
| Thin pillar page (<1,500 words) — expand to 3,000+ | 4 | 4 | 16 | 4–6 hrs |
| Missing FAQ / PAA answers | 3 | 5 | 15 | 1–2 hrs |
| Orphaned cluster pages (exist but not linked to pillar) | 4 | 5 | 20 | 30 min |
| Missing AI-citable data/statistics page | 4 | 3 | 12 | 4–6 hrs |
| Missing location × service intersection page | 3 | 4 | 12 | 2–4 hrs |

### Immediate Priority (Next 30 Days)
1. **Fix orphaned cluster pages** — add `<a href="/[pillar-url]">` internal link from every cluster page to its parent pillar. Also add cluster link from pillar. Effort: 30 min each. Priority: 20 (4×5). Expected: direct PageRank flow improvement.
2. **Create/upgrade pillar pages to 3,000+** words — For top 2 service clusters with missing or thin pillars: build comprehensive pillar pages using Surfer SEO (target score ≥80) + Clearscope (target A-). Include: all subtopics, 5+ FAQs, HowTo schema, unique local data/statistics. Effort: 8–12 hrs each.
3. **Fill "red" cluster gaps** — Clusters where ALL competitors have pages but client doesn't: create 1,500+ word cluster pages, link to pillar immediately after publish. Effort: 3–5 hrs each.
4. **Answer top 10 PAA questions** — Use AlsoAsked.com for each pillar topic → extract top 10 PAA questions → add as FAQ entries on relevant service pages + FAQPage schema. Effort: 1–2 hrs. Expected: AIO citation + PAA box wins.
5. **Add FAQPage schema to ALL cluster pages** — AIO cites pages with FAQPage at 3.2× rate. Add 5 FAQ minimum per page. Effort: 30 min/page. Priority: 20.

### Numbered Action Steps (Comprehensive)
| Step | Action | Effort | Priority | Expected Impact |
|------|--------|--------|---------|----------------|
| 1 | Fix orphaned cluster links (pillar ↔ cluster) | 30 min/page | 20 | PageRank distribution |
| 2 | Expand thin pillar to 3,000+ words + Surfer ≥80 | 8–12 hrs each | 15 | Rankings lift + AIO |
| 3 | Create missing cluster pages (red gaps) | 3–5 hrs each | 16 | New keyword rankings |
| 4 | Add PAA-based FAQ content + FAQPage schema | 1–2 hrs | 15 | AIO + PAA boxes |
| 5 | Refresh content decay pages (>20% YoY) | 2–4 hrs each | 16 | Traffic recovery |
| 6 | Build original data/statistics page per pillar | 8–16 hrs | 12 | AI citation priority |
| 7 | Create location × service intersection pages | 2–4 hrs each | 12 | Local long-tail rankings |
| 8 | Monitor Google Trends weekly for emerging topics | 30 min/week | 10 | First-mover advantage |

### Medium-Term (Days 31–90)
1. Build out secondary clusters topic-by-topic using Ahrefs Content Gap data
2. Create supporting topic content for each established cluster
3. Publish FAQ hub pages for each pillar with schema markup (FAQPage + HowTo)
4. Build original data/statistics pages — survey customers, create localized studies

### Long-Term (Months 3–6)
1. Complete coverage of all topic pillars to topical authority status
2. Build seasonal sub-clusters (holiday, weather-related, emergency services)
3. Create emerging topic content before competitors (monitor Google Trends + AlsoAsked weekly)
4. Commission original research/case studies per pillar — primary data = AI citation priority

---

## Deliverable: Complete Topical Map

```
TOPICAL AUTHORITY MAP — [Business Name]
Generated: [Date]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PILLAR 1: [Main Service/Topic]
├── CLUSTER: [Subtopic]
│   ├── ✅ [Existing page URL] — [title]
│   ├── ❌ MISSING: [page idea] — Priority: High | Est. Traffic: [X/mo]
│   └── ⚠️ THIN: [existing URL] — needs expansion
├── CLUSTER: [Subtopic]
│   └── [...]
Overall Status: [X]% complete
Gap vs. Leader: [X] pages needed to match [competitor]

PILLAR 2: [Main Service/Topic]
[...]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TOPICAL COVERAGE SCORE: [X]%
Pages needed to reach 80% coverage: [X] pages
Estimated time to topical authority: [X months]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Output

Write complete topical map and gap analysis to `{AUDIT_DIR}/topical-gaps.md` with YAML frontmatter. Write HTML report to `{REPORTS_DIR}/phase-7-topical-gaps.html` and convert to PDF via `python3 scripts/generate_pdf.py`.

```yaml
---
skill: research/topical-gaps
phase: 7
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
status: complete
topical_coverage_pct: [X%]
pillars_mapped: [X]
gaps_identified: [X]
---
```

**Key consumers:**
- `strategy/topical-authority` — uses map for authority building strategy
- `research/keyword-gaps` — maps keyword data onto topical gaps
- `output/report-generation` — topical coverage % in master report section 7
