# Tips Blog Schema

**Related Wiki Concepts:** [[wildnatedge-writing-standards]] · [[e-e-a-t]] · [[content-scoring-rubric]] · [[content-review-scorecard]] · [[flesch-reading-ease]] · [[geo-llm-visibility]] · [[answer-capsule-framework]] · [[keyword-intent-mapping]] · [[keyword-placement-priority]] · [[keyword-density-targets]] · [[blog-content-pattern]] · [[staff-augmentation]] · [[ymyl]] · [[ai-overviews-aio]]

Rules specific to tips-format blogs for WildnetEdge. This supplements the general standards in CLAUDE.md and wiki/concepts/wildnatedge-writing-standards.md — do not repeat what is already there.

---

## 1. What a Tips Blog Is

A tips blog is a numbered-list article (typically 8–12 tips) that helps a decision-maker solve a specific hiring, technical, or operational problem. The numbered format gives it scannability for busy readers and natural FAQ/AIO extraction targets for AI platforms.

**Use this format for:** hiring guides, evaluation checklists, process improvement pieces, "what to look for when..." articles.

**Do not use this format for:** opinion pieces, comparison articles, or thought leadership pieces where a numbered structure would feel forced.

---

## 2. Structure (Required Order)

```
Frontmatter (YAML — meta description < 155 chars, primary keyword in it)
Key Takeaways (####)  ← NO hyperlinks inside Key Takeaways
Hook paragraph(s) — no heading
## [Catchy cost section heading]  (cost table — hiring-focused pieces)
## Tip 1: [Catchy heading]
## Tip 2: [Catchy heading]
...
## Tip N: [Catchy heading]
## [Unique conclusion heading — specific to the blog topic]
## FAQs
CTA Banner
```

---

## 3. Anti-Template Rules (Critical)

These rules exist because tips blogs share the same skeleton. Without active variation, every blog ends up feeling like a copy of the last one.

### Hook — Never Repeat These Patterns
- **BANNED opener:** "Finding the right X sounds manageable until you are [timeframe] into the project and realize..."
- **BANNED opener:** "This happens more often than it should."
- **BANNED:** Any hook that follows the "sounds easy → surprising failure" structure used in the iOS reference blog.
- **Required:** Each blog must have a structurally different hook. Options: data-led open, observation about the market, a specific paradox, a counter-intuitive claim, a direct problem statement.

### Key Takeaways — No Generic Summaries
- At least 2 of the 5 bullets must be surprising or counter-intuitive — facts the reader would not predict without reading the blog.
- Avoid bullets that simply restate the tip headings.
- Bad: "Choosing the right hiring model is important."
- Good: "State management framework choice reveals more about a Flutter developer than any whiteboard test."

### Tip Openings — Mandatory Variation
No two consecutive tips may open with the same grammatical structure. Rotate between:
- **Data/fact open:** Start with a statistic or technical fact.
- **Scenario open:** Start with a concrete situation a reader recognizes.
- **Question open:** Start with a question the reader is asking.
- **Direct statement open:** Start with a clear, confident assertion.
- **Observation open:** Start with a pattern noticed across many engagements.

After writing all tips, look at the first sentence of each. If more than 3 start with "Ask the candidate..." or "A developer who..." or any other repeated structure — rewrite them.

### Conclusion — Full Rules
- **BANNED heading:** "The Right Hire Is the First Product Decision You Make" — this was the iOS reference blog heading. Every tips blog must have a unique conclusion heading tied to its specific topic.
- **BANNED opener:** "Every [bad outcome]... traces back to a hiring decision made with..."
- **BANNED para 2 opener:** "At Wildnet Edge, our [focus keyword] are integrated into..." — too templated.
- **Required:** 2 short paragraphs. Para 1 is a forward-looking or thematic close specific to the blog topic. Para 2 mentions Wildnet Edge + focus keyword in the same sentence, with a different opening than "At Wildnet Edge."
- The conclusion heading must be written fresh for each blog. It should reflect the central insight of the specific post, not a generic "the hire is the first decision" idea.

### CTA Banner — Full Rules
- **BANNED structure:** "Need dedicated X developers for your next product build? / Let us help you find experienced X talent matched to your product goals..." — this exact structure appeared in both the iOS reference and v1 of the Flutter blog.
- **Required:** Each CTA must have a genuinely different structure. Options: lead with what the reader already knows they need, lead with a specific WildnetEdge capability, lead with a question about the reader's timeline or goal.
- The action button label must be specific to the blog topic, not a generic "Hire X Now."

---

## 4. Answer Capsule Implementation for Tips Blogs

Each tip section is an answer capsule (see wiki/concepts/answer-capsule-framework.md) but implemented with varied prose:

- The tip H2 heading is the question/claim
- The first 1–2 sentences are the direct answer (what to do and why)
- The body is the evidence, context, or test method
- End with a concrete "how to test this" or "what the right answer sounds like" where relevant — these are highly extractable by AI Overviews

Every tip needs at minimum: a direct answer, one piece of evidence or context, and one actionable test or signal.

---

## 5. Keyword Placement (Tips-Blog Specific)

Focus keyword placement for a 10-tip blog:
- Title / H1: 1 use
- Key Takeaways bullet 1: 1 use
- Intro paragraph: 1 use
- Tip 2 or 3 body: 1 use (natural, not forced — e.g., "One of the most actionable tips to hire X is...")
- Tip 6 or 7 body: 1 use
- Conclusion: 1 use (WildnetEdge + focus keyword in the same sentence)

Total: 6 uses. This satisfies the 5–7 requirement without forcing repetition.

Secondary keywords: distribute one per tip where natural. Do not cluster all secondary keywords in the first 3 tips.

---

## 6. Cost Table Rules

- Always include for hiring-focused tips blogs.
- Three rows: Junior (1–3 yrs), Mid-level (3–5 yrs), Senior (5+ yrs).
- Three columns: Full-Time USA, Contract Rate USA, Offshore Rate.
- Research current market rates — do not copy previous blog's rates verbatim. Rates shift.
- One sentence before the table: introduce the cost context. One sentence after: connect the table to the tips.

---

## 7. FAQ Rules

- 5 questions, labeled Q1–Q5.
- Source questions from: Google SERP "People Also Ask," AI Overviews, and ChatGPT responses for the target keyword.
- Questions must be phrased as a reader would actually ask them — conversational, not keyword-stuffed.
- Answers: 2–4 sentences each. Direct. Include at least one number per answer where possible.
- Standard FAQ topics for hiring blogs: cost, difference between models, technical skills, remote hiring tips, timeline.

---

## 8. Language Standards

- **Word count: 1300 to 1500 words.** Count everything except frontmatter. Stay within this range. Tighter is better. Do not pad to hit a number.
- **American English only.** No exceptions. Use: analyze (not analyse), behavior (not behaviour), center (not centre), organize (not organise), color (not colour), optimized (not optimised), modeled (not modelled).
- **USA is always capitalized** as "USA" — never "usa" or "Usa" anywhere in the document, including cost tables, headings, and body copy.
- **No em dashes anywhere.** Replace every em dash with a comma, colon, or a new sentence. Before filing, search the draft for " — " and rewrite any sentence that contains one.
- **Meta description:** Must be fewer than 155 characters. Must include the primary keyword. Write it before the body so the frame is clear. Curiosity-driven preferred.
- **Key Takeaways: no hyperlinks.** Hyperlinks belong in the body only — never in the Key Takeaways bullets.
- **External sources (body only):** Every tips blog must include 3 to 5 hyperlinked citations to credible, non-competitor sources. Acceptable sources: Statista, McKinsey, Deloitte, IBM, Gartner, Stack Overflow Developer Survey, LinkedIn Economic Graph, Apple/Google official documentation, Forrester, IDC. Hyperlink the specific word or phrase inline. Never list sources at the end.
  - Sources must support the specific claim they are attached to. A developer adoption stat must link to a developer survey, not a page about developer working hours.
  - Use 2024–2026 stats only. Replace any older stat before filing.
  - Avoid overclaims: "Flutter is the most popular cross-platform framework" ✓ vs "most developers use Flutter" ✗

### Proper Nouns and Technology Names
ALL technology and framework names are proper nouns and must be capitalized exactly:
- Flutter, Dart, iOS, Android, SwiftUI, UIKit, Skia, Impeller, Bloc, Riverpod, GetX, Provider, MobX
- Google, Apple, Microsoft, IBM, Stack Overflow, Statista, WildnetEdge
- If in doubt: look up the official brand capitalization

### Keyword Grammar Rules
Secondary keywords must be grammatically integrated into natural sentences. Never insert a keyword verbatim if it reads unnaturally or lacks grammar words:
- "flutter app developers usa" → "Flutter app developers in the USA"
- "dedicated flutter developers" → "dedicated Flutter developers"
- "flutter development company usa" → "Flutter development company in the USA"
- "hire remote flutter developers" → "hire remote Flutter developers"
- "cross platform app developers" → "cross-platform app developers" or "cross platform app developers"
- Rule: If a keyword has a proper noun (framework, company, product), capitalize it. If it lacks prepositions/articles to read naturally, add them.

### No-Fluff Rule
Every sentence must add information the reader did not have before. Delete:
- Setup sentences: "Here is something that happens in almost every engagement..."
- Filler transitions: "This is particularly important because..."
- Restatements: sentences that say what the previous sentence already said
- Test: read each sentence and ask "What new information does this add?" If nothing, delete it.

### Catchy Headings
Tip headings must read like something an experienced editor would approve:
- Can be complete statements ending with a period: "A Quote Without Scope Is a Lie."
- Can use a semicolon to join two ideas: "The App Store Does Not Lie; Use It"
- Must create curiosity or deliver a surprising frame
- BANNED: generic instructions like "Define Project Scope Before You Talk to Anyone"

---

## 9. Callout Formats

Use these formatted callouts within tip sections to improve scannability:

- `**Pro Tip**:` — actionable insight beyond the main point of the tip (1–2 sentences)
- `**Ask this**:` — exact interview question phrasing to use with a candidate
- `**Ask**:` — a suggested question, quoted in the text
- `**Example**:` — a concrete scenario or test to illustrate the tip

**Rules:**
- Maximum 1–2 callouts per tip section. Do not overuse.
- Callouts replace summary sentences — do not add them on top of a full paragraph
- Each callout must be 1–3 sentences max
- Bold the label (`**Pro Tip**:`), follow with normal text

### Bullet Points Within Tips
When a tip involves a list of 3 or more items, use bullet points:
- What to document, check, ask, or look for
- Steps in a process
- Multiple options the reader must consider
Bullets make content scannable for decision-makers. Each bullet should be one complete thought.

### WildnetEdge-Specific Mentions
Include specific WildnetEdge value propositions where natural, especially in Tip 2 (hiring model):
- Onboarding speed: "WildnetEdge onboards dedicated developers in 1–2 days"
- Internal service page links: link the service page name to the real URL where available
- FAQ answers can include: "By the way, our staff-augmented developers are aligned within 1–2 days"
These must feel natural, never forced. Include them only where genuinely relevant.

### FAQ Format Update
FAQs can now use bullet points within answers when listing multiple items:
- Technical skills, timeline stages, process steps work well as bullets
- Add one real-world insight per FAQ where possible (e.g., "most brands spend 2 months hiring before work begins")

---

## 10. Plagiarism Prevention

**Research workflow:**
1. Read competitor pages for structural coverage and topic gaps — not for language.
2. Extract data points (statistics, rates, percentages) with their sources.
3. Close the competitor pages before writing.
4. Write from what you know and what the wiki contains — not from paraphrasing what competitors said.

**Self-check before filing:**
- Do not search for your sentences in a plagiarism tool — instead, ask: "Did I write this sentence based on my own synthesis, or am I paraphrasing a competitor's phrase?"
- Any sentence that mirrors a competitor's structure should be rewritten entirely.
- Statistics must be attributed to their original source (e.g., "Stack Overflow 2025"), not to the competitor who cited them.

---

## 11. Output Filing

Every produced tips blog goes into:
`blog-types/tips-blogs/output/[topic-slug]-[year].md`

After filing, update:
- `blog-types/tips-blogs/_learnings.md` — add a brief entry on what this blog did well, what it did not, and any feedback received
- `wiki/log.md` — standard log entry
- `wiki/index.md` — no entry needed (output files are not wiki pages)

---

## 13. Writer Rewrite Rules (Added 2026-06-22 — Apply to All Future Blogs)

These rules were extracted from the writer's rewrite of Blog #2 (React Native). Apply to every blog from now on.

### Numbers and Symbols
- In **Key Takeaways** and **callout labels**, use digits + % sign: "15–20%" not "15 to 20 percent."
- In **body prose**, written-out numbers are fine for readability.
- Tip headings can use symbols for visual punch: ≠ for "not equal to," % for percentages.

### WildnetEdge Links (Embed in Body, Not Just CTA)
Every blog must include two WildnetEdge internal links in the body:
1. **Staff augmentation speed** (Tip 2 / hiring model tip): link "one to two business days" or "48 hours" → `https://www.wildnetedge.com/it-staff-augmentation-company`
2. **Topic service page** (Tip 3 or 4): link the focus keyword or an action phrase → the relevant WildnetEdge service URL for that blog topic
3. **CTA button**: always hyperlink → `https://www.wildnetedge.com/`

### Table Caption
After every data table, add a short italicized caption on its own line:
`*[Year]'s [Topic] Costing vs Experience in the USA*`
Example: `*2026's React Native Developer Costing vs Experience in the USA*`

### Image Placeholder
After any bullet list of 3+ items in a tip, add an italicized placeholder line on its own line below the last bullet. This marks where a visual should be inserted before publishing:
`*[Alt text — briefly describe what image should show]*`
Example: `*Tips to Hire React Native Developers in 2026*`

### Bold Contrasting Labels
When a tip contrasts two or more models or options, **bold the label on first use** within that tip:
- **Dedicated developers** vs **Freelancers**
- **React.js developers** vs **React Native developers**
This improves scannability for decision-makers.

### FAQ Enhancements
- Bullet points inside FAQ answers are allowed and encouraged for multi-step processes.
- **Pro Tip**: or **Hack**: callouts are allowed inside FAQ answers for actionable shortcuts.
- Add a one-line intro phrase before bullet lists in FAQs: "Follow these steps." or similar.

### Grammar: "None of these"
"None" followed by a prepositional phrase takes a singular verb.
- Correct: "None of these **is** supported by the Expo managed workflow."
- Wrong: "None of these **are** supported..."

### Source Quality
Prefer sources in this order:
1. Academic papers, government/official data (HHS, HealthIT.gov, academic journals)
2. Primary research firms (Grandview Research, Statista, Deloitte, McKinsey)
3. Industry surveys (Stack Overflow, LinkedIn Economic Graph)
4. News/blog citations only when no primary source is available

---

## 12. Reference Files

`blog-types/tips-blogs/_reference/` contains stripped-down reference examples. Read ALL files in this folder before writing any tips blog:
- `Tip Blog Schema.docx` — original user-provided format spec
- `ios-developer-hiring-reference.md` — structural map and banned language patterns
- `flutter-writer-rewrite-reference.md` — writer's rewrite showing callout formats, keyword handling, heading style, FAQ structure. **This is the canonical style reference.**
