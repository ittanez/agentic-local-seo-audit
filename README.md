# Local SEO Audit System

A comprehensive 21-phase local business SEO audit plugin for Claude Code. Performs deep competitive analysis, technical SEO, content strategy, AI visibility optimization, and produces prioritized action plans.

## Features

- **21 Audit Phases** covering every dimension of local SEO
- **24 Skills** that activate automatically based on context
- **36 Slash Commands** for targeted audit phases and utility tools
- **6 Sub-Agents** for parallel audit execution
- **Competitor Analysis** across 9 dimensions with scoring
- **AI Visibility Auditing** — AI Overviews, ChatGPT, Perplexity, Gemini, Claude, Copilot
- **Content, Keyword & Topical Gap Analysis** with prioritized roadmaps
- **Schema Markup Generator** — ready-to-paste JSON-LD for local businesses
- **GBP Optimization Toolkit** — descriptions, posts, Q&A, photo lists
- **Master Report Compiler** with 30/90/180/365-day action plans
- **Quality Gates** ensuring every recommendation is specific, actionable, and prioritized

## Installation

### From Claude Marketplace

```bash
claude plugin install local-seo-audit
```

### From GitHub

```bash
claude plugin install local-seo-audit@mshahiddigital
```

### Manual / Local Testing

```bash
git clone https://github.com/mshahiddigital/local-seo-audit.git
claude --plugin-dir ./local-seo-audit
```

### Scope Options

```bash
# Available everywhere (default)
claude plugin install local-seo-audit --scope user

# Project-specific (shared via git)
claude plugin install local-seo-audit --scope project

# Local only (gitignored)
claude plugin install local-seo-audit --scope local
```

## Quick Start

### Full 21-Phase Audit

```
/local-seo-audit:seo-audit https://example.com
```

This triggers the complete audit workflow:
1. Collects business information via intake form
2. Runs competitor analysis + penalty check
3. Proceeds through all 21 phases
4. Compiles a master audit report with prioritized action plans

### Quick Health Check (5 Phases)

```
/local-seo-audit:quick-audit https://example.com
```

Covers Technical SEO, On-Page, Local SEO, Speed, and AI Visibility. Produces a 1-page summary with top 10 action items.

## All Commands

### Audit Triggers

| Command | Description |
|---------|-------------|
| `/local-seo-audit:seo-audit [url]` | Full 21-phase audit |
| `/local-seo-audit:quick-audit [url]` | Fast 5-phase health check |
| `/local-seo-audit:audit-intake` | Start intake form |

### Phase Commands

| Command | Phase | Description |
|---------|-------|-------------|
| `/local-seo-audit:audit-competitors [urls]` | 1 | Competitor deep analysis |
| `/local-seo-audit:audit-technical [url]` | 2 | Technical SEO audit |
| `/local-seo-audit:audit-onpage [url]` | 3 | On-page SEO audit |
| `/local-seo-audit:audit-content [url]` | 4 | Content audit |
| `/local-seo-audit:audit-content-gaps [url]` | 5 | Content gap analysis |
| `/local-seo-audit:audit-keywords [url]` | 6 | Keyword gap analysis |
| `/local-seo-audit:audit-topical-gaps [url]` | 7 | Topical map & gaps |
| `/local-seo-audit:audit-authority [url]` | 8 | Topical authority |
| `/local-seo-audit:audit-entities [url]` | 9 | Entity audit |
| `/local-seo-audit:audit-speed [url]` | 10 | Core Web Vitals & speed |
| `/local-seo-audit:audit-local [url]` | 11 | Local SEO & GBP |
| `/local-seo-audit:audit-backlinks [url]` | 12 | Backlink profile |
| `/local-seo-audit:audit-social [url]` | 13 | Social media |
| `/local-seo-audit:audit-ai-seo [url]` | 14 | AI visibility |
| `/local-seo-audit:audit-reputation [url]` | 15 | Reputation & reviews |
| `/local-seo-audit:audit-brand-serp [url]` | 16 | Brand SERP |
| `/local-seo-audit:audit-cro [url]` | 17 | UX & CRO |
| `/local-seo-audit:audit-voice [url]` | 18 | Voice search |
| `/local-seo-audit:audit-accessibility [url]` | 19 | Accessibility |
| `/local-seo-audit:audit-penalty [url]` | 20 | Penalty check |
| `/local-seo-audit:audit-multi-location [url]` | 21 | Multi-location |

### Utility Commands

| Command | Description |
|---------|-------------|
| `/local-seo-audit:audit-report` | Compile master audit report |
| `/local-seo-audit:audit-quick-wins` | Extract all quick wins |
| `/local-seo-audit:audit-action-plan [30d\|90d\|6m\|12m]` | Prioritized action plan |
| `/local-seo-audit:audit-compare [url]` | Client vs competitor comparison |
| `/local-seo-audit:audit-status` | Show audit progress |
| `/local-seo-audit:topical-map [niche]` | Build topical authority map |
| `/local-seo-audit:keyword-map` | Keyword-to-page mapping |
| `/local-seo-audit:schema-generator [url] [type]` | Generate JSON-LD schema |
| `/local-seo-audit:content-brief [keyword]` | SEO content brief |
| `/local-seo-audit:gbp-optimize [business]` | GBP optimization toolkit |
| `/local-seo-audit:citation-list [category] [location]` | Citation building list |
| `/local-seo-audit:ai-visibility-check [business] [location]` | AI platform visibility check |

## Skills (Auto-Activated)

Skills activate automatically when Claude detects relevant context. No manual invocation needed.

| Skill | Activates For |
|-------|---------------|
| `seo-audit-identity` | Any SEO audit discussion |
| `audit-intake` | Starting an audit, providing URLs |
| `competitor-analysis` | Competitive research |
| `technical-seo` | Crawlability, indexation, schema, redirects |
| `onpage-seo` | Title tags, meta descriptions, headers, content |
| `content-audit` | Content quality, thin content, duplicates |
| `content-gaps` | Missing content opportunities |
| `keyword-gaps` | Keyword research, ranking opportunities |
| `topical-gaps` | Topic mapping, cluster completeness |
| `topical-authority` | Authority building, expertise signals |
| `entity-audit` | Knowledge Graph, entities, schema |
| `speed-optimization` | CWV, LCP, INP, CLS, performance |
| `local-seo` | GBP, citations, NAP, reviews, local pack |
| `backlink-audit` | Link profile, link building, toxic links |
| `social-media-audit` | Social profiles, engagement, Open Graph |
| `ai-seo` | AI Overviews, AEO, GEO, LLM visibility |
| `reputation-audit` | Reviews, sentiment, brand reputation |
| `brand-serp` | Branded search, Knowledge Panel |
| `ux-cro-audit` | Conversion paths, analytics, UX |
| `voice-search` | Voice queries, conversational content |
| `accessibility-audit` | WCAG, ADA, heading hierarchy, alt text |
| `penalty-check` | Manual actions, algorithm penalties |
| `multi-location-seo` | Multi-location GBP, geo-siloing |
| `report-generation` | Compiling audit reports, action plans |

## Sub-Agents

Claude spawns specialized agents for parallel audit execution:

| Agent | Handles |
|-------|---------|
| `technical-analyst` | Technical SEO + Speed + Accessibility |
| `content-analyst` | Content + Gaps + Topical Authority |
| `keyword-analyst` | Keywords + On-Page + Entities |
| `local-seo-analyst` | Local SEO + Reviews + Multi-location |
| `ai-visibility-analyst` | AI SEO + Brand SERP + Voice |
| `offpage-analyst` | Backlinks + Social + CRO |

## MCP Connectors

The plugin includes connector configs for external data sources. Update `.mcp.json` with your actual server URLs:

- **Google Search Console** — queries, pages, coverage, CWV
- **Google Analytics (GA4)** — traffic, conversions, events
- **Google Business Profile** — reviews, insights, posts
- **PageSpeed Insights** — CWV performance data
- **SimilarWeb** — competitor traffic and keyword data

## Output Format

Every audit phase produces structured output with:

- Status indicators: Pass / Warning / Fail
- Impact levels: Critical / High / Medium / Low
- Priority scoring: Impact (1-5) x Feasibility (1-5)
- Specific fix steps with effort estimates
- Competitor comparison context
- Estimated timeline: Immediate / This Week / This Month / Next Quarter

The master report includes:
- Overall health score (X/100)
- Priority action matrix
- Quick wins checklist
- 30-day, 90-day, 6-month, and 12-month roadmaps
- KPI tracking framework
- Resource and budget recommendations

## Requirements

- Claude Code v1.0.33 or later
- Web search and web fetch permissions enabled

## Configuration

After installation, the plugin works out of the box. For MCP integrations, update `.mcp.json` with your actual server endpoints.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-audit-phase`)
3. Commit your changes (`git commit -m 'Add new audit phase'`)
4. Push to the branch (`git push origin feature/new-audit-phase`)
5. Open a Pull Request

## License

MIT - see [LICENSE](LICENSE) for details.

## Support

- Issues: [GitHub Issues](https://github.com/mshahiddigital/local-seo-audit/issues)
- Discussions: [GitHub Discussions](https://github.com/mshahiddigital/local-seo-audit/discussions)
