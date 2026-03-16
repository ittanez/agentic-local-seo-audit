---
name: penalty-check
description: >
  Google penalty and manual action detection. Activates when discussing
  traffic drops, penalties, manual actions, algorithm updates, deindexation,
  ranking losses, or suspicious pattern detection. Run this EARLY — a confirmed
  penalty invalidates all other optimization work until resolved.
  Phase 20. Output: {AUDIT_DIR}/penalty-findings.md
---

# Penalty & Manual Action Check — Phase 20

## Why Run First (Wave 1)

A penalty makes 90% of other audit findings irrelevant until resolved.
Check penalty status before deep-diving into optimization.

---

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` for business name, URL, and project paths.
Read `{AUDIT_DIR}/competitor-profiles.md` for competitor traffic benchmarks (clean sites for comparison).

---

## Step 2: Manual Actions Check

### GSC Manual Actions (If Access Available)
- Navigate: GSC → Security & Manual Actions → Manual Actions
- Document any manual actions: type, scope (site-wide / partial), date applied
- Check if reinclusion request ever submitted

**Tools:** Google Search Console (free), Ahrefs Site Audit → Manual Actions alerts (paid)

### Manual Action Types — 2025 Reference Table
| Type | What It Means | Severity | Avg Recovery Time |
|------|--------------|---------|-------------------|
| Unnatural links to your site | Toxic backlink profile | 🔴 Critical | 3–6 months after disavow |
| Unnatural links from your site | Selling/exchanging links | 🔴 Critical | 2–4 months after cleanup |
| Thin content with little or no added value | Thin/duplicate content at scale | 🔴 Critical | 1–3 months after improvement |
| Cloaking / sneaky redirects | Showing different content to Google vs. users | 🔴 Critical | 1–2 months after fix |
| Pure spam | Site flagged as spam network | 🔴 Critical | 6–12 months (or never) |
| User-generated spam | UGC sections used by spammers | 🟠 High | 1–2 months |
| Structured data issue | Schema spam or misleading markup | 🟠 High | 2–4 weeks |
| AMP content mismatch | Different content in AMP vs. canonical | 🟡 Medium | 2–4 weeks |
| Site reputation abuse | Hosting low-quality 3rd-party content for ranking | 🔴 Critical | 3–6 months (added May 2024) |
| Scaled content abuse | Mass AI-generated or low-value content | 🔴 Critical | 3–6 months (2024+) |

---

## Step 3: Algorithm Penalty Detection

Even without GSC access, detect algorithmic penalties via traffic pattern analysis.

### Tools for Traffic Pattern Analysis
- **Semrush Sensor** — tracks daily ranking volatility (free tier available)
- **Algoroo** — algorithm update correlation tool (free)
- **MozCast** — SERP turbulence tracker (free)
- **SimilarWeb** — estimated organic traffic trend (freemium)
- **Wayback Machine** — historical site snapshots to detect major content changes

### 2025 Algorithm Update Timeline (Cross-Reference Traffic Drops)
| Update | Date | What It Targets |
|--------|------|----------------|
| Helpful Content System | Sep 2023, Mar 2024 | Unhelpful, SEO-first content |
| Core Update | Mar 2024 | Broad quality assessment — hit many small sites |
| Spam Update | Mar 2024, Jun 2024 | Link spam, scaled content abuse, expired domain abuse |
| Site Reputation Abuse | May 2024 | Hosting 3rd-party low-quality content for ranking |
| Core Update | Aug 2024 | Quality, EEAT, unhelpful content |
| Core Update | Nov 2024 | Continued quality signals, authority |
| Core Update | Mar 2025 | AI-generated content abuse, low-value content at scale |
| AI Overview impact | 2024–2025 ongoing | Reduces organic CTR for featured results |
| Spam Update | Jun 2025 | Evolved link spam detection |

### Traffic Pattern Red Flags
| Pattern | Likely Cause | Severity |
|---------|-------------|---------|
| Sudden 30%+ drop on specific date | Algorithmic penalty | 🔴 Critical |
| Gradual 50%+ decline over 6–12 months | Quality/HCU issue | 🟠 High |
| Drop in branded traffic only | Trust/reputation issue | 🟠 High |
| Specific page type affected (e.g., all blog posts) | Content quality issue | 🟡 Medium |
| Specific keyword category affected | Topical relevance issue | 🟡 Medium |
| Mobile traffic drops more than desktop | Mobile usability issue | 🟡 Medium |

---

## Step 4: Unnatural Link Profile Analysis

### Tools
- **Ahrefs** → Site Explorer → Backlinks → filter: Dofollow, new links velocity
- **Google Search Console** → Links → Top linking sites + anchor text distribution
- **Semrush** → Backlink Audit → Toxic Score breakdown
- **Majestic** → Trust Flow vs. Citation Flow ratio (TF/CF < 0.3 = risk)

### Unnatural Link Red Flags (Specific Thresholds)
| Signal | Red Flag Threshold | Tool to Check |
|--------|-------------------|--------------|
| Exact-match commercial anchors | >10% of link profile | Ahrefs anchor report |
| Referring domains from .ru/.cn spam | >5% of RD count | Ahrefs + GSC |
| Links from same C-class IPs | >20 links from same /24 subnet | Majestic |
| Trust Flow < Citation Flow (TF:CF) | Ratio < 0.3 | Majestic |
| Sudden referring domain spike | +500% in 30 days then crash | Ahrefs history |
| Footer/sitewide links from unrelated sites | Any present | Ahrefs link type filter |
| PBN or link farm patterns | DA <10 + no real content | Ahrefs + manual check |

### Disavow File Status
- Locate: GSC → Links → Disavow
- Has a disavow file been submitted? When was it last updated?
- Are new toxic links appearing AFTER the disavow submission?

---

## Step 5: Thin/Duplicate Content Check

### Tools
- **Screaming Frog SEO Spider** — crawl for word counts, duplicate titles/metas, thin pages
- **Siteliner** — duplicate content % across site (free up to 250 pages)
- **Google Search Console** → Coverage → Excluded pages (indexation issues)
- **Copyscape** — detect scraped/plagiarised content (paid)
- **site_crawler.py** → reads `{DATA_DIR}/crawl/` for word count data per page

### Thin Content Thresholds
| Content Type | Minimum Word Count | Red Flag |
|-------------|-------------------|---------|
| Homepage | 600+ words | <400 words |
| Service page | 800+ words | <500 words |
| Location page | 600+ words | <400 words |
| Blog post | 1,200+ words | <600 words |
| Product page | 400+ words | <200 words |

### Scaled Content Abuse Detection (2024–2025 Critical)
- Large volumes of AI-generated pages with no human editorial oversight
- Programmatic pages targeting location × service variations with near-identical content
- Content that answers questions but provides no unique experience, expertise, or data
- Pages with high bounce rate + zero dwell time + no engagement signals

---

## Step 6: Technical Deception Check

```bash
# Googlebot vs. user-agent comparison
curl -A "Googlebot" https://domain.com    # Googlebot view
curl https://domain.com                    # User view
# Compare: different content = cloaking risk

# Redirect chain check
curl -IL https://domain.com

# Hidden text detection (in browser console)
document.querySelectorAll('[style*="display:none"], [style*="visibility:hidden"]')
```

### Search Operator Verification
```
site:domain.com                     → Total indexed pages (flag if >2× sitemap count)
site:domain.com -www                → www/non-www duplicate check
site:domain.com inurl:?             → Parameterized duplicate pages being indexed
"[business name]" -site:domain.com → Scraped copies of content
cache:domain.com                    → Last crawl date and cached content
domain.com spam                     → External spam reports
domain.com penalized                → Community penalty reports
```

---

## Step 7: Competitor Clean Profile Benchmark

Compare the target site's signals against confirmed-clean competitor sites. This establishes what a healthy local business looks like in this niche.

| Signal | Client | Top Competitor | 2nd Competitor | Healthy Benchmark |
|--------|--------|----------------|----------------|-------------------|
| Organic traffic trend (6mo) | ±% | ±% | ±% | Stable or growing |
| Referring domains (total) | # | # | # | Industry average |
| Avg anchor text: branded | % | % | % | 50–60% |
| Avg anchor text: exact match | % | % | % | <10% |
| Indexed pages vs. sitemap | ratio | ratio | ratio | Within 20% |
| Pages <300 words | % | % | % | <5% of crawled |
| Manual actions | Yes/No | Yes/No | Yes/No | None |
| GSC coverage errors | # | n/a | n/a | <1% of indexed |

---

## Step 8: AI Visibility Impact of Penalties (2025)

A Google algorithmic penalty has compounding effects beyond organic search:
- **AI Overview exclusion** — Penalized or low-trust sites are rarely cited in AI Overviews
- **Knowledge Graph suppression** — Spam signals reduce entity trust score
- **Brand SERP damage** — Negative SERP features appear for branded queries
- **AI assistant citations** — ChatGPT, Perplexity, Gemini avoid citing penalized or low-trust domains

Check: Search `[business name] site:domain.com` in AI Overviews / Perplexity / ChatGPT. Is the site referenced?

---

## Step 9: Recovery Roadmap (If Penalty Confirmed)

### Manual Action Recovery (ordered by priority)
1. **Identify exact violation** — Read GSC manual action notice verbatim — Effort: 30 min
2. **Link cleanup** — Contact webmasters to remove toxic links (email each) — Effort: 2–5 hrs
3. **Create disavow file** — List all remaining toxic domains/URLs — Effort: 1–2 hrs
4. **Submit disavow** — Upload to GSC Disavow Tool (use domain: prefix) — Effort: 15 min
5. **Fix underlying content violations** — Rewrite thin pages (800+ words each) — Effort: 2–4 hrs per page
6. **Submit reinclusion request** — After ALL violations resolved — Effort: 30 min — Wait: 2–8 weeks
7. **Monitor GSC weekly** — Track manual action status + coverage changes — Effort: 30 min/week

### Algorithmic Recovery (Helpful Content / Core Updates)
1. **Audit worst-performing pages** (Screaming Frog + GSC performance data) — Effort: 2 hrs
2. **Prune or consolidate thin content** — Noindex or 301 redirect to better page — Effort: 1 hr per page
3. **Improve E-E-A-T signals** — Author bios, original data, expert quotes — Effort: 4–8 hrs per page
4. **Wait for next core update** — Google only re-evaluates during Core Updates (quarterly) — Timeline: 3–6 months
5. **Monitor with Semrush Sensor** — Track volatility correlation to recovery — Effort: 15 min/week

---

## Step 10: Scoring

| Category | Score Contribution | Weight |
|----------|------------------|--------|
| No manual actions present | 25 pts | Critical |
| No algorithmic correlation to traffic drop | 20 pts | High |
| Clean link profile (TF:CF >0.3, <10% exact-match) | 20 pts | High |
| No thin/duplicate content at scale | 20 pts | High |
| No technical deception signals | 15 pts | Medium |

**Score Interpretation:**
| Score | Status | Interpretation |
|-------|--------|---------------|
| 90–100 | ✅ Clean | No penalty signals — proceed with full audit |
| 70–89 | ⚠️ Caution | Risk factors present — monitor closely |
| 50–69 | 🟠 Risk | Likely algorithmic issues — investigate and improve |
| 30–49 | 🔴 High Risk | Probable unresolved penalty — prioritize recovery |
| <30 | ❌ Critical | Confirmed penalty — halt other phases until resolved |

**Priority Matrix:**
| Action | Impact (1–5) | Feasibility (1–5) | Priority Score |
|--------|-------------|-------------------|----------------|
| Submit disavow file | 5 | 4 | 20 |
| Remove/noindex thin pages | 4 | 4 | 16 |
| Improve E-E-A-T on key pages | 5 | 3 | 15 |
| Submit reinclusion request | 5 | 5 | 25 |
| Fix canonical / redirect issues | 4 | 4 | 16 |

---

## Output Format

Write to `{AUDIT_DIR}/penalty-findings.md` with this structure:

```yaml
---
skill: audit/penalty-check
phase: 20
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
status: [clean|caution|risk|critical]
---
```

```
AUDIT PHASE: Penalty Check | ID: PENALTY-001 | Phase: 20
BUSINESS: [Name] | URL: [URL] | DATE: [Date]
SCORE: X/100 | STATUS: ✅ Clean / ⚠️ Caution / 🔴 Risk / ❌ Critical

MANUAL ACTIONS: None / [type, scope, date]
ALGORITHMIC CORRELATION: None / [update name, date, traffic % drop]

PENALTY TYPE:         [if applicable]
SCOPE:               Site-wide / Partial
LIKELY CAUSE:        [link spam / thin content / cloaking / scaled content]
RECOVERY STATUS:     Not Started / In Progress / Resolved

CRITICAL ISSUES:
🔴 [issue with evidence, tool that found it, steps to fix]

HIGH PRIORITY:
🟠 [issue with evidence and priority score: Impact × Feasibility]

COMPETITOR COMPARISON:
| Signal             | Client | Comp 1 | Comp 2 | Benchmark |
|--------------------|--------|--------|--------|-----------|
| Organic trend 6mo  |        |        |        | Growing   |
| Exact-match anchors|  %     |  %     |  %     | <10%      |
| Indexed pages      |        |        |        | ~sitemap  |

RECOVERY ROADMAP (if penalty confirmed):
1. [Immediate action] — Effort: [X hrs] — Timeline: [X weeks] — Impact: [High/Med]
2. [action] — Effort: — Timeline: — Impact:
3. [action]

AI VISIBILITY IMPACT: [Is site appearing in AI Overviews / Perplexity / ChatGPT?]
```

---

## Handoff

Write output to `{AUDIT_DIR}/penalty-findings.md`.

**If penalty confirmed:** Flag immediately — all other phases are secondary until resolved. Include recovery roadmap with realistic timelines.

**If clean:** Note clean status — proceed with remaining phases. Include any mild risk factors as preventive actions.

**Key consumers:** `audit/technical-seo` (links to technical issues), `strategy/backlink-audit` (link profile detail), `output/report-generation` (master report integration).
