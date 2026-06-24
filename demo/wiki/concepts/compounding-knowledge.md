---
title: "Compounding Knowledge"
type: concept
tags: [knowledge-management, second-brain, property]
created: 2026-06-10
updated: 2026-06-10
sources: [2026-06-10-llm-wiki-pattern]
---

# Compounding Knowledge

The property of a knowledge base where **each new source makes the entire base richer**, not just adds one more retrievable item. The key differentiator of the [[llm-wiki-pattern]] over [[rag]].

## How It Works

When a new source is ingested:
- Entity pages are updated with new information from the source.
- Concept pages are revised to integrate new evidence.
- Contradictions with prior sources are flagged in place.
- The overview evolves to reflect the new synthesis.
- Cross-references from the new source point to existing pages; existing pages gain back-links.

The result: a question asked after 50 ingests draws on a 50-source synthesis that was built incrementally. In a RAG system, the same question triggers the same retrieval effort each time.

## Analogy

Compounding knowledge is to RAG what compound interest is to simple interest. The returns accumulate. A RAG system earns the same interest rate every time; an LLM wiki's "interest" builds on prior rounds.

## Conditions for Compounding

1. The LLM must **integrate** (not just file) new sources — updating existing pages, not just creating new ones.
2. **Cross-references must be maintained** — orphan pages break the compounding effect.
3. The [[lint-workflow]] must run periodically to catch stale claims and missing links.

## Sources

- [[2026-06-10-llm-wiki-pattern]]
