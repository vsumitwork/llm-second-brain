---
title: "LLM Wiki Pattern"
type: concept
tags: [framework, knowledge-management, second-brain, architecture]
created: 2026-06-10
updated: 2026-06-10
sources: [2026-06-10-llm-wiki-pattern]
---

# LLM Wiki Pattern

A design pattern for building a **persistent, compounding personal knowledge base** where an LLM actively maintains a wiki of markdown files rather than passively answering queries from raw documents (as in [[rag]]).

## Core Distinction

| | [[rag]] | LLM Wiki |
|---|---------|----------|
| Knowledge storage | Raw documents + embeddings | Structured wiki pages |
| Query time work | Re-derive synthesis each time | Read pre-built synthesis |
| Cross-references | Found at query time | Already in place |
| Contradictions | Detected at query time | Already flagged |
| Who writes summaries | Nobody (LLM summarizes on demand) | LLM (persisted to disk) |
| Compounds over time | No | Yes |

## Three Layers

1. **Raw sources** (`raw/`) — immutable source documents. Articles, papers, files. Source of truth.
2. **Wiki** (`wiki/`) — LLM-owned structured knowledge. Summaries, entity pages, concept pages, analyses.
3. **Schema** (`CLAUDE.md`) — operating rules for the LLM. Defines workflows, naming conventions, page formats.

## Three Operations

- **[[ingest-workflow]]** — read a source, extract entities/concepts, update all relevant wiki pages, update index and log.
- **[[query-workflow]]** — read index, read relevant pages, synthesize answer, optionally file answer as analysis page.
- **[[lint-workflow]]** — health-check the wiki for contradictions, orphans, stubs, stale claims, missing links.

## Key Properties

- **Compounding**: each source makes the entire wiki richer, not just adds one more item to retrieve.
- **Pre-built synthesis**: answers draw on already-integrated knowledge, not re-derived fragments.
- **Human-in-the-loop**: human curates sources, asks questions, directs emphasis. LLM does bookkeeping.
- **The wiki is a git repo**: version history, branching, and collaboration are free.

## Intellectual Lineage

Related in spirit to [[vannevar-bush]]'s [[memex]] (1945). Bush envisioned personal, curated, associatively-linked knowledge with [[associative-trails]] between documents. The LLM wiki solves the one problem Bush couldn't: **who does the maintenance**.

## Sources

- [[2026-06-10-llm-wiki-pattern]]
