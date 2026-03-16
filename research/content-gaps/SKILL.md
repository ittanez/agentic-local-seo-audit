---
name: content-gaps
description: >
  Content gap analysis — identifies missing content opportunities vs. competitors.
  Activates when discussing content gaps, missing topics, content opportunities,
  competitor content comparison, golden opportunities, AI Overview gaps, or
  content strategy planning. Phase 5. Output: {AUDIT_DIR}/content-gaps.md
---

# Content Gap Analysis — Phase 5

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — business name, services, location, goals.
Read `{AUDIT_DIR}/content-inventory.md` — what client currently has (page list + word counts).
Read `{AUDIT_DIR}/competitor-profiles.md` — competitor content strategies and page counts.

**Tools for this phase:**
| Tool | Purpose | Cost |
|------|---------|------|
| **Ahrefs Content Gap** | Shows keywords competitors rank for that client doesn't — by topic cluster | Paid |
| **SEMrush Keyword Gap** | Side-by-side keyword comparison with traffic estimates | Paid |
| **BuzzSumo** | Identify top-performing competitor content by shares and backlinks | Paid |
| **AlsoAsked.com** | PAA-based question mapping — identify unanswered questions per topic | Freemium |
| **AnswerThePublic** | Visualize question clusters around service topics | Freemium |
| **Google PAA boxes** | Live "People Also Ask" questions — free, real-time | Free |
| **Google Search** | Manual SERP analysis per topic — identify AIO presence | Free |
| **Google Search Console** | Which queries get impressions but poor CTR — existing gap opportunities | Free |

**2025 Content Gap Context:**
- AI Overviews (AIO) now appear for ~20–35% of local service queries — content gaps aren't just "not ranking" but "not cited by AI"
- FAQPage schema + direct standalone answers = primary AIO citation trigger → each identified gap should consider AIO optimization
- Google's Helpful Content System penalizes thin coverage of many topics — better to dominate 3 clusters than lightly cover 10

---

## Section 1: Topic Gaps vs. Competitors

Use **Ahrefs Content Gap** (enter client vs. top 3 competitors):

### Table-Stakes Gaps (All Competitors Cover, Client Doesn't)
Topics all top competitors rank for = table stakes. Missing these = immediate priority:

| Topic/Keyword | Comp 1 Rank | Comp 2 Rank | Comp 3 Rank | Client Rank | Monthly Volume | Priority |
|--------------|------------|------------|------------|------------|---------------|---------|
| [topic] | P[X] | P[X] | P[X] | Not ranking | [est.] | Critical |
| [topic] | P[X] | P[X] | P[X] | Not ranking | [est.] | High |

### Advantage Topics (Only Leader Covers)
Topics only the #1-ranking competitor addresses = replication opportunity:

| Topic | Competitor | Comp URL | Page Type | Est. Volume | Opportunity |
|-------|-----------|---------|----------|------------|------------|
| [topic] | [comp] | [url] | Blog/Service/FAQ | [vol] | High/Med |

### Competitor-Specific Content Audits
For each competitor (from competitor-profiles.md), list their top 10 pages by traffic (Ahrefs → Organic Pages):

| Competitor | Top Content | Traffic/Month | Content Type | Client Equivalent? |
|-----------|------------|-------------|-------------|-------------------|
| Comp 1 | [page title] | [est.] | Pillar/Blog | Yes/No |
| Comp 2 | [page title] | [est.] | Service/FAQ | Yes/No |

---

## Section 2: Content Format Gaps

Beyond topics — are the right content FORMATS missing? Identified from competitor analysis:

| Format | Client Has? | Competitors Have? | AIO Eligible? | Impact | Priority |
|--------|-----------|-----------------|------------|--------|---------|
| "How much does [service] cost in [city]?" pricing guide | Yes/No | Yes/No | High | High | |
| "[Service A] vs. [Service B]" comparison page | Yes/No | Yes/No | High | High | |
| "Signs you need [service]" diagnostic guide | Yes/No | Yes/No | Medium | Medium | |
| "DIY vs. Professional [service]" guide | Yes/No | Yes/No | Medium | Medium | |
| "[Service] process: step-by-step" explainer | Yes/No | Yes/No | High | High | |
| "How long does [service] take?" FAQ | Yes/No | Yes/No | High | Medium | |
| "Emergency [service] [city]" — intent page | Yes/No | Yes/No | High | Critical | |
| Local guide: "Complete guide to [service] in [city]" | Yes/No | Yes/No | High | High | |
| "Best [service] in [city]" owned list (client-authored) | Yes/No | Yes/No | High | High | |
| Seasonal: "[service] in winter/summer" | Yes/No | Yes/No | Low | Low | |
| Video: before/after showing [service] | Yes/No | Yes/No | Medium | High | |

---

## Section 3: Golden Opportunities (Blue Ocean)

### Topics with Real Demand + No Strong Competitor Coverage
Identify through: low-KD keywords in Ahrefs, PAA questions with poor answers, AlsoAsked.com questions with no direct client/competitor content:

| Topic/Question | Search Volume | KD (1-100) | Best Existing Answer | Quality Gap | Opportunity |
|--------------|-------------|-----------|---------------------|------------|------------|
| [topic] | [vol] | [KD] | [site.com] | Poor/Fair | Win featured snippet |

### Rising Trends (Emerging Demand)
Use Google Trends + Ahrefs Explorer → filter for growing keywords:

| Emerging Topic | Trend Direction | Current Volume | Projected Volume | First-Mover Opportunity |
|--------------|---------------|--------------|----------------|------------------------|
| [topic] | Rising ↑ | [vol] | [proj.] | High/Medium |

### Unanswered PAA Questions
For target keywords, check PAA boxes — identify questions where no result fully satisfies:

| Question | Source | Current Answer Quality | Content Type Needed | AIO Priority |
|---------|--------|----------------------|-------------------|------------|
| [question] | Google PAA | Poor/Fair | FAQ + HowTo schema | High/Med |

### Unowned Featured Snippets
Use Ahrefs → SERP Features → filter for "Featured Snippet" in keywords client doesn't own:

| Query | Current Snippet Owner | Snippet Quality | Win Strategy | Effort |
|-------|----------------------|----------------|-------------|--------|
| [query] | [site] | Thin | Direct answer + table/list | 1–2 hrs |

---

## Section 4: AI Overview Gap Analysis (2025 Critical)

AIO appears for 20–35% of local service queries. Being absent from AIO = invisible to AI-first searchers.

For top 30 target keywords, test AIO presence:

| Keyword | AIO Appears? | Client Cited in AIO? | AIO Format | Content Fix Needed |
|---------|-----------|---------------------|-----------|-------------------|
| [keyword] | Yes/No | Yes/No | List/Paragraph/Table | FAQPage + direct answer |

**AIO content requirements to win citation:**
1. Direct standalone answer in first 50 words of the page
2. FAQPage schema with question/answer matching the AIO query pattern
3. Business rated ≥4.3 stars (review signal for local AIO)
4. Content updated within 90 days (freshness = AIO citation bias)
5. HowTo schema for process-based queries

**AIO Gap Summary:**
| Service Cluster | AIO Appears? | Client Cited? | Pages Needed |
|----------------|------------|------------|-------------|
| [service 1] | Yes for X/10 queries | No | [specific pages] |

---

## Section 5: Existing Page Improvement Opportunities

Don't just create new content — improving existing pages often delivers results in 2–4 weeks vs. 3–6 months for new pages.

### Position 4–10 Quick Wins (High Priority — Low Competition)
From GSC + Ahrefs → Organic Keywords → filter for positions 4–10:

| Page | Current Position | Target Keyword | Monthly Volume | Action | Effort |
|------|----------------|---------------|--------------|--------|--------|
| [URL] | 5 | [keyword] | [vol] | Add FAQ section + schema | 1–2 hrs |
| [URL] | 8 | [keyword] | [vol] | Add 500 words + internal links | 2–3 hrs |

### Position 11–20 Opportunities (Page 2 → Page 1)
From GSC → filter positions 11–20 for high-volume keywords:

| Page | Position | Keyword | Volume | Action | Effort |
|------|---------|---------|--------|--------|--------|
| [URL] | 13 | [keyword] | [vol] | Expand + earn 3 links | 3–5 hrs + link |

### High Impressions / Low CTR (GSC)
Pages generating many impressions but <2% CTR → title/meta problem, not ranking problem:

| Page | Impressions/Month | CTR | Position | Recommended Title | Effort |
|------|-----------------|-----|---------|-----------------|--------|
| [URL] | [X] | [X%] | [pos] | [new title — add emotional trigger] | 15 min |

### Content Decay — Declining Pages (>20% YoY impressions drop)
From GSC YoY comparison:

| Page | Prior Clicks | Current Clicks | YoY Change | Action | Priority |
|------|------------|--------------|-----------|--------|---------|
| [URL] | [X] | [Y] | -[%] | Refresh stats/examples + schema | Critical if >50% |

---

## Section 6: Local Content Gaps

Location-specific content gaps often have lower competition and high conversion intent.

### City/Neighborhood Content Missing (Service × Location Matrix)

| | [City 1] | [City 2] | [Neighborhood 1] | [Neighborhood 2] |
|-|---------|---------|-----------------|-----------------|
| [Service A] | ✅ | ❌ | ❌ | ❌ |
| [Service B] | ✅ | ✅ | ❌ | ❌ |
| [Service C] | ❌ | ❌ | ❌ | ❌ |

**Priority: red cells with highest population/search density first.**

### Emergency + High-Intent Local Gaps
| Query Pattern | Volume | Client Page? | Action |
|-------------|--------|------------|--------|
| "Emergency [service] [city]" | [vol] | Yes/No | Create dedicated emergency page |
| "[service] open now [city]" | [vol] | Yes/No | Add hours + GBP service markup |
| "Same day [service] [city]" | [vol] | Yes/No | Create/optimize service page |
| "24 hour [service] [city]" | [vol] | Yes/No | Create/optimize service page |

---

## Section 7: Content Gap Priority Matrix

Score all identified gaps. Build/improve the highest-priority first:

| Gap | Content Type | Est. Monthly Traffic | Competition (KD) | Time to Rank | Impact (1–5) | Feasibility (1–5) | Priority | Effort |
|-----|------------|--------------------|--------------------|------------|-------------|-------------------|---------|--------|
| [table-stakes topic] | Blog post | [vol] | Low (<20) | 1–3 months | 4 | 4 | 16 | 4–6 hrs |
| [missing service page] | Service page | [vol] | Medium (20–50) | 2–4 months | 5 | 4 | 20 | 6–10 hrs |
| [unowned snippet] | FAQ section | [vol] | Low | 2–8 weeks | 4 | 5 | 20 | 1–2 hrs |
| [AIO gap] | FAQ + schema | [vol] | N/A | 2–6 weeks | 5 | 5 | 25 | 1–2 hrs |
| [P4–10 quick win] | Expand existing | [vol] | Low | 2–4 weeks | 4 | 5 | 20 | 1–2 hrs |

**Top 10 Priority Content Pieces (ordered by Priority Score):**
1. [Content title] — [keyword] — [format] — [est. traffic] — Effort: [X hrs]
2. [Content title] — [keyword] — [format] — [est. traffic] — Effort: [X hrs]
3. [Content title] — [keyword] — [format] — [est. traffic] — Effort: [X hrs]
4. [Content title] — [keyword] — [format] — [est. traffic] — Effort: [X hrs]
5. [Content title] — [keyword] — [format] — [est. traffic] — Effort: [X hrs]

---

## Output

Write complete findings to `{AUDIT_DIR}/content-gaps.md` with YAML frontmatter:

```yaml
---
skill: research/content-gaps
phase: 5
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
gaps_identified: [X]
quick_wins: [X]
aio_gaps: [X]
table_stakes_missing: [X]
---
```

Include:
- Score X/100 with gap severity breakdown
- Topic gaps table (all 3 competitors vs. client)
- Content format gaps checklist
- Golden opportunities list (blue ocean + PAA + snippets)
- AIO gap analysis table (30 target keywords)
- Existing page improvement opportunities (P4-10 quick wins)
- Local content matrix (service × location)
- Priority matrix (all gaps, Impact × Feasibility scored)
- Top 10 priority content pieces with effort estimates

**Key consumers:**
- `research/keyword-gaps` — keyword mapping for identified content gap topics
- `research/topical-gaps` — maps gaps to topical authority structure
- `output/report-generation` — feeds quick wins and 30/90-day content plans
