---
title: "LLM Wiki — A Pattern for Building Personal Knowledge Bases"
type: source
tags: [knowledge-management, llm, second-brain, architecture, framework]
created: 2026-06-10
updated: 2026-06-10
sources: [2026-06-10-llm-wiki-pattern]
---

# LLM Wiki — A Pattern for Building Personal Knowledge Bases

**Source:** `raw/2026-06-10-llm-wiki-pattern.md`
**Ingested:** 2026-06-10

## Summary

A design pattern for using LLMs not as retrieval engines (like [[rag]]) but as active knowledge-base maintainers. The LLM reads sources and integrates their content into a persistent, interlinked wiki of markdown files. The wiki compounds over time: cross-references are pre-built, contradictions are pre-flagged, synthesis already reflects everything ingested. The human curates sources and asks questions; the LLM does all bookkeeping.

## Key Claims

- **RAG re-derives on every query**; the LLM wiki compiles knowledge once and keeps it current.
- The wiki is a **compounding artifact** — each new source makes the whole richer, not just adds a new chunk.
- Three layers: raw sources (immutable), wiki (LLM-owned), schema (CLAUDE.md / AGENTS.md).
- Three operations: [[ingest-workflow]], [[query-workflow]], [[lint-workflow]].
- The human's role is **curation, direction, and synthesis**; the LLM's role is bookkeeping.
- The pattern is spiritually related to [[vannevar-bush]]'s [[memex]] (1945) — the part Bush couldn't solve (who does maintenance) is what LLMs handle.
- Good answers to queries should be **filed back** into the wiki as analysis pages so explorations compound.
- The wiki is just a git repo — version history and collaboration are free.

## Key Entities & Concepts

- [[vannevar-bush]] — inventor of the Memex concept (1945)
- [[rag]] — the dominant alternative pattern (retrieval-augmented generation)
- [[memex]] — Bush's 1945 vision of a personal associative knowledge store
- [[llm-wiki-pattern]] — the core pattern this source introduces
- [[compounding-knowledge]] — the key property that distinguishes this from RAG
- [[obsidian]] — recommended IDE for browsing the wiki
- [[ingest-workflow]] — workflow for adding a new source
- [[query-workflow]] — workflow for asking questions against the wiki
- [[lint-workflow]] — workflow for health-checking the wiki
- [[associative-trails]] — Bush's term for linked paths through knowledge

## Notable Quotes

> "The wiki is a persistent, compounding artifact. The cross-references are already there. The contradictions have already been flagged."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## Gaps & Questions

> Gap: The document doesn't specify how to handle very large wikis (1000+ pages) where reading index.md becomes expensive. qmd/MCP search is mentioned but not detailed.

> Gap: No guidance on conflict resolution when two sources directly contradict each other — who arbitrates?

> Gap: Team/multi-user wikis are mentioned but not elaborated. How do multiple humans interact with a single LLM-maintained wiki?
