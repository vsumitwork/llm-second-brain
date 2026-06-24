---
title: "Content Scoring Rubric"
type: concept
tags: [content-quality, scoring, seo, publishing-standard]
created: 2026-06-10
updated: 2026-06-10
sources: [Central_RAG_Document_Enhanced_v2]
---

# Content Scoring Rubric

The 100-point scale used to evaluate all content before publishing. Source: [[central-rag-document]] Section 7. **Minimum score to publish: 75.** Score 90+ = ready to publish with high confidence of ranking and LLM citation.

## Score Tiers

| Score | Label | Action |
|-------|-------|--------|
| 90–100 | Excellent | Publish and monitor |
| 75–89 | Good | Fix minor E-E-A-T or schema gaps first |
| 60–74 | Average | Targeted rewrite of weak sections |
| 40–59 | Poor | Major rewrites; re-evaluate keyword strategy |
| 0–39 | Failing | Full replacement required |

## Score Breakdown (100 Points)

| Category | Max Points | Sub-Categories |
|----------|-----------|----------------|
| [[e-e-a-t]] Signals | 25 | Experience (8) + Expertise (7) + Authoritativeness (5) + Trust (5) |
| Content Quality & Structure | 20 | Depth (5) + Originality (5) + Formatting (5) + Answer-first (5) |
| Keyword & Search Intent | 15 | Keyword usage (5) + Intent alignment (5) + Semantic coverage (5) |
| LLM/AI Visibility | 15 | [[geo-llm-visibility]] structure (5) + [[schema-markup]] (5) + AI-bot access + entity (5) |
| Page-Type Best Practices | 15 | Page-type compliance (10) + Conversion elements (5) |
| Technical Baseline | 10 | Core Web Vitals (3) + Tags/structure (4) + Crawlability (3) |

## Detailed E-E-A-T Scoring (25 Points)

| Signal | Max | Criteria |
|--------|-----|----------|
| First-hand experience demonstrated | 4 | 4=original data/screenshot; 2=anecdotal; 0=none |
| Named author with relevant bio | 4 | 4=full bio+credentials+photo; 2=name only; 0=none |
| Author credentials match topic | 3 | 3=directly relevant; 2=adjacent; 0=missing |
| External citations (credible sources) | 3 | 3=3+ high-DA; 2=1-2 sources; 0=none |
| Content freshness (< 12 months) | 3 | 3=< 6 months; 2=6-18 months; 0=> 18 months |
| Schema markup (Author, Article, Org) | 3 | 3=all types; 2=partial; 0=missing |
| Trust signals (HTTPS, contact, privacy) | 3 | 3=all present; 2=some; 0=missing HTTPS |
| Consistent entity information | 2 | 2=fully consistent; 0=inconsistencies found |

## Technical Baseline (Must-Pass Before Content Scoring)

Technical failures act as a **ceiling** on overall score — fix these before content scoring:

| Check | Requirement |
|-------|-------------|
| HTTPS | Non-negotiable — critical trust penalty if missing |
| LCP | < 2.5 seconds |
| INP | < 200ms |
| CLS | < 0.1 |
| Title Tag | 50–60 characters, primary keyword included |
| Meta Description | 150–160 characters, CTA + keyword |
| H1 Tag | Exactly one per page, contains primary keyword |
| URL | Clean, lowercase, hyphenated, keyword, < 75 chars |
| Internal Links | Minimum 2–3 contextual links |
| Schema | Minimum: Organization + page-specific type |
| robots.txt | GPTBot, ClaudeBot, PerplexityBot, Google-Extended allowed |

## WildnetEdge Scorecard Minimums (from [[wildnatedge-writing-standards]])

| Content Type | Min Avg (of 5) |
|---|---|
| Service Pages | 4.0 |
| Blogs | 4.0 |
| Website Pages | 3.5 |
| Social | 3.5 |

## Sources

- [[2026-06-10-central-rag-document]]
- [[2026-06-10-wildnatedge-writing-guide]]
