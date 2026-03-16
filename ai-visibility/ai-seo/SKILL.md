---
name: ai-seo
description: >
  AI search visibility and AI SEO optimization. Activates when discussing AI
  Overviews, AI Mode, AEO, GEO, LLM SEO, ChatGPT visibility, Perplexity
  mentions, Gemini AI, Copilot, answer engine optimization, generative engine
  optimization, or any AI search presence topic.
  Phase 14. Output: {AUDIT_DIR}/ai-seo-findings.md
---

# AI Visibility & AI SEO Audit — Phase 14

## Executive Summary

AI search is the fastest-growing traffic channel in 2025. Google AI Overviews appear for 20–35% of local service queries (SparkToro 2025). ChatGPT Search has 200M+ monthly active users. Perplexity processes 100M+ queries/month. Being cited in AI answers = significant visibility gain; being absent = invisible to AI-first searchers. This phase audits where the client appears (or doesn't) across all major AI platforms, identifies content gaps causing AI invisibility, and produces a prioritized action plan for AI citation dominance.

**2025 AI search benchmarks:**
- AIO citation rate: pages with FAQPage schema cited 3.2× more than pages without (Amsive 2025)
- ChatGPT freshness: pages updated within 30 days cited at 76.4% rate vs. 31.2% for 90+ day old pages
- Perplexity local query share: 18% of all queries are local business intent (Perplexity data, 2025)
- AIO + organic position 1 = ~45% CTR combined (vs. ~25% for position 1 alone when AIO shows)

---

## Tools for This Phase

| Tool | Purpose | Cost |
|------|---------|------|
| **Google Search** (incognito) | Test AIO presence for top 20–30 target keywords | Free |
| **ChatGPT** (GPT-4o with Search) | LLM visibility test — local service queries | Free/Paid |
| **Perplexity** | AI search citations for local service queries | Free |
| **Google Gemini** | Gemini AI visibility test + source attribution | Free |
| **Microsoft Copilot** | Bing-powered AI visibility | Free |
| **Google Rich Results Test** | FAQPage, HowTo, Speakable schema validation | Free |
| **Ahrefs** | Featured snippet ownership — AIO pulls from snippets | Paid |
| **SEMrush** | Featured snippet tracking per target keyword | Paid |
| **AlsoAsked.com** | PAA question mapping — AIO uses PAA patterns | Freemium |
| **Otterly.ai** | Track AIO mentions over time (monitoring) | Paid |

---

## The AI Search Landscape (2025-2026)

AI search is no longer emerging — it IS the mainstream:
- **Google AI Overviews**: Shown for ~20-30% of queries (growing)
- **Google AI Mode**: Full conversational search experience
- **ChatGPT Search**: Now default for 200M+ users with web access
- **Perplexity**: 100M+ monthly queries, growing fast
- **Microsoft Copilot**: Integrated into Windows/Edge/Bing
- **Gemini (Google)**: Deep integration with Android + Google Workspace
- **Claude (Anthropic)**: Growing presence with web search

For local businesses, AI search drives both:
1. Direct visibility (being mentioned in AI answers)
2. Competitive displacement (competitor gets the mention instead)

---

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — business name, URL, services, location.
Read `{AUDIT_DIR}/competitor-profiles.md` — competitor AI visibility signals.
Read `{AUDIT_DIR}/onpage-findings.md` — content structure gaps.

---

## Section 1: Google AI Overviews (AIO) Audit

### Test Protocol
Test top 20-30 target keywords in Google Search (incognito, desktop + mobile):

For each query, document:
| Query | AIO Shows? | Client Cited? | Competitors Cited? | Source URLs Used | AIO Format |
|-------|-----------|--------------|-------------------|-----------------|-----------|
| [query] | Yes/No | Yes/No | [names] | [URLs] | Paragraph/List/Table/Steps |

### AIO Appearance Patterns to Identify
- Which query types trigger AIO? (Informational, local, how-to, comparison?)
- Which content format is used in AIO? (Paragraphs, numbered steps, bullet lists?)
- What's the word count of the cited answer section?
- Does AIO pull from the first paragraph? A specific H2 section?
- Are any client pages cited? If so, which ones and why?

### AIO Optimization Strategy
To be cited in AI Overviews, content needs:
1. **Direct answers** — First 40-60 words answer the query directly
2. **Question-format headers** — H2: "What is [topic]?" / "How does [process] work?"
3. **Structured formatting** — numbered steps, bullet lists, tables rank well
4. **Unique data/insights** — AI cites specific facts, statistics, and expert opinions
5. **E-E-A-T signals** — Strong author credentials, institutional trust
6. **Comprehensive coverage** — Answer main query + related sub-questions
7. **Page authority** — Higher authority pages cited more often

---

## Section 2: Google AI Mode Audit

Google AI Mode (launched 2024, expanding 2025) enables fully conversational search.

### Test AI Mode Queries
- Enable AI Mode (Google account > Experiments or rolled-out region)
- Test conversational queries:
  - "What's the best [service] in [city] and why?"
  - "Compare [client] vs. [competitor 1] for [service]"
  - "I need [service] near [neighborhood] — any recommendations?"
  - Follow-up: "What makes them stand out?"

### Document Findings
| Query | Client Mentioned? | Accuracy | Competitor Priority | Source |
|-------|-----------------|---------|-------------------|--------|

---

## Section 3: LLM Visibility Audit (ChatGPT, Perplexity, Gemini, Copilot, Claude)

### Test Matrix
For each platform × query type:

**Platforms to test:**
- ChatGPT (GPT-4o with Search)
- Perplexity
- Google Gemini
- Microsoft Copilot
- Claude.ai (Anthropic)

**Query types to test:**
1. `Best [service] in [city]`
2. `[Service] near [neighborhood/landmark]`
3. `[Business Name]` — accuracy check
4. `[Business Name] reviews` — reputation
5. `How to find a good [service type] in [city]`
6. `[Specific service] cost in [city]`

**For each result document:**
- Business mentioned? (Yes/No)
- Accuracy of info (address, phone, hours, services)?
- Positive/negative framing?
- Competitors mentioned instead?
- Source URLs cited?
- Position (1st mention / 2nd / not mentioned)?

### LLM Visibility Score (per platform)
- Mentioned accurately in top 3 answers: 5/5
- Mentioned but with errors: 3/5
- Mentioned peripherally: 1/5
- Not mentioned: 0/5

---

## Section 4: AEO — Answer Engine Optimization Assessment

AEO focuses on structuring content so AI can extract and use it as answers.

### Content Assessment
For each key service page and FAQ page:
- [ ] Does each section start with a direct, standalone answer?
- [ ] Are definitions provided for key service terms?
- [ ] Are process steps numbered and clearly labeled?
- [ ] Are comparisons structured in tables?
- [ ] Are FAQs in explicit question + answer format (not buried)?
- [ ] Are specific figures, statistics, and data points included?
- [ ] Can the answer be extracted and read without surrounding context?

### FAQ Content Audit
- FAQ page exists?
- FAQs based on real customer questions (not generic)?
- FAQPage schema implemented?
- PAA (People Also Ask) boxes captured with existing content?
- Test: do current FAQs appear in PAA for target queries?

### Featured Snippet Optimization
Since AI Overviews pull from featured snippets:
- Which target queries have featured snippets?
- Does the client own any?
- What format does the winning snippet use?
- What page structure modifications are needed to win it?

---

## Section 5: GEO — Generative Engine Optimization Assessment

GEO focuses on making content easily citable by AI systems.

### Citeability Checklist
- [ ] Specific, quotable statements with data?
  Good: "Chicago homeowners saved an average of $2,400/year after our insulation upgrade"
  Bad: "We help homeowners save money on energy bills"

- [ ] Original research, surveys, or case studies?
- [ ] Named expert quotes with credentials?
- [ ] Step-by-step instructions with clear numbered format?
- [ ] Comparison tables with specific data?
- [ ] Local statistics about the service area?
- [ ] Industry benchmarks stated clearly?

### Source Authority Assessment
AI systems cite authoritative sources. Check:
- Domain authority and trust indicators
- E-E-A-T signals present (author, expertise, experience demonstrated)
- Linked to from other authoritative sources in the niche?
- Consistently mentioned on industry resource pages?

### Entity Optimization for AI
AI systems understand entities better than raw keyword text:
- Is the business entity clearly defined (who, what, where, when)?
- Are service entities named consistently (using industry-standard terminology)?
- Are geographic entities precise (neighborhood, city, region)?
- Do related entities connect? (business → services → location → team)?
- Schema markup reinforces all entity relationships?

---

## Section 6: Structured Data for AI Readability

Schema types most valuable for AI citation:
| Schema Type | AI Benefit |
|------------|-----------|
| LocalBusiness | Business entity establishment |
| FAQPage | Direct Q&A extraction |
| HowTo | Step-by-step answer extraction |
| Article + Author | E-E-A-T, content authority |
| AggregateRating | Trust signal for AI recommendations |
| Speakable | Marks content optimized for voice/AI reading |
| Service | Clear service entity definition |
| Review | Specific review content citation |

Validate all schema at: search.google.com/test/rich-results

---

## Section 7: Competitor AI Visibility Comparison

| Platform | Client Score | Comp 1 | Comp 2 | Comp 3 |
|----------|-------------|--------|--------|--------|
| Google AIO | | | | |
| ChatGPT Search | | | | |
| Perplexity | | | | |
| Gemini | | | | |
| Copilot | | | | |
| Overall AI Score | | | | |

**Findings:** Which competitor dominates AI visibility and why? What content do they have that the client lacks?

---

## Section 8: AI SEO Action Plan

### Priority Matrix

| Action | Impact (1–5) | Feasibility (1–5) | Priority | Effort |
|--------|-------------|-------------------|---------|--------|
| Add FAQPage schema to all service pages | 5 | 5 | 25 | 30 min/page |
| Rewrite service page intros (direct 50-word answer) | 5 | 4 | 20 | 30–60 min/page |
| Add specific data points (costs, timelines) to pages | 5 | 4 | 20 | 30–60 min/page |
| Create dedicated FAQ page (conversational queries) | 4 | 5 | 20 | 2–4 hrs |
| Add question-format H2s to top 5 service pages | 4 | 4 | 16 | 30 min/page |
| Add HowTo schema to process pages | 4 | 5 | 20 | 30 min/page |
| Publish original research / local statistics page | 5 | 3 | 15 | 4–8 hrs |
| Build E-E-A-T author profiles (credentials, bios) | 4 | 4 | 16 | 2–4 hrs |
| Refresh pages > 30 days old (freshness = AIO boost) | 4 | 5 | 20 | 30–60 min/page |
| Add Speakable schema to key answer sections | 3 | 4 | 12 | 30 min |

### Immediate (Week 1–2) — Quick Wins
- [ ] Add FAQPage schema to all service pages — Effort: 30 min/page — Expected: 3.2× more AIO citations
- [ ] Rewrite service page intros with direct standalone answers (first 50 words) — Effort: 30–60 min/page
- [ ] Add specific data points (pricing, timelines, statistics) to every service page — Effort: 30–60 min/page

### Short-Term (Month 1)
- [ ] Create dedicated FAQ page optimized for conversational queries — Effort: 2–4 hrs
- [ ] Restructure top 5 service pages with question-format H2s — Effort: 30 min/page
- [ ] Publish original research piece (local survey, case study, cost data) — Effort: 4–8 hrs
- [ ] Add HowTo schema to all process-based pages — Effort: 30 min/page

### Medium-Term (Months 2–3)
- [ ] Build E-E-A-T author profiles for all content contributors — Effort: 2–4 hrs
- [ ] Earn citations from authoritative local/industry sites — Effort: ongoing
- [ ] Create content that fills AI citation gaps vs. top competitor — Effort: 2–4 hrs/piece

---

## Scoring

| Category | Weight |
|----------|--------|
| Google AI Overviews presence | 25% |
| ChatGPT/Perplexity/Gemini visibility | 25% |
| AEO content structure | 20% |
| GEO citeability signals | 15% |
| Schema for AI readability | 15% |

---

## Output

Write complete findings to `{AUDIT_DIR}/ai-seo-findings.md` with YAML frontmatter:

```yaml
---
skill: ai-visibility/ai-seo
phase: 14
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
aio_cited: [yes|no|partial]
chatgpt_cited: [yes|no]
perplexity_cited: [yes|no]
faqpage_schema: [yes|no|partial]
aio_keywords_tested: [X]
aio_keywords_cited: [X]
---
```

Include:
- Score X/100 with per-category breakdown
- Full AI visibility matrix (all 5 platforms × 6 query types)
- AIO appearance analysis for top 20–30 keywords
- Competitor AI visibility comparison table
- AEO content structure checklist (per key page)
- GEO citeability checklist
- Schema for AI readability (present vs. missing per page)
- Content gap list (what's missing for AI citation)
- Priority matrix (all actions, Impact × Feasibility scored)
- 30/90-day AI SEO action plan with effort estimates

**Output files:**
- `{AUDIT_DIR}/ai-seo-findings.md` — AI visibility audit with score and citation gap analysis
- `{REPORTS_DIR}/phase-14-ai-seo.pdf` — auto-generated PDF after phase completes

**Key consumers:**
- `ai-visibility/voice-search` — voice and AIO share optimization signals
- `audit/onpage-seo` — AIO structure requirements inform on-page optimization
- `cross-cutting/serp-trust-auditor` — Trust & AI Readiness (T2) dimension
- `output/report-generation` — AI visibility section in master report

---

## AI Visibility Quick Reference

### Schema Markup Priority for AI Citation

| Schema Type | AIO Citation Boost | Implementation | Effort |
|------------|-------------------|----------------|--------|
| FAQPage | 3.2× citation rate | Add to all service + location pages (5 FAQ min) | 30 min/page |
| HowTo | 2.1× for process queries | Add to any "how to" or process service pages | 45 min/page |
| Organization + sameAs | Entity confidence boost | Homepage only; include 7+ sameAs URLs | 30 min |
| AggregateRating | +17–25% branded CTR | All pages with real review data | 30 min |
| LocalBusiness subtype | Local AIO eligibility | Homepage + key service pages | 30 min |
| BreadcrumbList | Navigation context for AI | Sitewide (via CMS plugin often) | 1 hr |

### 2025 AI Search Platform Benchmarks

| Platform | Local Coverage | Citation Criteria | Update Frequency |
|---------|---------------|------------------|-----------------|
| Google AI Overviews | 20–35% of local queries | E-E-A-T + schema + topical authority | Real-time (Gemini-based) |
| ChatGPT (web search) | 15–25% of local queries | Freshness (76.4% cite <30-day pages) | Weekly crawl |
| Perplexity AI | 10–20% of local queries | Source authority + content depth | Real-time |
| Google Gemini (assistant) | Growing rapidly | Knowledge Graph entity strength | Real-time |
| Bing Copilot | 5–15% of local queries | Bing indexation + content trust | Daily crawl |

### GBP + AIO Local Pack Integration
GBP-driven AI Overviews for local queries: "best [service] near me" queries now show AIO with local pack. To appear:
1. GBP must be verified and have 4.0+ star rating with 20+ reviews
2. Business category must exactly match query intent
3. Website must have LocalBusiness schema with areaServed matching the user's location
4. Q&A section must have keyword-relevant answers seeded

INP for AI search: Googlebot renders pages before indexing for AIO inclusion. Pages with INP >500ms may have content not fully extracted for AI citations. Target INP <200ms on all schema-rich pages.
