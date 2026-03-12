---
name: technical-seo
description: >
  Complete technical SEO audit expertise. Activates for any technical SEO
  discussion: crawlability, indexation, site architecture, redirects,
  canonicals, structured data, HTTPS, hreflang, JavaScript rendering,
  robots.txt, XML sitemaps, or site infrastructure analysis.
---

# Technical SEO Audit Framework

## Audit Checklist

### Crawlability & Indexation
- Robots.txt analysis (blocking critical resources? correct directives?)
- XML Sitemap (exists? submitted? accurate? auto-updated? includes all important URLs?)
- Index coverage (indexed vs. submitted vs. expected)
- Crawl budget (URL parameters? calendar pages? faceted nav? session IDs?)
- Orphan pages (zero internal links pointing to them)
- Crawl depth (critical pages > 3 clicks from homepage?)
- Noindex/nofollow (important pages accidentally blocked?)
- JavaScript rendering (content visible without JS? SSR/SSG?)
- Soft 404s (200 status but error/thin content)
- Crawl traps (infinite pagination, calendar URLs, search URLs)

### Site Architecture & URL Structure
- Clean, descriptive, keyword-inclusive URLs
- Logical hierarchy (max 3 levels for important pages)
- Breadcrumbs (present, schema-marked, functional)
- Pagination handling, faceted navigation management

### HTTPS & Security
- SSL validity, mixed content, HTTP→HTTPS redirect, HSTS, security headers

### Redirect Management
- Chains (flatten to single hop), loops, 301 vs 302, old URL handling

### Canonical Tags
- Self-referencing, cross-domain, conflict detection, pagination handling

### Structured Data / Schema
Required for local businesses:
- LocalBusiness (complete with all properties)
- Organization, BreadcrumbList, Service, FAQ, HowTo
- Article/BlogPosting, Review/AggregateRating, VideoObject
- Event, Product (if applicable), Person (team pages)
- sameAs linking all official profiles
- Validate with Rich Results Test — zero errors

## Per-Item Output Format
Status: ✅ Pass | ⚠️ Warning | ❌ Fail
Issue: [Description]
Impact: Critical | High | Medium | Low
Fix: [Exact steps]
Priority: Immediate | This Week | This Month | Next Quarter
Effort: Quick Fix (<1hr) | Medium (1-4hrs) | Complex (4+hrs)
