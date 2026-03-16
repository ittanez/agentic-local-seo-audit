---
name: topical-authority
description: >
  Topical authority assessment and building strategy. Activates when discussing
  domain topical authority, expertise signals, content authority building,
  Knowledge Graph topic recognition, E-E-A-T content authority, or competitive
  authority positioning. Phase 8. Output: {AUDIT_DIR}/topical-authority.md
---

# Topical Authority Audit — Phase 8

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — business name, URL, services, location.
Read `{AUDIT_DIR}/topical-gaps.md` — topical coverage map and identified gaps.
Read `{AUDIT_DIR}/competitor-profiles.md` — competitor authority signals.
Read `{AUDIT_DIR}/content-inventory.md` — content quality baseline.

**Tools for this phase:**
| Tool | Purpose | Cost |
|------|---------|------|
| **Ahrefs** | Topical authority via Domain Rating, organic traffic per topic cluster, content gap vs. competitors | Paid |
| **SEMrush** | Topic Research, Topical Authority score (0–100 per domain per topic), Keyword Gap | Paid |
| **Surfer SEO** | Content Score per page (target: 80+ for pillar, 70+ for cluster), NLP entity coverage | Paid |
| **Clearscope** | Content grade per page (target: A- for pillar, B+ for cluster), entity density analysis | Paid |
| **MarketMuse** | Topic model completeness, content brief generation, competitive content gap | Paid |
| **Google Search Console** | Which topics drive clicks — existing authority signals (free, requires access) | Free |
| **AlsoAsked.com** | PAA topic mapping — identify question clusters per topic pillar | Freemium |
| **Google Trends** | Topic momentum — rising vs. declining topics in the niche | Free |

**2025–2026 Topical Authority Context:**
- Google's AI Overviews (AIO) cite topically authoritative brands **2–3× more** than generalist sites
- Businesses that publish a minimum of **25 articles** on a topic cluster begin accumulating topical authority signals measurable in GSC (early 2026 observation)
- **58% AI Overview surge** across 9 industries in early 2026 — topical authority now directly determines AI citation rate
- **ChatGPT cites content updated within last 30 days** at 76.4% vs. 23.6% for older content — freshness is a citation factor
- Content decay: >20% YoY decline in clicks or impressions on a page signals topical authority loss on that cluster

---

## Section 1: Topical Authority Score (Per Core Topic)

For each main service/topic the business should own, score 5 dimensions:

### Scoring Dimensions
| Dimension | 1 (Weak) | 5 (Leader) | Assessment Method |
|-----------|---------|-----------|------------------|
| **Depth** | Surface 500-word overview | 3,000+ word expert pillar with unique data/case studies | Screaming Frog word count + manual quality check |
| **Breadth** | <5 subtopics covered | 20+ subtopics with dedicated pages | Ahrefs → Site Explorer → Organic Keywords → filter by topic |
| **Freshness** | Last updated 2+ years ago | Updated within 90 days, current-year stats | GSC → Performance → filter by page, check impressions trend |
| **Quality** | Generic AI-generated content | Unique expert insights, original data, proprietary methods | Manual review vs. Surfer Content Score ≥80 |
| **Recognition** | No featured snippets or PAA | Owns 5+ snippets, cited in AIO, topic entity in Knowledge Panel | Ahrefs → SERP Features filter; manual AIO search |

### Authority Matrix

| Core Topic | Depth /10 | Breadth /10 | Freshness /10 | Quality /10 | Recognition /10 | Total /50 | Grade |
|-----------|-----------|------------|--------------|------------|----------------|---------|-------|
| [service 1] | | | | | | | |
| [service 2] | | | | | | | |
| [local topic] | | | | | | | |

**Grade:** 45–50 = A (Market Leader) | 35–44 = B (Competitive) | 25–34 = C (Developing) | <25 = D/F (Weak)

**Article count per cluster (2025 threshold):**
| Cluster | Articles Published | Status |
|---------|------------------|--------|
| [topic] | [X] | <25 = below threshold / 25–50 = building / 50+ = authority |

---

## Section 2: Content Depth Standards (2025 Benchmarks)

| Page Type | Minimum Words | Surfer Target Score | Clearscope Grade | Internal Links |
|-----------|-------------|--------------------|--------------------|---------------|
| Pillar page | 3,000 | 80+ | A- or higher | 8–15 cluster links out |
| Cluster page | 1,500 | 70+ | B+ | 1 pillar + 3–5 cluster links |
| Supporting page | 900 | 65+ | B | 1 cluster or pillar link |
| FAQ entry | 250 | N/A | N/A | 1 service/pillar link |

Pages failing these thresholds are topical authority liabilities — they signal low expertise to Google's Helpful Content System.

**Content decay detection (using GSC):**
- Export GSC Performance data → compare this 90 days vs. same period last year
- Flag any page with >20% YoY decline in clicks or impressions → add to refresh queue
- Flag any page with >50% YoY decline → prioritize for full rewrite or consolidation

---

## Section 3: Competitor Authority Comparison

Use **Ahrefs** (Domain Rating + organic traffic per cluster) and **SEMrush** Topical Authority score:

| Topic | Client Pages | Client TA Score | Comp 1 Pages | Comp 1 TA | Comp 2 Pages | Comp 2 TA | Gap | Priority |
|-------|------------|----------------|------------|---------|------------|---------|-----|---------|
| [topic 1] | | | | | | | | H/M/L |
| [topic 2] | | | | | | | | H/M/L |

**Authority Leader Analysis:**
- Who leads for each topic? What content volume/depth gives them the edge?
- Use **Ahrefs Content Gap**: enter client domain vs. top 2 competitors → identify which topic clusters competitors rank for that client doesn't
- What is the page-count gap to match the leader per cluster?
- Which competitor has the highest Surfer Content Score on their pillar pages?

**Topical Dominance Opportunities:**
Topics where competitors have only 1–3 thin pages that client could dominate with a strong cluster:
| Topic | Competitor Coverage | Client Coverage | Opportunity Score |
|-------|-------------------|----------------|------------------|
| [topic] | [X thin pages] | [Y pages] | High/Med/Low |

---

## Section 4: Authority Signals Assessment

### Content Authority Signals (E-E-A-T)
- [ ] Expert author bylines with credentials on all topic-relevant content?
- [ ] Author pages: professional background, certifications, years of experience?
- [ ] Original research, local data, or client case studies published?
- [ ] Content citing authoritative sources (government, research, trade associations)?
- [ ] Unique perspectives not found elsewhere (proprietary methods, real project outcomes)?
- [ ] Real-world examples from actual client work (photos, outcomes, specifics)?

### Structural Authority Signals
- [ ] Complete topic clusters: pillar + cluster + supporting content (25+ articles per main cluster)?
- [ ] Internal links consistently reinforcing topic hierarchy (all cluster pages link to pillar)?
- [ ] All related subtopics covered — no significant gaps vs. AlsoAsked/PAA?
- [ ] Content comprehensiveness exceeds top competitor on Surfer side-by-side comparison?

### AI Visibility Authority Signals (2025 Critical)
- [ ] AIO appears for core topic queries? (`best [service] in [city]` — does client appear?)
- [ ] ChatGPT/Perplexity mentions client for core topic queries?
- [ ] Content updated within last 30 days on key pillar pages (freshness = AI citation factor)?
- [ ] FAQPage schema on all pillar pages (primary AIO trigger)?
- [ ] HowTo schema on service/tutorial pages?

### Recognition Authority Signals
- [ ] Featured snippets owned for core topic keywords? (Check Ahrefs → SERP Features)
- [ ] PAA boxes answered by site content? (Use AlsoAsked.com to map PAA questions)
- [ ] AI Overviews citing site for core topics? (Manual test: search 5 core queries)
- [ ] Google Knowledge Graph associating brand with topics?

### External Authority Signals
- [ ] Cited by other authoritative sites in the niche (editorial links, not paid)?
- [ ] Quoted in local news or industry publications?
- [ ] Industry association membership + content contribution?
- [ ] Speaking mentions or expert features in media?

---

## Section 5: Knowledge Graph Topic Association

Does Google associate this business with its core topics?

### Tests to Run
1. Search `[business name]` → does Knowledge Panel show core topics/services?
2. Search `[business name] [core topic]` → does Google show topic association in results?
3. Search `[core topic] [city]` → does Knowledge Panel or AIO mention this business?
4. Ask ChatGPT: `Who are the top [service] providers in [city]?` → is business mentioned?

### Building Topic Association (Sequence)
1. Publish minimum 25 articles on target topic cluster (threshold for authority accumulation)
2. Add Schema.org `knowsAbout` to Organization schema with core topic entities
3. Earn editorial links from authoritative sites mentioning business in topic context
4. Submit updated sitemap after publishing cluster content
5. Ensure all cluster pages link to pillar with consistent anchor text (no generic "click here")

---

## Section 6: Content Quality Standard (2025–2026)

For topical authority in 2025–2026, content must clear this bar:
- ✅ Written or reviewed by a genuine subject matter expert (named, credentialed)
- ✅ Contains specific, verifiable details competitors don't mention
- ✅ Includes original data, local examples, or proprietary perspectives
- ✅ Structured for both human readers and AI extraction (H2 hierarchy, FAQ, tables)
- ✅ Updated within 90 days — current-year statistics cited
- ✅ Demonstrates experience: real photos, case outcomes, specific project details
- ✅ Surfer Content Score ≥70 (cluster) or ≥80 (pillar)
- ❌ NOT bulk AI-generated without expert review (Helpful Content penalty risk)
- ❌ NOT generic "Here are 5 tips..." without depth and specifics
- ❌ NOT padded with filler to hit word count without adding information value
- ❌ NOT a content page with >20% YoY traffic decline left unrefreshed

---

## Section 7: Authority Building Roadmap

### Priority Matrix (Impact × Feasibility)
| Gap Type | Impact (1–5) | Feasibility (1–5) | Priority Score | Effort |
|----------|-------------|-------------------|----------------|--------|
| Thin pillar page (<1,500 words) → expand to 3,000+ | 5 | 4 | 20 | 6–10 hrs |
| Cluster below 25-article threshold | 5 | 3 | 15 | 4 hrs/article |
| Content decay: page losing >20% YoY clicks | 4 | 4 | 16 | 3–5 hrs/page |
| Missing FAQPage schema on pillars | 4 | 5 | 20 | 30 min/page |
| Expert author bylines missing | 4 | 5 | 20 | 1–2 hrs/page |
| Orphaned cluster pages (no link to pillar) | 4 | 5 | 20 | 15 min/page |
| Low Surfer Content Score (<65) | 4 | 4 | 16 | 2–4 hrs/page |
| AIO not appearing for core queries | 5 | 3 | 15 | 4–8 hrs (cluster expansion) |

### Immediate Priority (Next 30 Days)
1. Add FAQPage schema to all pillar pages — triggers AIO — Effort: 30 min/page — Priority: 20
2. Fix all orphaned cluster pages — add internal links to pillar — Effort: 15 min each — Priority: 20
3. Expand thin pillar pages to 3,000+ words with Surfer optimization — Effort: 6–10 hrs each
4. Refresh top 5 content decay pages (>20% YoY decline) — update stats, examples, schema

### Medium-Term (Days 31–90)
1. Build each cluster to 25+ articles (threshold for Google authority accumulation)
2. Add expert author bylines with credentials to all existing topic content
3. Commission original local study or data piece per pillar (primary AI citation trigger)
4. Use Ahrefs Content Gap to fill cluster pages competitors rank for that client doesn't

### Long-Term (Months 3–6)
1. Achieve 50+ article coverage on primary topic clusters
2. Build Clearscope grade A- on all pillar pages and B+ on all cluster pages
3. Earn 5+ editorial links from authoritative sites per core topic
4. Establish author entity associations in Google Knowledge Graph

---

## Output

Write to `{AUDIT_DIR}/topical-authority.md` with YAML frontmatter:

```yaml
---
skill: strategy/topical-authority
phase: 8
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
status: [leader|competitive|developing|weak]
topics_assessed: [X]
avg_cluster_article_count: [X]
---
```

Include:
- Score X/100 with per-topic breakdown
- Topic authority matrix (5 dimensions per core topic)
- Content depth table with Surfer Score targets
- Competitor authority comparison (TA score, page count, content quality)
- Authority signals checklist (content, structural, AI visibility, recognition, external)
- Content decay report (pages with >20% YoY decline)
- Knowledge Graph association status
- Priority authority building roadmap (Impact × Feasibility scored)
- 30/90/180-day content plan

**Key consumers:**
- `research/topical-gaps` — gap analysis informs authority building priorities
- `research/keyword-gaps` — keyword opportunities mapped to authority clusters
- `output/report-generation` — topical authority score in master report section 8
