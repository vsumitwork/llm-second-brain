---
title: "Lint Workflow"
type: concept
tags: [wiki-maintenance, quality-control]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-10-llm-wiki-pattern]
---

## Definition

The lint workflow is the wiki maintenance process run when the user says "lint the wiki." It audits the entire wiki for health issues and produces a prioritized fix list.

## Seven Checks

1. **Contradictions** — claims on different pages that conflict with each other
2. **Stale claims** — content superseded by newer ingested sources (check log.md order)
3. **Orphan pages** — pages with no inbound `[[links]]` from other pages
4. **Stub pages** — pages that exist as unresolved `[[links]]` but have no content file
5. **Missing cross-references** — entity or concept mentioned on a page but not linked
6. **Data gaps** — `> Gap:` blockquotes that could now be filled by a new source or web search
7. **Index drift** — pages that exist but are missing from index.md, or index entries for pages that no longer exist

## Output

A prioritized list of issues. The user decides which to fix now vs. log for later. The wiki agent does not auto-fix without user direction — except stub pages, which can be created immediately.

## Related Concepts

- [[llm-wiki-pattern]] — the overall wiki operating model this workflow maintains
- [[compounding-knowledge]] — the principle that makes regular linting necessary: the wiki compounds, so drift accumulates

## Sources

- [[2026-06-10-llm-wiki-pattern]]
