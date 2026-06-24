---
title: "Obsidian"
type: entity
tags: [product, tool, knowledge-management, markdown]
created: 2026-06-10
updated: 2026-06-10
sources: [2026-06-10-llm-wiki-pattern]
---

# Obsidian

A local-first, markdown-based personal knowledge management app. Files live on disk as plain `.md` files — no proprietary format, no cloud lock-in. The recommended interface for browsing and navigating a [[llm-wiki-pattern]] wiki.

## Role in the LLM Wiki Pattern

In the [[llm-wiki-pattern]], Obsidian serves as the **IDE for the wiki**: the LLM writes the files, the human browses and navigates them in Obsidian in real time. The metaphor: "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

## Relevant Features

- **Graph view** — visualizes the link structure of the wiki; shows hubs, orphans, and clusters.
- **Wikilinks** (`[[page-name]]`) — the cross-reference format used throughout this wiki.
- **Web Clipper** — browser extension that converts web articles to markdown for quick addition to `raw/`.
- **Download attachments** — hotkey to download all inline images to a local `assets/` folder.
- **Marp plugin** — renders Marp-format slides from markdown files.
- **Dataview plugin** — SQL-like queries over YAML frontmatter; enables dynamic index tables.

## Sources

- [[2026-06-10-llm-wiki-pattern]]
