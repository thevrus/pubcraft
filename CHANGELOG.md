# Changelog

All notable changes to Pubcraft will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.2] — 2026-05-06

### Added
- `references/seo-article.md` — new "On-page metadata: title, description, H1 alignment" section. Title tag (50–60 chars / ~575 px, primary keyword in first 30 chars, plus a differentiator). Meta description (120–158 chars, Problem-Solution-CTA, primary keyword in first 90 chars). H1↔title keyword alignment with the Zyppy 2024 finding that Google rewrites mismatched titles from H1 ~61% of the time.
- `references/seo-article.md` — new "Charts and tables" subsection: pair every SVG/Canvas chart with a parallel HTML table for AI extractability and accessibility, bar widths must represent the underlying value (not normalize to top-of-set), comparison tables as citation magnets.
- `references/seo-article.md` — new "URL and IA placement" section: `/research/[slug]` as the default for original-data series, `/[topic-hub]/[slug]` for permanent annually-updated hubs, `/blog/[slug]` for one-offs.
- `references/seo-article.md` — new production-checklist phases: "On-page metadata phase" (title, description, H1, URL placement) and "Charts and tables phase" (SVG-paired-with-HTML-table, bar-width integrity).
- `references/compliance.md` — new "Escalation callouts" section. Generalizes the emergency-callout UX pattern across health, financial, legal, and investment verticals: when an article covers the planned/preventive version of a problem and the reader's situation is more urgent than the article's scope, surface that with a styled callout, not a paragraph.

### Changed
- `references/seo-article.md` — internal-linking rule replaced with a length-scaled version: 3–6 links for ≤1,500 words, 6–10 for 1,500–3,000, 10–15 for 3,000+ original-data reports and pillar pages. Added anchor-text variation guidance (keyword-match ~30%, partial-match ~40%, descriptive or branded ~30%).
- `references/seo-article.md` — FAQPage schema guidance sharpened: when adding FAQ schema, build the question set from People-Also-Ask on the target query (6–8 questions, 50–150-word answers grounded in article data). PAA-mined FAQs are AI-Overview citation magnets even when they don't earn a SERP rich result.
- `references/seo-article.md` — schema-stacking line now lists common vertical-specific types (`MedicalWebPage`, `FinancialProduct`, `RealEstateListing`, `Recipe`, `Course`, `Event`, `Product`) and points to `schema.org/docs/full.html` for the rest. Stack alongside `Article`, never replacing it.

### Why
Audit of a high-quality vertical-specific original-data report surfaced five on-page-SEO mechanics pubcraft hadn't codified: title-tag/meta-description/H1 alignment as pre-publication blockers, FAQ-from-PAA construction, length-scaled internal linking, SVG-paired-with-HTML-table for AI extractability + chart-integrity QA, and URL/IA placement as a strategic decision. Each is generalized to apply across any vertical (financial, real estate, regulatory, SaaS, product) rather than the specific vertical the audit came from. The escalation-callout UX pattern is added to compliance.md generalized across health/financial/legal/investment so any regulated-content draft surfaces urgent-variant resources in a structured way instead of a buried paragraph.

## [0.4.1] — 2026-05-06

### Added
- `references/seo-article.md` — new "Original-data articles" section codifying the five required elements when an article reports first-party data: `Dataset` JSON-LD schema, comparative-baseline framing for every statistic, methodology block, **explicit Limits sub-block** (selection bias, response-rate caveats, what the data does not capture), and observational ("this is what we see") rather than universal stance.
- `references/seo-article.md` — new length tier "Original-data report" (3,000–6,000 words) for first-party-data formats.
- `references/seo-article.md` — new drafting-phase checklist items for original-data articles (baseline framing, methodology + Limits, observational stance).
- `references/seo-article.md` — `Dataset` schema added to standard recommendations whenever an article reports first-party data.
- `references/output-formatting.md` — full `Dataset` JSON-LD code block (creator, temporalCoverage, spatialCoverage, variableMeasured, license) with rationale: AI assistants treat declared Datasets as authoritative primary sources and disproportionately cite them.
- Schema-stacking guidance: `Article` + `Dataset` + `FAQPage` + `Organization` (plus any vertical-specific type that genuinely applies) is a valid combination — each describes a different facet, and AI assistants extract from all of them.
- `references/compliance.md` — new "Escalation callouts" section. Regulated content (health, financial, legal, investment) must surface the urgent variant of a problem with a styled, visually distinct inline callout — not a paragraph — naming the trigger and the next-tier resource. Added as step 3 in the regulated-vertical workflow.

### Changed
- `references/output-formatting.md` — replaced the `MedicalWebPage` code block in "Code-block patterns to keep ready" with a universal `Article` code block. Vertical-specific schemas now point to `schema.org/docs/full.html` rather than picking a winner. Pubcraft is schema-agnostic; vertical choice is the user's, not the skill's.
- `references/output-formatting.md` — audit-template schema example switched from `MedicalWebPage` to `Article` for the same reason.
- `references/output-formatting.md` — inline-code table cell example switched from `MedicalWebPage` to `Article`/`Dataset`.

### Why
Audit of a high-quality original-data report surfaced three patterns pubcraft did not previously codify: `Dataset` schema as a citation magnet, comparative-baseline framing for every statistic, and an explicit Limits sub-block as a Quality-Rater-Guidelines-aligned trust signal. v0.4.1 folds these vertical-agnostic patterns into the standard checklist so any pubcraft-drafted original-data article ships with them on first draft. Audit also surfaced that earlier versions leaned on `MedicalWebPage` as a default schema example, which gave the skill an unintended health-vertical bias; v0.4.1 corrects this by leading with the universal `Article` schema and pointing users to schema.org for vertical-specific types.

## [0.4.0] — 2026-04-29

### Added
- `references/geo.md` — Generative Engine Optimization (AEO/LLMO): citation-magnet patterns (definitions, named-expert quotes, dated statistics, comparison tables), llms.txt reality check, technical bare minimum (server-rendered HTML, Article+Person schema, GPTBot/ClaudeBot/PerplexityBot in robots.txt), brand-mention optimization, AI search market share, measurement via referrer analytics + manual prompt audits.
- `references/youtube-long-form.md` — full upload package: five-system algorithm, satisfaction-signal shift, MrBeast stair-step + Veritasium open-loop + tutorial three-act structures, A/B testing reality (Dec 9, 2025), thumbnail/title craft, mandatory AI disclosure (May 21, 2025), inauthentic-content rule (July 15, 2025), RPM by category, banned phrases.
- `references/podcast.md` — solo + interview architecture, mandatory cold-open teaser, dual show-notes standard (in-app vs. full-essay-as-blog-post), YouTube as #1 podcast platform, video-podcast economics, monetization beyond CPM, NotebookLM disclosure norms.
- `references/newsletters.md` — Ghost section: Ghost 6.0 ActivityPub launch (Aug 2025), 0% transaction fee vs. Substack 10%, three-platform decision matrix.
- `references/output-formatting.md` — production-grade Markdown templates for every deliverable type: standard report opener, article-review template, content brief, GEO audit, ASCII charts, Mermaid diagrams (routing tree, content cluster), JSON-LD code blocks (MedicalWebPage, Person, robots.txt), SaaS-replacement footer pattern. Load-always alongside `style-guide.md`.
- `examples/` — four worked ❌/✅ samples: LinkedIn (text + carousel), X (single + Premium long-form + thread), Reddit (r/SaaS case study), Product Hunt (full five-piece launch package).
- `references/seo-article.md` — March 2026 core update callout: 71% of affiliate sites took a visibility hit, 24% of top-10 pages dropped out of the top 100. Pushes back on thin comparison/affiliate briefs.
- `SKILL.md` Part 1.3 — AI search layer treated as a first-class concern alongside Google.
- `references/style-guide.md` "Why these rules exist" — explains the mechanism behind each style flag (perplexity-based detectors, em-dash over-production, "Not X, but Y" defaults, falsifiable specifics for E-E-A-T and GEO) with canonical sources (September 2025 QRG, December 2025 Helpful Content "Who/How/Why," March 2026 core update, Princeton GEO study, Sedestral 2026, BrightEdge GEO benchmark).
- `SKILL.md` Part 7 — two new operating instructions: step 11 "teach the why, not just the verdict" (cite the mechanism on every flag); step 12 "format every response as production-grade Markdown" per `output-formatting.md`.
- `SOURCES.md` — bibliography of every primary and secondary source the skill draws from, grouped by Google/SEO authorities, GEO/AEO research, AI-detection mechanisms, platform-algorithm primaries, industry studies, and compliance regulation. Each entry pairs source + date + which file uses it, so any flag can be traced back to its mechanism.

### Changed
- Monolithic `SKILL.md` split into progressive-disclosure structure: ~240-line `SKILL.md` (universal context — search/AI landscape, E-E-A-T, research methodology, routing) plus `references/` directory loaded on demand.
- Repositioned from "junior writer" to "senior content strategist + writer" across SKILL.md and README. Reflects what the skill replaces: Surfer SEO, Clearscope, Frase, MarketMuse, Copy.ai/Jasper, Originality.ai/GPTZero, Outranking, AthenaHQ/Profound, WriterAccess (~$400–$2,500/mo of paid SaaS).
- README hero + "What it replaces (free vs. paid)" comparison table mapping pubcraft to the paid stack it makes optional.
- YAML `description` rebalanced to <1024 chars while adding YouTube/podcast/Ghost/AEO triggers.

## [0.3.0] — 2026-04-28

### Added
- Part 10 — Cross-Platform Reference Tables: AI-content policy and community sentiment (18-platform table), format quick-reference (limits, optimal lengths).
- EU AI Act (effective Aug 2, 2026) disclosure obligations covered as a publisher-side rule.
- Dev.to / Hashnode reference: Hashnode-on-your-domain canonical strategy for SEO; AI-content reception specific to developers (hallucinated APIs are unforgivable).
- Medium reference: Boost as the only meaningful distribution lever, +5% external-source bonus (Oct 2025), AI-only-earning ban.
- Hacker News reference: front-page score formula, second-chance pool, Show/Ask/Launch HN conventions.

## [0.1.0] — 2026-04-28

### Added
- E-E-A-T checklist for YMYL on-page requirements.
- Source quality hierarchy (Tier 1–4).
- Hallucinated-statistic verification protocol.
- Banned-words list (Tier 1, 2, 3) and banned structural patterns.
- Pre-writing research protocol with information-gain check.
- Article structure guidance by intent type.
- 2025-current schema markup recommendations (Article in, HowTo out, FAQ caveats).
- Compliance handling for financial, investment, medical, legal, insurance, cannabis verticals.
- Template disclaimer block for regulated content.
