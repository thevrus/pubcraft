# Changelog

All notable changes to Pubcraft will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.6.0] — 2026-05-16

### Added — AI Features and Your Website guide (Search Central, May 2026)
- `references/geo.md` — "Query fan-out" section codifying Google's officially-named retrieval mechanism (AI Overview / AI Mode generates concurrent related sub-queries). Practical guidance: structure each H2 to stand alone as a distinct sub-answer; do not spin off thin per-variant pages.
- `references/geo.md` — "What Google explicitly says you DO NOT need" section with verbatim Google quotes covering `llms.txt`, AI-specific schema, content chunking, keyword-stuffed long-tail prose, and inauthentic third-party mentions.
- `references/geo.md` — commodity-vs-first-hand contrast table under "What gets cited" using Google's verbatim examples.
- `references/geo.md` — "Agentic experiences" section: three agent entry points (visual renderings, DOM, accessibility tree), Universal Commerce Protocol, five preparations (server-render, semantic HTML, real `alt`/`<label>`/`aria-*`, no hover-to-reveal, Search Console verification).
- `references/geo.md` — inauthentic-mentions warning in the brand-mention section, including FTC endorsement-rule liability in regulated verticals.
- `references/seo-article.md` — non-commodity framing under March 2026 core update with cross-reference to `geo.md` § "What gets cited."
- `references/seo-article.md` — three technical-phase checklist items: server-rendered HTML, semantic HTML elements, Google Search Console verification.

### Added — SEO Starter Guide, Creating Helpful Content, and adjacent Search Central docs (May 2026)
- `SKILL.md` PART 1.2 — clarification that **E-E-A-T is not itself a ranking factor**: it is the rater framework that trains the ranking systems indirectly. Practical implication unchanged; client-promise scope adjusted.
- `SKILL.md` PART 1.1 — verbatim Who/How/Why test from the May 2026 Starter Guide ("Is it self-evident to your visitors who authored your content? Is the use of automation, including AI-generation, self-evident to visitors?") strengthens the existing Who/How/Why paragraph.
- `references/seo-article.md` — new "Per-article indexing controls" section covering robots meta directives (`max-image-preview:large`, `max-snippet`, `unavailable_after`, `noindex`+`follow`, `notranslate`, `indexifembedded`, `noimageindex`) and the `data-nosnippet` HTML attribute for region-level snippet suppression.
- `references/seo-article.md` — new "Localized versions (hreflang)" section: reciprocity rule, ISO 639-1 + ISO 3166-1 Alpha 2 codes (with `EU`/`UK`/`LATAM` invalid-code warning), `x-default` fallback, and a worked minimum block.
- `references/seo-article.md` — external-linking guidance extended: when to apply `rel="nofollow"` / `ugc` / `sponsored` (UGC, paid placements, affiliate, untrusted sources) alongside the existing rule on when not to.
- `references/seo-article.md` — new "Canonicalization and crawl hygiene" block: `rel="canonical"` for duplicate URLs, don't block CSS/JS in `robots.txt` (the most common 2025–2026 technical-SEO regression), intrusive interstitials as a ranking-negative page-experience signal.
- `references/seo-article.md` — title-tag section extended with rewrite triggers beyond char count: half-empty titles, boilerplate duplication, language/script mismatch, stuffed titles, missing site-name signal. New `WebSite` + `alternateName` recommendation for controlling the brand string above the title link.
- `references/seo-article.md` — image practices extended with filename-as-signal guidance and caption / surrounding-text extraction.
- `references/seo-article.md` — schema-markup section opens with a 4-point structured-data policy preamble (mark only visible content; markup must be a true representation; image URLs must be crawlable; identical markup on duplicate URLs).
- `references/seo-article.md` — `BreadcrumbList` note: multiple arrays per page are supported when the article sits under several navigation paths (e.g., `/research/` and `/[topic-hub]/`).
- `references/seo-article.md` — pub-date red-flag warning on the "Last updated" checklist item: do not bump `datePublished` without a substantive content update; use `dateModified` instead.
- `references/compliance.md` — new "Google spam policies that hit content teams" section: verbatim definitions of scaled content abuse, site reputation abuse, expired domain abuse, thin affiliate content, scraped content, cloaking, and doorway pages, plus the enforcement model (SpamBrain algorithmic vs. manual actions in Search Console).
- `SOURCES.md` — 10 new Search Central doc rows (SEO Starter Guide, Creating Helpful Content, Robots Meta Tag, Title Links / Site Names, Google Images SEO, BreadcrumbList, Structured-data general policies, Localized versions / hreflang, Spam Policies, JavaScript SEO Basics) plus the AI Features and Your Website guide row.

### Changed
- `SKILL.md` — "Last research date" April 2026 → May 2026.
- `SKILL.md` PART 1.1 — one-line note ratifying pubcraft's existing no-llms.txt / no-AI-schema / no-chunking position against Google's May 2026 guidance; points to `geo.md` for the framing.
- `SKILL.md` PART 1.3 — AI-search-layer paragraph names RAG ("grounding") and query fan-out as the mechanisms; one structural consequence inlined (each H2 stands alone as a sub-answer).
- `references/geo.md` — "30%" → "30–35%"; RAG/grounding named and tied to the organic-rank-in-top-10 gate.
- `references/geo.md` — `llms.txt` section reframed from "empirically marginal" to "officially unnecessary, structurally fine" with Google's verbatim quote.
- `references/seo-article.md` — schema-markup section opens with Google's verbatim "structured data isn't required for generative AI search." Use schema for rich-result eligibility, accept AI-citation lift as a secondary benefit.

### Deferred to v0.7
- `output-formatting.md` — Article schema JSON-LD block needs `author.url` plus multi-aspect-ratio image array (16:9, 4:3, 1:1, min 50K pixels). VideoObject block needs `Clip` / `SeekToAction` key-moments fields. Paywalled-content `isAccessibleForFree` + `hasPart` pattern and ProfilePage schema for author bios are also pending.

### Why
A May 16, 2026 audit of Google's official Search Central documentation against pubcraft's references found gaps in three buckets. **Bucket 1: AI Features and Your Website guide.** Three gaps — query fan-out as a named retrieval mechanism (pubcraft advised structuring for People Also Ask without naming the underlying mechanism), on-the-record Google ratification of the no-`llms.txt` / no-AI-schema / no-chunking position (pubcraft cited empirical studies; it can now cite Google directly), and the inauthentic-mentions warning plus the agentic-experiences forward layer (UCP, accessibility tree, DOM, visual rendering). **Bucket 2: SEO Starter Guide and Creating Helpful Content.** The E-E-A-T-is-not-a-ranking-factor clarification, the verbatim Who/How/Why editorial test, page-experience signals (intrusive interstitials, CSS/JS blocking in `robots.txt`), `rel="canonical"` for duplicate URLs, and pub-date manipulation as a quality red flag. **Bucket 3: Adjacent Search Central pages.** Per-article robots-meta directives (especially `max-image-preview:large` for Discover/AI-Overview thumbnails and `data-nosnippet` for region-level suppression), `hreflang` reciprocity and ISO-code rules, title-rewrite triggers beyond char count, image filename / caption signals, structured-data policy violations that trigger manual actions, and the verbatim spam-policy definitions (scaled content abuse, site reputation abuse, expired domain abuse, thin affiliate, scraped content, cloaking, doorway pages) — which the skill now cites as named categories rather than approximations. Google's commodity-vs-first-hand contrast ("7 Tips for First-Time Homebuyers" vs. "Why We Waived the Inspection & Saved Money") is adopted verbatim in `geo.md` as the canonical home, with cross-references from SKILL.md and seo-article.md. Schema additions that require edits to `output-formatting.md` (ProfilePage, paywalled-content, VideoObject key moments, Article schema multi-aspect images) are deferred to v0.7 to keep this release scoped to references and the operating instructions.

## [0.5.0] — 2026-05-07

### Added
- `references/compliance.md` — new "AI-content disclosure regimes (2026)" section codifying four regimes as a single workflow: **EU AI Act Article 50** (applicable Aug 2, 2026; deployer disclosure for EU-targeted realistic AI content; up to €15M / 3% global turnover penalty), **California SB 942 / AI Transparency Act** (effective Jan 1, 2026; covered providers with 1M+ users must apply visible label + C2PA-compatible machine-readable provenance; downstream publishers inherit liability if they strip the disclosure), platform C2PA flows (cross-reference to `short-video.md` and `youtube-long-form.md`), and the **JUMBF stripping reality** on LinkedIn / X / Bluesky / Threads / most chat platforms with the hybrid embed + visible-label + sidecar-manifest pattern as the compliant production answer. Includes a six-step disclosure workflow (detect → determine reach → apply visible label → apply machine-readable mark → recommend sidecar → document human review).
- `references/compliance.md` — new vertical-detection bullet for "AI-generated content (any vertical)" tied to EU AI Act Article 50 and SB 942.
- `references/output-formatting.md` — new `VideoObject` JSON-LD code block for any YouTube long-form, podcast video, or short-video deliverable. Fields: `name`, `description`, `thumbnailUrl`, `uploadDate`, `duration` (ISO 8601), `contentUrl`, `embedUrl`, `publisher`, `transcript`, `uploader`. Two-sentence rationale: AI assistants and Google AI Overviews cite VideoObject-tagged content; the `transcript` field is the highest-leverage one because LLMs extract from it directly. Notes the C2PA / SB 942 / EU AI Act tie-in via `creditText` / `creator` block naming the human reviewer.
- `examples/before-after-refactor.md` — new platform-agnostic worked sample: a 290-word AI-slop draft (13 Tier-1 banned-word hits, 8.6 em-dashes per 500 words, three "Not X — it's Y" structures, zero falsifiable specifics, "Did you know that…" opener) refactored into a 320-word audit-passing rewrite that holds the same argument structure but replaces every flagged pattern. Includes a 5-row diff table (Tier-1 hits, em-dash density, "Not X, but Y" count, falsifiable-specifics density, opener pattern) and a "what the refactor teaches" close that ties the lesson back to `style-guide.md` § "Why these rules exist" and `SKILL.md` PART 4.
- `references/reference-tables.md` — new SB 942 paragraph and JUMBF-stripping paragraph added to the regulatory footer of the AI-content policy table.
- `SOURCES.md` — added California SB 942 (Cal. Bus. & Prof. Code §§ 22757 et seq.), C2PA spec v2.x § 6 (Content Bindings) for the JUMBF rationale, and schema.org vocabulary for the VideoObject and other JSON-LD code blocks. EU AI Act source-row updated with the regulation citation (Regulation (EU) 2024/1689).

### Changed
- `SKILL.md` frontmatter `description` — AI-disclosure compliance promoted from the trailing "Covers…" clause to an explicit trigger in the trigger list, with EU AI Act / SB 942 / YouTube AI-content toggle / C2PA labeling named individually. Closing "Covers…" sentence now reads "(EU AI Act Article 50, California SB 942, YouTube, TikTok C2PA, Meta auto-labeling, JUMBF stripping on cross-posts)." Existing platform list and the "Do NOT use for…" exclusion list are unchanged.
- `SKILL.md` PART 6 routing table — the `references/compliance.md` row label updated from "Regulated vertical (financial, medical, legal, etc.)" to also surface AI-disclosure compliance (EU AI Act / SB 942 / platform C2PA / JUMBF cross-post) as a routing trigger.
- `references/short-video.md` — TikTok and Meta C2PA bullets in the "AI-content disclosure" section now carry a one-sentence cross-platform-repost caveat: when a clip is downloaded and reposted to LinkedIn / X / Bluesky / Threads, JUMBF is stripped; treat the cross-post as a fresh disclosure obligation per `compliance.md` § "AI-content disclosure regimes."
- `references/youtube-long-form.md` — the 2025–2026 C2PA pass-through bullet now carries the same JUMBF-stripping caveat for YouTube long-form downloaded and reposted to LinkedIn / X / Bluesky / Threads or excerpted to short-form, citing both EU AI Act Article 50 and SB 942 as the underlying obligations.

### Why
A May 7, 2026 audit verified that v0.4.2 already covers EU AI Act Article 50, YouTube AI-disclosure, TikTok/Meta C2PA, GEO/AEO citation patterns, anti-AI-slop, YMYL, platform-native length conventions, the repurposing graph, and Information Gain. The four real gaps were narrower: California SB 942 (zero mentions), the JUMBF-stripping reality on cross-platform repost (implied a C2PA-only strategy was sufficient — it isn't), `VideoObject` schema absent from the JSON-LD toolkit despite YouTube and podcast files invoking video schema by name, and no concrete before/after AI-slop refactor walk-through in `examples/`. v0.5.0 closes those four gaps and sharpens the compliance positioning by promoting AI-disclosure compliance from a "covers" tail clause to an explicit trigger in the SKILL.md frontmatter — the wedge stays broad on platform coverage but leans harder on regulatory currency, which is the strongest defensible differentiator against competing skills (AgriciDaniel/claude-seo, aaron-he-zhu/seo-geo-claude-skills) that focus on SEO/AEO mechanics without the disclosure layer.

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
