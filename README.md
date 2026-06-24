# LLM Second Brain — Compounding Content Production System

A persistent, self-improving knowledge base that produces SEO/GEO-optimized content at scale using Claude AI. Each session builds on the last. Each writer rewrite raises the floor for the next draft.

---

## What This Is

Most AI content workflows are stateless — every session starts from zero. This project builds a **compounding knowledge system** where:

- Sources are ingested once and never re-read
- Every rule a writer corrects gets written into the schema permanently
- Every blog produced leaves behind structured learnings for the next one
- The gap between "first AI draft" and "publish-ready" shrinks with every iteration

Built for **WildnetEdge** (B2B tech company) to produce hiring guide blogs targeting Google SERP, AI Overviews, AI Mode, and ChatGPT citations.

---

## Architecture

```
demo/
├── CLAUDE.md                    ← Operating manual (schema, workflows, rules)
├── raw/                         ← Immutable source documents (gitignored)
│   └── assets/
├── wiki/                        ← The knowledge base (Claude owns this entirely)
│   ├── index.md                 ← Content catalog — updated on every ingest
│   ├── log.md                   ← Append-only activity log
│   ├── overview.md              ← Evolving synthesis of the whole wiki
│   ├── concepts/                ← 19 concept pages (E-E-A-T, GEO, Flesch, etc.)
│   ├── entities/                ← Organizations, products, people
│   ├── sources/                 ← One summary page per ingested source
│   └── analyses/                ← Blog performance analyses, content briefs
└── blog-types/
    └── tips-blogs/
        ├── _schema.md           ← Production rulebook (grows with every rewrite)
        ├── _learnings.md        ← Mistake log (append-only)
        ├── _reference/          ← Writer-approved final versions (style floor)
        └── output/              ← Produced blogs
```

---

## How It Works

### Three Loops

**Loop 1 — Ingest**
A source document goes in. Claude extracts entities, concepts, and key claims into structured wiki pages. The raw document is never re-read again.

**Loop 2 — Produce**
To write a blog, Claude reads:
1. `_schema.md` — accumulated production rules
2. Last 20 lines of `_learnings.md` — recent failure log
3. Most recent writer-approved reference file — current style floor
4. Live competitor URLs — structural coverage and fresh stats

Then writes from synthesis — not from re-reading 50-page source documents.

**Loop 3 — Learn**
Writer reviews the draft. Changes are extracted as rules and added permanently to `_schema.md`. The rewritten version becomes the new `_reference/` floor. Next blog starts higher.

```
Ingest sources → Build wiki → Write blog → Writer rewrites
                                                    ↓
                              New rules → _schema.md
                              New floor → _reference/
                                                    ↓
                                          Next blog is better
```

### Token Efficiency

The system is designed to stay **under $0.50 per blog session**:
- Source documents are pre-digested into wiki pages — raw files never reloaded
- Targeted file reads with offset/limit on large files
- No redundant reads within a session
- Schema and learnings files are kept lean

---

## Knowledge Base (Wiki)

**5 sources ingested → 42 wiki pages**

| Category | Pages | Examples |
|---|---|---|
| Concepts — Content Standards | 5 | E-E-A-T, Flesch Reading Ease, Content Scoring Rubric |
| Concepts — SEO & GEO | 7 | AI Overviews, GEO/LLM Visibility, YMYL, Schema Markup |
| Concepts — Writing Mechanics | 6 | Keyword Placement Priority, Answer Capsule Framework |
| Concepts — Knowledge Base Meta | 5 | LLM Wiki Pattern, Compounding Knowledge, RAG |
| Entities | 3 | WildnetEdge, Obsidian, Vannevar Bush |
| Sources | 5 | RAG scoring engine, writing guide, readability standard |
| Analyses | 4 | Blog performance analyses, content brief template |

---

## Content Produced

| Blog | Focus Keyword | Status |
|---|---|---|
| 10 Tips to Hire Flutter App Developers in the USA (2026 Guide) | Tips to Hire Flutter App Developers | Writer-approved v4 |
| 10 Tips to Hire React Native Developers in the USA (2026 Guide) | Tips to Hire React Native Developers | Writer-approved final |
| 10 Tips to Hire Healthcare App Developers in the USA (2026 Guide) | Tips to Hire Healthcare App Developers | v1 produced, awaiting writer review |

All blogs target: Google SERP · AI Overviews · AI Mode · ChatGPT

---

## Production Standards

Every blog is held to three non-negotiable standards before filing:

- **WildnetEdge Writing Standards** — no em dashes, American English, active voice, no filler
- **Content Scoring Rubric** — 75+/100 before publishing
- **Flesch Reading Ease** — ≥ 50 (target 60–70)

---

## The Compounding Effect

```
Blog #1 (Flutter)
  └── Writer rewrites → 6 rules extracted → floor raised

Blog #2 (React Native)
  └── Writer rewrites → 8 new rules extracted → floor raised again
      └── Table captions, image placeholders, WildnetEdge body links,
          FAQ callouts, bold contrast labels, source quality hierarchy

Blog #3 (Healthcare) — first draft already incorporates all 14 prior rules
  └── Writer rewrite pending → will raise floor further
```

By blog #6–8, the first draft should be near-publishable without significant rewriting.

---

## Tech Stack

| Tool | Role |
|---|---|
| Claude AI (claude-sonnet-4-6) | Wiki agent, blog writer, rule extractor |
| Claude Code | IDE + session management |
| Obsidian | Wiki visualization (graph view), local markdown editor |
| Markdown + YAML frontmatter | Page format for all wiki and blog files |

---

## Key Design Decisions

**Why wiki over RAG?**
RAG re-derives knowledge every session from raw documents. A wiki pre-digests sources into structured pages that accumulate connections over time. The knowledge compounds — RAG doesn't.

**Why append-only logs?**
`_learnings.md` and `log.md` are never edited, only appended. This preserves the full history of what was tried, what failed, and what the writer changed — which is the most valuable signal for improving drafts.

**Why writer rewrites become schema?**
A writer's correction is better data than a style guide. It is specific, contextual, and comes from a real quality failure. Encoding it in `_schema.md` means that failure cannot recur.

---

## Graph View (Obsidian)

The wiki is designed to be opened in Obsidian. The graph view shows how concepts, sources, blogs, and production files are interconnected. Blog analysis pages link each produced blog back to the wiki concepts it applies.

---

## Status

Active — new blog topics added weekly. Writer feedback loop ongoing.
