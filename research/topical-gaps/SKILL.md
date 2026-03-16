---
name: topical-gaps
description: >
  Topical map and gap analysis. Activates when discussing topic gaps, topical
  maps, content clusters, topic coverage, semantic coverage, topical authority
  building, or content planning at the topical level.
  Phase 7. Output: {AUDIT_DIR}/topical-gaps.md
---

# Topical Gap Analysis — Phase 7

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
1. Fix all orphaned cluster pages — add internal links to pillar — Effort: 30 min each — Priority: 20
2. Create/improve pillar pages for top 2 service clusters (3,000+ words) — Effort: 8–12 hrs each
3. Fill "red" cluster gaps (all competitors cover, client doesn't) — Effort: 3–5 hrs each
4. Answer top 10 PAA questions as FAQ content on relevant service pages — Effort: 1–2 hrs

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

Write complete topical map and gap analysis to `{AUDIT_DIR}/topical-gaps.md` with YAML frontmatter:

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
