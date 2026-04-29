# Changelog

All notable changes to Pubcraft will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
