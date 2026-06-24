---
title: "RAG (Retrieval-Augmented Generation)"
type: concept
tags: [framework, llm, knowledge-retrieval, architecture]
created: 2026-06-10
updated: 2026-06-10
sources: [2026-06-10-llm-wiki-pattern]
---

# RAG (Retrieval-Augmented Generation)

The dominant pattern for LLM + document systems. At query time, relevant document chunks are retrieved (via embeddings/vector search) and fed to the LLM to generate an answer. Examples: NotebookLM, ChatGPT file uploads, most enterprise document-QA systems.

## How It Works

1. Documents are chunked and embedded into a vector database.
2. At query time, the user's question is embedded and nearest chunks are retrieved.
3. The LLM synthesizes an answer from those chunks.

## Limitations (per [[llm-wiki-pattern]])

- **Re-derives on every query**: no accumulated synthesis, no persistent cross-references.
- **Subtlety ceiling**: a question requiring synthesis across 5 documents must find and integrate all 5 relevant fragments at query time — fragile.
- **No contradiction detection**: contradicting claims in different documents are discovered at query time, not surfaced proactively.
- **Nothing compounds**: the system doesn't get richer as you add documents; it just gets a bigger retrieval pool.

## Contrast

See [[llm-wiki-pattern]] for the contrasting approach.

> Contradiction: None known. RAG and the LLM wiki pattern are complementary at large scale — the LLM wiki may need search infrastructure (like [[qmd]]) when the wiki grows past ~hundreds of pages.

## Sources

- [[2026-06-10-llm-wiki-pattern]]
