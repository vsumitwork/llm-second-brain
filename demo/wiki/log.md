# Wiki Log

Append-only. Each entry: `## [YYYY-MM-DD] TYPE | Description`
Parse last 5: `grep "^## \[" log.md | tail -5`

---

## [2026-06-10] maintenance | Wiki initialized
Created full directory structure (raw/, raw/assets/, wiki/entities/, wiki/concepts/, wiki/sources/, wiki/analyses/). Created CLAUDE.md schema, wiki/index.md, wiki/log.md, wiki/overview.md. 0 sources ingested. Ready for first ingest.

## [2026-06-10] ingest | "LLM Wiki — A Pattern for Building Personal Knowledge Bases"
Source: raw/2026-06-10-llm-wiki-pattern.md. Created: sources/2026-06-10-llm-wiki-pattern.md, entities/vannevar-bush.md, entities/obsidian.md, concepts/llm-wiki-pattern.md, concepts/rag.md, concepts/memex.md, concepts/compounding-knowledge.md, concepts/associative-trails.md. Updated: wiki/overview.md, wiki/index.md. 10 pages created/updated.

## [2026-06-10] maintenance | Wiki moved to demo/ folder; domain set to content creation
User moved all files to demo/ subfolder. Domain confirmed: B2B content creation for WildnetEdge. Wiki purpose: produce SEO/GEO-optimised content (blogs, service pages, case studies). 4 new sources added to raw/ for ingestion.

## [2026-06-10] ingest | "AI Content Score Engine — Master RAG Knowledge Base v2.0" (Central_RAG_Document_Enhanced_v2.md)
Source: raw/Central_RAG_Document_Enhanced_v2.md. 20-section master scoring and strategy reference. Created: sources/2026-06-10-central-rag-document.md, concepts/e-e-a-t.md, concepts/google-helpful-content-system.md, concepts/ai-overviews-aio.md, concepts/geo-llm-visibility.md, concepts/content-scoring-rubric.md, concepts/keyword-intent-mapping.md, concepts/schema-markup.md, concepts/ymyl.md, concepts/answer-capsule-framework.md. 10 pages created. Notable: sections 11–20 not fully extracted (link building, content refresh, CRO, analytics, international SEO — flagged as Gap for future pass).

## [2026-06-10] ingest | "WildnetEdge Content Writing & SEO Guide" (WildnetEdge_Writing_Guide.md)
Source: raw/WildnetEdge_Writing_Guide.md. Brand voice, tone, content-type formats, scorecards. Created: sources/2026-06-10-wildnatedge-writing-guide.md, entities/wildnet-edge.md, concepts/wildnatedge-writing-standards.md, concepts/blog-content-pattern.md. 4 pages created. Notable: hard rule confirmed — no em dashes in blogs. Scorecard minimums: 4.0/5.0 for blogs and service pages.

## [2026-06-10] ingest | "Flesch-Kincaid Readability Calculator" (Flesch Kincaid Calculator.md)
Source: raw/Flesch Kincaid Calculator.md. Readability scoring formulas. Created: sources/2026-06-10-flesch-kincaid-calculator.md, updated concepts/flesch-reading-ease.md. User's minimum requirement: Flesch Reading Ease 50+; target 60–70. 2 pages created/updated.

## [2026-06-10] ingest | "10 Tips to Hire iOS App Developers in the USA" (sample blog)
Source: raw/10 Tips to Hire iOS App Developers in the USA.md. Reference blog example. Created: sources/2026-06-10-ios-developer-hiring-blog.md. Updated: concepts/blog-content-pattern.md, entities/wildnet-edge.md, wiki/overview.md. This is the canonical output example for WildnetEdge blogs. 4 pages created/updated.

## [2026-06-10] maintenance | Filled stubs + created content brief template
Filled Obsidian-generated stub pages: concepts/keyword-density-targets.md, concepts/flesch-kincaid-grade-level.md. Created: analyses/content-brief-template.md (the operational brief to fill before every blog request). Total wiki: 5 sources ingested, 34 pages. System is production-ready.

## [2026-06-11] query | Blog v1 produced then discarded — Flutter developer hiring
First draft too close to iOS reference blog template. Discarded. Rebuilt blog-types system.

## [2026-06-11] maintenance | Created blog-types/tips-blogs/ production system
Created: blog-types/tips-blogs/_schema.md (anti-template rules, variation rules, plagiarism prevention), _learnings.md (feedback log for each blog), _reference/ios-developer-hiring-reference.md (structural guide only — banned language patterns listed), output/ folder. Updated CLAUDE.md to reference blog-types system. Added rule: read _schema.md + _learnings.md + latest output before writing any tips blog.

## [2026-06-11] maintenance | Moved Tip Blog Schema.docx to reference folder
Moved demo/Tip Blog Schema.docx → demo/blog-types/tips-blogs/_reference/Tip Blog Schema.docx. This is the canonical user-provided format spec for all tips blogs. Updated reference folder index in ios-developer-hiring-reference.md.

## [2026-06-11] query | Blog v2 produced — "10 Tips to Hire Flutter App Developers in the USA (2026 Guide)"
Output: blog-types/tips-blogs/output/flutter-developers-2026.md (~1,800 words). v2 fixes: new hook, varied tip openings, counter-intuitive Key Takeaways, no "traces back to" conclusion. Feedback received: em dashes, no source hyperlinks, conclusion/CTA too templated, not American English.

## [2026-06-11] maintenance | 6 new rules ingested from user feedback — schema updated
Word count 1300-1500, USA capitalized, short FAQs, no hyperlinks in Key Takeaways, meta <155 chars with keyword, catchy headings. Added to _schema.md Section 2 and Section 8. Updated _learnings.md with v3 feedback and v4 targets.

## [2026-06-11] maintenance | Updated _schema.md with 3 new rule sections
Added to tips-blog schema: Language Standards (American English, em dash ban, inline source hyperlinks from credible publishers), full Conclusion rules (banned heading, banned opener, banned para 2 structure), full CTA rules (banned structure, specific action label required). Updated _learnings.md with v2 feedback and v3 targets.

## [2026-06-11] query | Blog v4 produced — Flutter developer hiring blog (final)
~1400 words. All 6 rules applied. Catchy headings throughout. Zero em dashes. USA capitalized. Short FAQs. No hyperlinks in Key Takeaways. Meta 146 chars with primary keyword. 4 inline source hyperlinks in body only. Learnings filed.

## [2026-06-11] maintenance | Writer rewrite ingested — 6 new rules added to tips-blog system
Writer rewrote v4 of the Flutter blog. Key new rules extracted and added to _schema.md: (1) No fluff — every sentence must add new information, (2) Stats must be recent (2024–2026) and correctly matched to claims, (3) Clearer sentences — cut meander, not just length, (4) Keyword grammar — secondary keywords rewritten as natural English with proper prepositions, (5) Proper case for technology names — Flutter, Dart, iOS, etc. always capitalized, (6) Callout formats — Pro Tip/Ask this/Example/Ask callouts, bullet points within tips and FAQs, WildnetEdge-specific value props. Writer's rewrite saved as canonical style reference: _reference/flutter-writer-rewrite-reference.md. System ready for next blog topic.
All issues from v2 resolved. Zero em dashes. 4 inline hyperlinked sources: Stack Overflow Developer Survey 2024, Apple privacy manifest docs, Google Play developer docs, Statista mobile market. New conclusion heading: "Flutter Delivers What the Developer Behind It Can Execute." Conclusion para 2 starts with "Wildnet Edge structures..." not "At Wildnet Edge...". CTA rewritten from scratch: leads with reader's situation, ends with "Connect With a Flutter Expert." American English throughout. v3 learnings filed.

## [2026-06-15] maintenance | Added §13 token budget rules to CLAUDE.md
Hard constraint: max $0.50 per blog session. Rules: lazy load only, offset/limit for large files, no redundant reads, lean session start (CLAUDE.md + first 30 lines index.md + last 3 log entries), ingest selectively (new info only), one-line confirmations. CLAUDE.md updated, memory updated.

## [2026-06-15] query | Blog v1 produced — React Native developer hiring blog
Output: blog-types/tips-blogs/output/react-native-developers-2026.md (~1450 words). Focus keyword used 6 times. All 8 secondary keywords distributed. 4 inline citations: Dev.to, OpenPR, Remote Crew, Business Outsiders. Expo vs. Bare workflow as central differentiator. Learnings filed.

## [2026-06-22] query | Blog v1 produced — Healthcare app developer hiring blog
Output: blog-types/tips-blogs/output/healthcare-app-developers-2026.md (~1400 words). Focus keyword 6 uses. All 6 secondary keywords placed. 4 inline citations. Zero em dashes. Central angle: HIPAA as architecture foundation, not checklist. BAA explained practically across 4 touch points.

## [2026-06-22] maintenance | Writer rewrite ingested — 8 new rules added from React Native blog v2
Writer rewrote Blog #2 (React Native). Key rules extracted: digit+% in Key Takeaways, WildnetEdge body links (staff aug + service page), italicized table captions, image placeholders after bullet lists, bold contrasting labels, FAQ Pro Tip/Hack callouts, "None of these is" grammar, source quality hierarchy. All added to _schema.md §13. Learnings updated.

## [2026-06-22] maintenance | React Native writer rewrite saved to reference folder; CLAUDE.md updated
Created: _reference/react-native-writer-rewrite-reference.md (current canonical style reference). Updated CLAUDE.md §2 and §13: blog writing sequence now reads most recent _reference file (first 60 lines) instead of latest output file. Updated memory with new canonical pointer.

## [2026-06-22] maintenance | Graph connections fixed — 7 new pages, wikilinks added, CLAUDE.md updated
Created: concepts/staff-augmentation.md, concepts/content-review-scorecard.md, concepts/keyword-placement-priority.md, concepts/lint-workflow.md (all 4 were ghost nodes). Created: analyses/blog-flutter-developers-2026.md, analyses/blog-react-native-developers-2026.md, analyses/blog-healthcare-app-developers-2026.md. Added [[wikilinks]] header to _schema.md and _learnings.md. Updated CLAUDE.md §13: full reference file read (not 60 lines), Flesch check step, source quality check. Updated wiki/index.md to 42 pages.
