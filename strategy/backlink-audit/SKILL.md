---
name: backlink-audit
description: >
  Backlink and link profile analysis. Activates when discussing backlinks,
  link building, referring domains, anchor text distribution, toxic links, link
  gaps, digital PR, off-page authority, or link acquisition strategy.
  Phase 12. Output: {AUDIT_DIR}/backlink-findings.md
---

# Backlink & Link Profile Audit — Phase 12

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — business name, URL, location, industry.
Read `{AUDIT_DIR}/competitor-profiles.md` — competitor authority benchmarks.
Read `{AUDIT_DIR}/technical-findings.md` — redirect issues affecting link equity.

**Tools for this phase:**
| Tool | Purpose | Cost |
|------|---------|------|
| **Ahrefs** | Referring domains, DR, anchor text distribution, link history, content gap | Paid |
| **SEMrush** | Backlink Audit (Toxic Score), Link Building Tool, Backlink Gap | Paid |
| **Majestic** | Trust Flow (TF) / Citation Flow (CF) ratio — quality vs. quantity signal | Paid/Free |
| **Moz Link Explorer** | Domain Authority, Spam Score, link profile overview | Paid/Free (limited) |
| **Google Search Console** | Top linking sites, anchor text, disavow file management | Free (requires access) |
| **Bing Webmaster Tools** | Comprehensive inbound link data — often shows links GSC misses | Free |
| **OpenLinkProfiler** | Free link analysis up to 200K links | Free |

**2025 Link Building Context:**
Google's Helpful Content System (March 2024) reduced the value of thin, low-traffic links while increasing the weight of editorial, topical-relevance links. AI Overviews cite topically authoritative domains — earning topical links from local news and industry publications now doubles as both ranking signal AND AIO citation trigger.

---

## Section 1: Current Link Profile Overview

Pull data from **Ahrefs** (Site Explorer → Overview) and **GSC** (Links report):

| Metric | Client | Industry Avg | Comp 1 | Comp 2 | Gap |
|--------|--------|-------------|--------|--------|-----|
| Total referring domains | | | | | |
| Total backlinks | | | | | |
| Dofollow referring domains | | | | | |
| Nofollow referring domains | | | | | |
| Domain Rating / DA | | | | | |
| Majestic Trust Flow (TF) | | | | | |
| Majestic Citation Flow (CF) | | | | | |
| TF:CF ratio (target ≥0.5) | | | | | |
| Link velocity (new RDs/month) | | | | | |
| % links from niche-relevant sites | | | | | |

**TF:CF ratio interpretation:**
- ≥0.5: Healthy profile (quality ≥ quantity)
- 0.3–0.49: Caution — some spammy links
- <0.3: ❌ Risk — likely toxic links depressing Trust Flow

### Link Type Distribution (from Ahrefs → Backlinks → filter by Type)
| Type | Count | % | SEO Value |
|------|-------|---|-----------|
| Editorial (in-content, earned) | | | High |
| Directory listings | | | Medium |
| Social profiles | | | Low-Medium |
| Forum / comment links | | | Low |
| Press releases / news citations | | | High |
| Guest posts | | | Medium-High |
| Sponsorships / events | | | Medium |
| Sitewide footer/sidebar | | | Low |
| Unknown / misc | | | Unknown |

---

## Section 2: Anchor Text Distribution

Over-optimized anchor text = unnatural link pattern = algorithmic penalty risk.

Use **Ahrefs** → Site Explorer → Anchors:

| Anchor Type | Current % | Healthy Target | Status |
|------------|-----------|---------------|--------|
| Brand name (exact: "Acme Plumbing") | % | 40–55% | |
| Domain URL (acmeplumbing.com) | % | 20–30% | |
| Generic ("click here", "this site", "website") | % | 10–15% | |
| Exact-match keyword ("chicago plumber") | % | <10% — ❌ if >15% | |
| Partial-match keyword ("best plumber near me") | % | <10% | |
| Brand + keyword ("Acme Plumbing Chicago") | % | <10% (natural) | |
| Naked URL (https://...) | % | <5% | |
| Other / compound | % | Remainder | |

**Red flags:**
- Exact-match commercial anchor >15% → likely manual or algorithmic penalty risk
- Sudden anchor shift in last 90 days → may indicate purchased links
- Zero brand anchors → link profile artificially optimized → unnatural

---

## Section 3: Link Quality Assessment

For top 50 referring domains (Ahrefs → Top 100 Referring Domains → sort by DR):

| Domain | DR/TF | Relevance | Link Type | Dofollow? | Traffic? | Value |
|--------|-------|-----------|-----------|----------|---------|-------|
| [domain] | | High/Med/Low | Editorial/Dir | ✅/❌ | Yes/No | High/Med/Low |

**Quality signals checklist (assess each top domain):**
- Niche relevant (local, industry, or geographic)?
- Editorial placement (in-content link, not sitewide footer)?
- Linking page has real traffic (check Ahrefs → Referring pages → Traffic filter)?
- Site is indexed and ranking in Google (not deindexed)?
- Link from article/content page, not link-farm directory?

### Top 10 Most Valuable Links
| Referring Domain | DR | Linked Page | Anchor | Editorial? | Acquired How? |
|----------------|----|-----------|----|-----------|-------------|
| [domain] | | [page] | [anchor] | Yes/No | |

---

## Section 4: Toxic Link Assessment

Use **SEMrush Backlink Audit** (Toxic Score) and **Majestic** (TF:CF) to identify risk:

| Toxic Pattern | Risk Level | Detection | Count | Action |
|--------------|-----------|----------|-------|--------|
| PBN networks (sites existing only to sell links) | Critical | Ahrefs → Links from same IP blocks | | Disavow |
| Foreign gambling/pharma spam | Critical | Anchor text analysis | | Disavow |
| Link farms (1000s of outbound links) | High | Majestic CF >> TF | | Disavow |
| Auto-generated spun content sites | High | Low TF, high CF, random content | | Disavow |
| Comment spam (at scale) | Medium | Blog comment pattern | | Disavow |
| Exact-match anchor overdose | High | Anchor distribution | | Monitor |
| Links from deindexed sites | High | `site:domain.com` returns nothing | | Disavow |
| Sitewide links from unrelated sites | Medium | Ahrefs link type filter | | Evaluate |

### Disavow File Status
- Disavow file exists in GSC? Last updated: [date]
- New toxic links appearing after last disavow? [Yes/No — list new ones]
- Current Google stance (2024): Google ignores most low-quality links automatically — **only disavow confirmed manual-action-level toxicity or sudden large-scale spam link attacks**

---

## Section 5: Competitor Link Gap Analysis

Use **Ahrefs Content Gap** (switch to "Backlinks" mode) or **SEMrush Backlink Gap**:

### Competitor Profile Comparison
| Metric | Client | Comp 1 | Comp 2 | Comp 3 | Gap to Leader |
|--------|--------|--------|--------|--------|--------------|
| Referring domains | | | | | |
| Average RD Domain Rating | | | | | |
| Local/niche relevant RDs | | | | | |
| Links from local news | | | | | |
| Industry directory links | | | | | |
| Link velocity (RDs/month) | | | | | |

### Common Links (All Competitors Have, Client Doesn't)
These are minimum table-stakes links client must acquire:
| Site | Why It Matters | How to Get It | Effort |
|------|--------------|--------------|--------|
| BBB (bbb.org) — DA 90 | Trust signal, AIO citation | Membership application | 1 hr, $X/yr |
| Chamber of Commerce | DA 60+, local relevance | Membership | 1–2 hrs |
| [Local newspaper].com | High-trust local editorial | Pitch news angle | 2–4 hrs |
| [Industry directory] | Niche relevance | Listing submission | 30 min |

### Unique Competitor Links (Competitor Advantages)
| Competitor | Unique High-Value Link | How Earned | Replication Strategy |
|-----------|----------------------|-----------|---------------------|
| Comp 1 | [authoritative site] | [article/sponsorship] | [strategy] |
| Comp 2 | [local news piece] | [newsworthy event] | [pitch angle] |

---

## Section 6: Link Building Opportunities

### Priority Categories (Local Business Focus)

**1. Local Authority Links (Highest Impact per effort)**
| Opportunity | Target DA | Effort | Timeline | Priority |
|------------|---------|--------|---------|---------|
| Chamber of Commerce | 60–70 | 1–2 hrs | Week 1 | 5×5=25 |
| BBB membership | 90 | 1 hr | Week 1 | 5×5=25 |
| City government vendor directory | 70–80 | 1 hr | Week 1 | 5×5=25 |
| Local business association | 50–60 | 2–4 hrs | Week 2 | 4×5=20 |
| Local newspaper feature | 60–80 | 4–8 hrs | Month 1 | 5×3=15 |

**2. Industry Directory Links**
Use Whitespark Citation Finder to identify top 10 industry directories:
| Directory | Niche | DA | Listed? | Action |
|----------|-------|-----|---------|--------|
| [Angi/HomeAdvisor] | Home services | 80 | Yes/No | Submit |
| [Houzz] | Home/decor | 90 | Yes/No | Submit |
| [Thumbtack] | Services | 75 | Yes/No | Submit |

**3. Digital PR (Link-Earning Content)**
| Angle | Target Publications | Links Expected | Effort |
|-------|-------------------|---------------|--------|
| Local statistics: "[X%] of [city] homeowners..." | Local news, [City] magazine | 3–8 links | 8–16 hrs |
| Expert commentary for local journalists | Local TV/newspaper | 2–5 links | 2–4 hrs |
| Community sponsorship (charity, little league) | Event + local coverage | 2–4 links | $X + 2 hrs |
| Original local market research | Industry publications | 5–15 links | 20–40 hrs |

**4. Unlinked Brand Mentions**
Search `"[Business Name]" -site:[domain]` in Google and Ahrefs Alerts:
- List any site mentioning the brand without linking
- Outreach template: "Thank you for mentioning us — could you add a link?"
- Conversion rate: ~15–20% of unlinked mentions become links with outreach

**5. Broken Link Building**
- Use Ahrefs → Broken Links → filter for local or industry resource pages
- Find dead competitor links → create equivalent content → pitch as replacement
- Effort: 1–2 hrs per target | Expected: 1 link per 5–10 outreach emails

---

## Section 7: Link Velocity & History

From Ahrefs → New/Lost Referring Domains → chart view:

| Period | New RDs | Lost RDs | Net | Interpretation |
|--------|---------|---------|-----|---------------|
| Last 30 days | | | | |
| 31–60 days ago | | | | |
| 61–90 days ago | | | | |
| 6 months ago | | | | |

**Flags:**
- Sudden +500% spike in 30 days: possible purchased links — investigate
- Steady RD loss: links from deleted pages or site restructuring — recover lost links
- Zero velocity for 3+ months: no link building activity — opportunity

---

## Section 8: Internal Link Equity Distribution

External authority distributes through internal links. Cross-reference `{AUDIT_DIR}/technical-findings.md`:

- Homepage (most externally linked) → does it pass PageRank to key service pages via internal links?
- Key service pages: adequate internal links (target ≥3 internal links each)?
- Deep pages (depth >3): getting authority from internal link structure?

Run Ahrefs → Site Explorer → Pages → filter by Internal Links count — flag pages with 0 or 1 internal link.

---

## Priority Matrix

| Action | Impact (1–5) | Feasibility (1–5) | Priority | Effort |
|--------|-------------|-------------------|---------|--------|
| BBB membership (DA 90 link) | 4 | 5 | 20 | 1 hr |
| Chamber of Commerce join | 4 | 5 | 20 | 1–2 hrs |
| City government vendor directory | 4 | 5 | 20 | 1 hr |
| Unlinked mention outreach | 3 | 5 | 15 | 30 min/mention |
| Industry directory submissions | 3 | 5 | 15 | 30 min each |
| Local newspaper pitch | 5 | 3 | 15 | 4–8 hrs |
| Digital PR original research | 5 | 2 | 10 | 20–40 hrs |
| Disavow toxic links (if confirmed) | 4 | 4 | 16 | 2–4 hrs |

---

## Scoring

| Category | Weight | Score |
|----------|--------|-------|
| Referring domain count vs. competitors | 20% | /20 |
| Link quality (TF:CF ≥0.5, editorial, niche-relevant) | 30% | /30 |
| Anchor text distribution (natural — brand dominant) | 20% | /20 |
| No toxic/manipulative links | 15% | /15 |
| Link velocity (consistent monthly growth) | 15% | /15 |

**Veto:** Confirmed manual action for unnatural links → maximum 40/100 until resolved.

---

## Output

Write to `{AUDIT_DIR}/backlink-findings.md` with YAML frontmatter:

```yaml
---
skill: strategy/backlink-audit
phase: 12
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
referring_domains: [X]
domain_rating: [X]
tf_cf_ratio: [X.X]
toxic_links_found: [yes|no|count]
---
```

Include:
- Score X/100 with per-category breakdown
- Profile overview metrics table (client vs. 3 competitors)
- Anchor text distribution analysis vs. healthy targets
- Top 10 most valuable links
- Toxic link list (with disavow recommendations)
- Competitor link gap analysis (common links client is missing)
- Link opportunity list by category (priority matrix scored)
- Link velocity/history chart summary
- 30/90/180-day link building plan

**Key consumers:**
- `audit/penalty-check` — reads for toxic link and anchor text signals
- `cross-cutting/serp-trust-auditor` — Off-Page Authority dimension
- `output/report-generation` — backlink score in master report section 12
