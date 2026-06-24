---
title: "Google AI Overviews (AIO)"
type: concept
tags: [seo, google, ai-search, aio, geo, content-structure]
created: 2026-06-10
updated: 2026-06-10
sources: [Central_RAG_Document_Enhanced_v2]
---

# Google AI Overviews (AIO)

Google's AI-generated summary boxes that appear at the top of search results pages, above organic rankings. Optimising for AIO is critical for [[wildnet-edge]] content because AIO citations drive brand visibility and topical authority — especially in B2B technology, where AIO appears on **70% of queries**.

## Key Data (2025–2026)

| Metric | Value | Source |
|--------|-------|--------|
| AIO appearance rate (all US queries) | 25.8% | Semrush/Stackmatix 2026 |
| AIO rate for informational queries | 39.4% | Stackmatix 2026 |
| AIO rate for B2B technology queries | **70%** | SingleGrain 2025 |
| AIO rate for long-tail (7+ word queries) | 65.9% | DataSlayer Sep 2025 |
| % AIO citations from top 30% of page | 44% | SEO Sherpa 2025 |
| % AIO citations from content < 2 years old | 85% | Semrush 2025 |
| Avg sources cited per AIO | 4–8 | Semrush AIO Study 2025 |
| % queries where #1 organic rank appears in AIO | ~72% | First Page Sage 2026 |

## The Answer Capsule Framework

Every major H2/H3 section should be formatted as an **answer capsule** — a self-contained extractable unit:

1. **Question-form heading** — mirrors the user query: "How does X work?" not "Overview of X"
2. **1–2 sentence direct answer immediately beneath** — this is what AIO extracts
3. **2–5 supporting bullet points** — evidence, context, or nuance
4. **One cited statistic with named source** — fact density increases extraction probability
5. *(Optional)* "Why this is true" or "How we know this" sub-paragraph

## Structural Requirements for AIO Eligibility

- **Answer-first architecture:** 44% of citations come from the first 30% of a page — put direct answers before context
- **Question-based headings:** H2s and H3s should mirror user queries
- **Short paragraphs:** max 2–3 sentences — LLMs extract clean, bounded chunks
- **FAQ sections:** marked up with FAQPage schema; place at end of page; target voice/conversational queries
- **How-to structure:** numbered steps (3–7 ideal); marked up with HowTo schema
- **Comparative content:** "X vs Y" sections and numbered rankings are frequently extracted

## Technical Requirements

- Allow Googlebot-Extended in robots.txt
- Server-side rendering (SSR) — JavaScript-only rendered content may not be processed for AIO
- Core Web Vitals in "Good" range: LCP < 2.5s, INP < 200ms, CLS < 0.1
- Schema: Organization, Article, Author, FAQPage, HowTo, ImageObject
- Internal linking from authoritative hub pages
- Backlinks from at least 3–5 authoritative referring domains
- Content freshness: update annually minimum; quarterly for fast-moving topics

## Anti-Patterns (What NOT to Do)

- **Snippet bait:** Punchy 2-sentence answer at top, thin explanation beneath — AIO systems detect this
- **Blocking AI crawlers** in robots.txt — never block GPTBot, ClaudeBot, PerplexityBot, Google-Extended
- **Keyword stuffing** — Princeton GEO Study (2024) found this performs *worse* in LLM citation tests
- **No citations** — unsourced claims are penalised in [[e-e-a-t]] evaluation
- **Raw AI content** — unedited AI output without expert oversight won't rank or get cited consistently

## Sources

- [[2026-06-10-central-rag-document]]
