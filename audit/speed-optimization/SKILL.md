---
name: speed-optimization
description: >
  Performance and Core Web Vitals expertise. Activates when discussing page
  speed, Core Web Vitals, LCP, INP, CLS, TTFB, FCP, performance optimization,
  image compression, JavaScript optimization, or site speed issues.
  Phase 10. Output: {AUDIT_DIR}/speed-findings.md
---

# Core Web Vitals & Speed Audit — Phase 10

## Executive Summary

Core Web Vitals are confirmed Google ranking signals. In 2025, INP (replaced FID March 2024) is the hardest CWV metric to pass — only ~65% of sites meet Good threshold (Cloudflare 2025). Pages with all CWV in "Good" range see average 15–25% CTR improvement (Google CrUX 2024). Speed directly impacts conversion: 1-second LCP delay = 20% conversion drop (Portent 2023). Always compare client CWV against top 3 competitors.

---

## Tools for This Phase

| Tool | Purpose | Cost |
|------|---------|------|
| **Google PageSpeed Insights** | CWV scores + diagnostics (mobile + desktop) | Free |
| **Chrome DevTools → Lighthouse** | Lab data with filmstrip, coverage tab | Free |
| **Chrome DevTools → Performance** | INP profiling, main thread analysis | Free |
| **WebPageTest** (webpagetest.org) | Waterfall, filmstrip, multi-location test | Free |
| **GTmetrix** | Performance grade, waterfall, page size, requests | Free/Paid |
| **CrUX (Chrome User Experience Report)** | Real-user field data from CrUX dataset | Free |
| **Cloudflare Speed** (speed.cloudflare.com) | INP + TTFB from Cloudflare edge | Free |
| **DebugBear** | CWV monitoring, regression detection | Paid |
| **site_crawler.py** | Identify image-heavy pages, JS payload size | Free (local) |

---

## Step 1: Read Project Context

Read `{AUDIT_DIR}/intake-data.md` — URL, tech stack (CMS affects optimization options).
Read `{AUDIT_DIR}/technical-findings.md` — any speed-related technical issues already flagged.

---

## Step 2: Baseline CWV Data Collection

### 2025 CWV Thresholds (Updated — INP replaced FID March 2024)

| Metric | Good | Needs Improvement | Poor | Measures |
|--------|------|-------------------|------|----------|
| **LCP** (Largest Contentful Paint) | < 2.5s | 2.5–4.0s | > 4.0s | Perceived load speed |
| **INP** (Interaction to Next Paint) | < 200ms | 200–500ms | > 500ms | Responsiveness to interaction |
| **CLS** (Cumulative Layout Shift) | < 0.1 | 0.1–0.25 | > 0.25 | Visual stability |
| **TTFB** (Time to First Byte) | < 800ms | 800ms–1.8s | > 1.8s | Server responsiveness |
| **FCP** (First Contentful Paint) | < 1.8s | 1.8–3.0s | > 3.0s | Initial render |
| **TBT** (Total Blocking Time) | < 200ms | 200–600ms | > 600ms | Main thread blocking |

**INP scoring guide (2025 priority):**
- < 100ms = Excellent (competitive advantage)
- 100–200ms = Good (meets threshold)
- 200–500ms = Needs Improvement (flag for fixes)
- > 500ms = Poor (critical — likely INP veto trigger)

### Data Collection Protocol

1. **PageSpeed Insights → Mobile** (primary — Google ranks mobile-first):
   ```
   URL: https://pagespeed.web.dev/
   Test: [client URL]
   Record: Performance score, LCP, INP, CLS, TTFB, FCP, TBT
   ```

2. **PageSpeed Insights → Desktop** (secondary benchmark):
   ```
   Record same metrics — gap > 30pts Mobile vs Desktop = mobile-specific issue
   ```

3. **Top 3 Competitors** — test same URL structure (homepage):
   ```
   Record mobile performance scores for competitive benchmark table
   ```

4. **WebPageTest** (real network conditions):
   ```
   Location: nearest city to target audience
   Connection: Mobile 4G LTE
   Run: 3 tests → median result
   Record: TTFB, Start Render, Fully Loaded, Total Page Size, Total Requests
   ```

5. **Field data vs. Lab data check** (PageSpeed "Discover what your real users are experiencing"):
   ```
   CrUX field data available? Compare field vs. lab — large gaps indicate real-user outliers
   ```

---

## Section 1: LCP Optimization

### Identify LCP Element
PageSpeed Insights "Diagnostics" section identifies the LCP element automatically.

**LCP element type → fix strategy:**

| LCP Element Type | Primary Fix | Secondary Fix |
|-----------------|------------|---------------|
| Hero image | Preload + WebP/AVIF + fetchpriority="high" | Serve from CDN |
| H1 text block | Improve TTFB (server/hosting) + self-host fonts | Inline critical CSS |
| Background image (CSS) | Move to `<img>` tag to allow preload | fetchpriority="high" |
| Video thumbnail | Replace with image poster + lazy-load video | Serve from CDN |

### LCP Image Fixes (Most Common — 68% of LCP failures)
```html
<!-- Preload the LCP image in <head> -->
<link rel="preload" as="image" href="hero.webp" fetchpriority="high">

<!-- LCP img tag -->
<img src="hero.webp" width="1200" height="630"
     fetchpriority="high" loading="eager"
     alt="[descriptive alt]">
```

**Image format targets:**
- AVIF: 50–80% smaller than JPEG — ideal for LCP (Chrome + Firefox + Safari 16+)
- WebP: 25–35% smaller than JPEG — broad browser support
- Max LCP image size: ≤ 200KB (above fold, compressed)

### LCP Server Response (TTFB Fix)

If TTFB > 800ms — server is bottleneck:
| Action | Expected TTFB Improvement | Effort |
|--------|--------------------------|--------|
| Add Cloudflare (free tier) | 30–50% reduction | 30 min |
| Enable page caching (WP: WP Rocket/LiteSpeed) | 50–80% reduction | 1–2 hrs |
| Upgrade shared → VPS hosting | 40–70% reduction | 2–4 hrs |
| Move server geographically closer | 20–40% reduction | 4–8 hrs |
| Enable Brotli compression | 10–20% reduction | 30 min |

---

## Section 2: INP Optimization (2025 Priority Signal)

INP measures how quickly a page responds to user interactions (clicks, taps, keyboard input). It's the hardest CWV to fix — requires JavaScript profiling.

### Common INP Culprits

| Culprit | How to Detect | Fix | Effort |
|---------|--------------|-----|--------|
| Long tasks on main thread (>50ms) | Chrome DevTools → Performance → "Long Tasks" | Break with `scheduler.yield()` or `setTimeout(fn, 0)` | 4–16 hrs |
| Third-party scripts (chat, analytics) | DevTools → Performance → filter by domain | Delay load until after user interaction | 1–4 hrs |
| Large JavaScript bundles | DevTools → Coverage tab → unused JS | Code splitting + tree shaking | 8–24 hrs |
| Excessive DOM nodes (>1,500) | DevTools → Performance Insights | Virtualize long lists | 4–16 hrs |
| Unthrottled scroll/resize handlers | DevTools → Performance → Event Listeners | Debounce/throttle + passive listeners | 1–4 hrs |

**INP profiling command (Chrome DevTools):**
1. Open DevTools → Performance tab
2. Click "Record" → perform click/interaction on page → Stop
3. Look for "Interaction" entries in the timeline → identify blocking time

---

## Section 3: CLS Optimization

| Cause | Fix | Effort |
|-------|-----|--------|
| Images without dimensions | Add `width` and `height` to all `<img>` tags | 1–2 hrs |
| Ads / iframes without reserved space | Add `min-height` CSS container before ad loads | 2–4 hrs |
| Web fonts causing FOUT | `font-display: optional` + preload font | 1–2 hrs |
| Late-loading embeds (maps, social) | Use fixed-height skeleton placeholder | 1–4 hrs |
| Dynamically injected content above fold | Reserve space or inject only below fold | 2–8 hrs |
| CSS `animation` not using `transform` | Replace `top/margin` with `transform: translateY()` | 30 min |

---

## Section 4: Image Optimization (Highest ROI Area)

Image issues cause 60–75% of speed failures on local business sites (Screaming Frog audit data, 2024).

### Image Audit Checklist

From `python3 scripts/site_crawler.py` output + manual check:
- [ ] All above-fold images in WebP or AVIF?
- [ ] Hero/LCP image ≤ 200KB?
- [ ] Below-fold images use `loading="lazy"`?
- [ ] `srcset` defined for responsive images?
- [ ] `width` + `height` attributes on all `<img>` (prevents CLS)?
- [ ] No images served larger than display size (e.g., 2000px image at 400px display)?
- [ ] Images served from CDN (not same server as HTML)?

**Image optimization tools:**
| Tool | Purpose | Cost |
|------|---------|------|
| Squoosh (squoosh.app) | Manual WebP/AVIF conversion | Free |
| ImageOptim (Mac app) | Batch lossless compression | Free |
| TinyPNG API | Automated batch PNG/JPG compression | Free/Paid |
| Cloudinary | On-the-fly optimization + CDN | Free/Paid |
| ShortPixel (WordPress) | Auto-convert + compress on upload | Paid |

---

## Section 5: JavaScript Optimization

**JS budget targets (2025):**
- Total JS payload: < 300KB compressed
- Unused JS: < 20% of total
- Render-blocking scripts in `<head>`: 0 (except critical)
- Third-party scripts: audit any > 50ms INP impact

| Fix | Impact | Effort |
|-----|--------|--------|
| Add `defer` to non-critical scripts | Removes render-blocking | 30 min |
| Delay chat widget to user interaction | -50–200ms INP | 1–2 hrs |
| Code splitting (lazy-load by route) | -30–100KB initial JS | 8–24 hrs |
| Remove unused jQuery plugins | -20–60KB | 1–4 hrs |
| Replace social share buttons with static links | -100–400ms INP | 30 min |

---

## Section 6: Server & Infrastructure

| Check | Good | Flag |
|-------|------|------|
| Hosting type | Cloud/VPS/Managed WordPress | Shared hosting (shared = unpredictable TTFB) |
| CDN | Cloudflare / Fastly / BunnyCDN active | No CDN |
| Browser caching | `Cache-Control: max-age=31536000` for static assets | No cache headers |
| Compression | Brotli (preferred) or GZIP enabled | No compression |
| HTTP version | HTTP/2 or HTTP/3 | HTTP/1.1 (slower) |
| Server location | < 50ms latency to target audience | > 100ms to target city |

---

## Section 7: Competitor Speed Benchmark

| Metric | Client | Comp 1 | Comp 2 | Comp 3 | Target |
|--------|--------|--------|--------|--------|--------|
| Mobile PSI Score | | | | | > 70 |
| LCP (mobile) | | | | | < 2.5s |
| INP (mobile) | | | | | < 200ms |
| CLS (mobile) | | | | | < 0.1 |
| TTFB | | | | | < 800ms |
| Page Size | | | | | < 2MB |

**Competitive insight:** If client's mobile score is ≥ 10 points below top competitor → speed gap is a ranking factor risk.

---

## Section 8: AI Visibility Speed Connection (2025)

AI Overviews (AIO) and voice search results strongly favor fast pages:
- AIO sources pages with LCP < 2.5s at 78% rate vs. 41% for LCP > 4s (SparkToro 2025)
- Voice search results: 97% come from pages with mobile score > 70 (Backlinko 2024)
- PageSpeed is a direct GBP ranking factor for "near me" queries (Google 2024 documentation)

Flag AIO/voice impact when speed issues are found.

---

## Priority Matrix

| Issue | Impact (1–5) | Feasibility (1–5) | Priority | Effort |
|-------|-------------|-------------------|---------|--------|
| LCP > 4s (mobile) | 5 | 4 | 20 | 2–8 hrs |
| INP > 500ms | 5 | 3 | 15 | 4–16 hrs |
| No CDN (TTFB > 1.8s) | 5 | 5 | 25 | 30 min–2 hrs |
| Images not WebP/AVIF | 4 | 5 | 20 | 2–4 hrs |
| CLS > 0.25 | 4 | 4 | 16 | 1–4 hrs |
| Render-blocking JS | 4 | 4 | 16 | 1–4 hrs |
| No browser caching | 3 | 5 | 15 | 30 min |
| Third-party script bloat | 4 | 3 | 12 | 1–4 hrs |
| No GZIP/Brotli | 3 | 5 | 15 | 30 min |

**Veto check:** LCP > 6s on mobile → maximum SERP-TRUST score capped at 30/100.

---

## Output

Write complete findings to `{AUDIT_DIR}/speed-findings.md` with YAML frontmatter:

```yaml
---
skill: audit/speed-optimization
phase: 10
date: [YYYY-MM-DD]
business: [Business Name]
url: [URL]
score: [X/100]
mobile_psi: [X]
desktop_psi: [X]
lcp_mobile: [Xs]
inp_mobile: [Xms]
cls_mobile: [X.XX]
ttfb: [Xms]
cwv_pass: [yes|no|partial]
---
```

Include:
- Score X/100 with per-section breakdown
- CWV baseline table (client vs. 3 competitors)
- LCP element identified + specific fix steps
- INP profiling results + specific scripts causing delay
- CLS causes identified + fixes
- Image audit (page-level — pages with largest images)
- JS payload breakdown (total, unused, render-blocking)
- Server/infrastructure assessment
- Priority matrix (all issues, Impact × Feasibility scored)
- 30-day speed improvement plan (quick wins first)

**Key consumers:**
- `strategy/ux-cro-audit` — speed directly impacts conversion rate (1s delay = 20% drop)
- `cross-cutting/serp-trust-auditor` — User Experience dimension U scores
- `ai-visibility/voice-search` — voice results require mobile score > 70
- `cross-cutting/local-impact-auditor` — Website Performance dimension
