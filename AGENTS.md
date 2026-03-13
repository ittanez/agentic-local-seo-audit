# Sub-Agents

The Local SEO Audit System uses 6 specialized sub-agents for parallel audit execution. Claude spawns these automatically when running a full audit to process multiple phases simultaneously.

## Agent Overview

```
┌──────────────────────────────────────────────────────────┐
│                   ORCHESTRATOR (Claude)                    │
│                                                           │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐        │
│  │  Technical   │ │   Content   │ │   Keyword   │        │
│  │  Analyst     │ │   Analyst   │ │   Analyst   │        │
│  └─────────────┘ └─────────────┘ └─────────────┘        │
│                                                           │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐        │
│  │ Local SEO   │ │AI Visibility│ │  Off-Page   │        │
│  │  Analyst    │ │  Analyst    │ │   Analyst   │        │
│  └─────────────┘ └─────────────┘ └─────────────┘        │
└──────────────────────────────────────────────────────────┘
```

## Agent Specifications

### 1. Technical Analyst
- **File**: `agents/technical-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 2 (Technical SEO), Phase 10 (Speed), Phase 19 (Accessibility)
- **Tools**: WebSearch, WebFetch, Bash
- **Output**: Technical issue checklist with status/impact/fix/effort per item

### 2. Content Analyst
- **File**: `agents/content-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 4 (Content), Phase 5 (Content Gaps), Phase 7 (Topical Gaps), Phase 8 (Authority)
- **Tools**: WebSearch, WebFetch
- **Output**: Content inventory, gap tables, topical map, authority scores

### 3. Keyword Analyst
- **File**: `agents/keyword-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 3 (On-Page), Phase 6 (Keywords), Phase 9 (Entities)
- **Tools**: WebSearch, WebFetch
- **Output**: Keyword gap tables, on-page checklists, entity matrices

### 4. Local SEO Analyst
- **File**: `agents/local-seo-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 11 (Local SEO), Phase 15 (Reputation), Phase 21 (Multi-Location)
- **Tools**: WebSearch, WebFetch
- **Output**: GBP audit, review analysis, citation audit, local SERP rankings

### 5. AI Visibility Analyst
- **File**: `agents/ai-visibility-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 14 (AI SEO), Phase 16 (Brand SERP), Phase 18 (Voice Search)
- **Tools**: WebSearch, WebFetch
- **Output**: AI visibility comparison table, brand SERP inventory, voice readiness checklist

### 6. Off-Page Analyst
- **File**: `agents/offpage-analyst.md`
- **Model**: claude-sonnet-4-6
- **Handles**: Phase 12 (Backlinks), Phase 13 (Social), Phase 17 (UX/CRO)
- **Tools**: WebSearch, WebFetch
- **Output**: Link profile comparison, social scorecard, CRO checklist

## Inter-Agent Handoff Protocol

When agents complete their phases, they pass context back to the orchestrator:

| Context | Format | Example |
|---------|--------|---------|
| Phase scores | `{phase}: {score}/100` | `Technical SEO: 62/100` |
| Critical issues | `[CRITICAL] {issue} — {phase}` | `[CRITICAL] No XML sitemap — Technical SEO` |
| Quick wins | `[QUICKWIN] {action} — {effort}` | `[QUICKWIN] Add alt text to 12 images — 1hr` |
| Competitor data | `{competitor}: {dimension} {score}` | `CompetitorA: Reviews 4.8/5 (142 reviews)` |
| LOCAL-IMPACT items | `{code}{number}: {score}/3` | `L01: 2/3 (GBP claimed but incomplete)` |
| SERP-TRUST items | `{code}{number}: {score}/4` | `T05: 3/4 (Schema present, missing FAQ)` |

## Parallel Execution Pattern

During a full audit, agents run in two waves:

**Wave 1** (Foundation):
- Technical Analyst → Technical SEO + Speed
- Local SEO Analyst → GBP + Reviews + Citations
- Keyword Analyst → On-Page + Keywords

**Wave 2** (After Wave 1 context available):
- Content Analyst → Content + Gaps + Authority
- AI Visibility Analyst → AI SEO + Brand SERP + Voice
- Off-Page Analyst → Backlinks + Social + CRO

The orchestrator compiles all agent outputs into the master report and scoring frameworks.
