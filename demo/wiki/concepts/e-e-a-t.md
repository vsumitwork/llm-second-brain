---
title: "E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness)"
type: concept
tags: [seo, google, content-quality, ranking-framework, e-e-a-t]
created: 2026-06-10
updated: 2026-06-10
sources: [Central_RAG_Document_Enhanced_v2]
---

# E-E-A-T

Google's four-dimension framework for evaluating whether a page deserves to rank. Defined in Google's Search Quality Rater Guidelines (QRG). **Not a direct algorithmic signal** — it shapes the systems (Helpful Content System, SpamBrain, Panda-successor updates) that suppress or reward content at scale. In the [[content-scoring-rubric]], E-E-A-T accounts for 25 of 100 points.

## The Four Dimensions

### Experience (8/25 points)
First-hand, lived interaction with the topic. Introduced by Google in 2022 to distinguish content written by someone who has **actually done the thing** versus assembled from secondary research.

Signals: original screenshots, data exports, personal anecdotes, dateable case studies, survey data, A/B test findings, real client outcomes with numbers.

### Expertise (7/25 points)
Depth of knowledge in the content and in the creator's broader profile. Two types:
- **Formal expertise:** Required for [[ymyl]] topics — medical, legal, financial. Must have credentials (MD, JD, CFP).
- **Informal expertise:** Acceptable for lifestyle, DIY, hobby content — deep demonstrated knowledge and track record.

Author bio requirements for maximum score: name visible, professional title, credentials, years in field, notable achievements, LinkedIn link, photo, Person schema with sameAs.

### Authoritativeness (5/25 points)
Reputation signal — how others in the ecosystem reference your content and brand. Driven by backlink profile, brand mentions, press coverage, Wikipedia/Wikidata presence, and consistent NAP entity data.

### Trustworthiness (5/25 points — Master Signal)
Google's QRG states Trust is the most important dimension. Zero trust = zero E-E-A-T regardless of credentials.

**Technical trust:** HTTPS (non-negotiable), Privacy Policy, Terms of Service, Cookie consent, Contact information, Accessibility.

**Content trust:** Cite credible external sources with visible links; display published AND last updated dates; correct errors transparently; no affiliate link overload.

**Trust decay factors (eliminate these):**
| Factor | Impact |
|--------|--------|
| Content older than 2 years (fast topics) | High |
| No author attribution | High |
| No SSL (HTTP) | Critical |
| Thin content (< 300 words) | High |
| Plagiarised/duplicate content | Critical |
| Unverified health/financial claims | Critical |

## E-E-A-T Scoring in the Content Rubric

| Signal | Max Points |
|--------|-----------|
| First-hand experience demonstrated | 4 |
| Named author with relevant bio | 4 |
| Author credentials match topic | 3 |
| External citations from credible sources | 3 |
| Content freshness (< 12 months) | 3 |
| Schema markup (Author, Article, Org) | 3 |
| Trust signals (HTTPS, contact, privacy) | 3 |
| Consistent entity information | 2 |
| **Total** | **25** |

## Application to WildnetEdge Content

- Every blog needs a **named author byline with bio and credentials**
- All service pages need a **methodology section** and **results/outcomes with numbers**
- Every piece needs **3–5 external citations** to credible sources
- Always display **published date AND last updated date**

## Sources

- [[2026-06-10-central-rag-document]]
