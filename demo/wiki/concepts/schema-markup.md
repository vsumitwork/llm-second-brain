---
title: "Schema Markup (Structured Data)"
type: concept
tags: [schema, structured-data, json-ld, seo, geo, technical-seo]
created: 2026-06-10
updated: 2026-06-10
sources: [Central_RAG_Document_Enhanced_v2]
---

# Schema Markup (Structured Data)

JSON-LD structured data that serves two simultaneous purposes: makes content eligible for rich results in Google SERPs, and structures information as machine-readable data that LLMs can confidently extract and attribute. **Schema is the bridge between human-readable content and machine-processable knowledge.**

Organization schema is the single most important implementation for [[geo-llm-visibility]] — it should appear on every page sitewide.

## Required Schema by Page Type

| Page Type | Required | Optional/Recommended |
|-----------|---------|---------------------|
| All Pages | Organization, WebPage | BreadcrumbList |
| Homepage | Organization, WebSite | LocalBusiness, SiteLinksSearchBox |
| Service Page | Service, FAQPage | LocalBusiness, Review, Offer |
| Blog Post | Article (or BlogPosting), Person (Author) | FAQPage, HowTo, ImageObject |
| Case Study | Article, Organization | Review |
| How-To Guide | HowTo | FAQPage, Article |
| FAQ Page | FAQPage | WebPage |

## Organization Schema (Mandatory Sitewide)

Most important schema for entity recognition by LLMs. Required properties:
`@type, name, url, logo, description, foundingDate, contactPoint, sameAs`

`sameAs` must link to: LinkedIn, Twitter/X, Facebook, Crunchbase, Wikipedia (if exists), Google Business Profile, YouTube, GitHub

## Article/BlogPosting Schema

Required: `headline, author (Person schema), datePublished, dateModified, image, publisher (Organization), mainEntityOfPage, description`

Critical: **`dateModified` must be updated every time content is substantively updated** — both a freshness signal for LLMs and a rich result eligibility requirement.

## Why Schema Matters for [[e-e-a-t]]

Schema signals (Author, Article, Org) account for **3 of 25 E-E-A-T points** in the [[content-scoring-rubric]]. Missing schema = automatic -3 on E-E-A-T score.

## Sources

- [[2026-06-10-central-rag-document]]
