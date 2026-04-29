# Sources

What this skill is based on. Every claim in `SKILL.md` and `references/` traces to one of the sources below. Cite the mechanism, not the verdict — when flagging a draft, name the source so the user can verify or push back.

Sources are grouped by what they support. Dates reflect the version actually referenced; check for newer revisions before treating any number as current.

---

## 1. Google — search quality, ranking, and updates

Used in: `SKILL.md` Part 1, `references/seo-article.md`, `references/style-guide.md`, `references/output-formatting.md`, `references/compliance.md`.

| Source | Date | What it supports |
|---|---|---|
| Google **Search Quality Rater Guidelines** (the QRG, 182 pp.) | September 11, 2025 | E-E-A-T pillar weights, page 124+ on AI content, "rephrased existing content with no original information" = Lowest Quality. The canonical reference for trust-as-dominant-pillar. |
| Google **Helpful Content** "Who, How, Why" framework | December 2025 | Author accountability, AI-disclosure expectation, "value-free production" penalty mechanism. |
| Google **March 2026 core update** | March 2026 | 71% of affiliate sites took a visibility hit; 24% of top-10 pages dropped out of the top 100; sites with original research and named credentialed authors gained 15–25%. |
| Google **March 2024 core update + spam policies** | March 2024 | The reset that ended scaled-AI-content era; baseline for current SpamBrain enforcement. |
| Google **structured-data deprecations** (Course Info, Estimated Salary, Claim Review, Vehicle Listings) | June 12, 2025 | What schema types to *remove*, not add. |
| **Core Web Vitals — INP replaced FID** | March 2024 | Performance targets in `seo-article.md`. |
| **John Mueller** (Google Search Advocate) public statements on `llms.txt` | 2025 | "Search does not use llms.txt for ranking." |

---

## 2. AI search — GEO / AEO / LLMO

Used in: `references/geo.md`, `references/style-guide.md`, `references/seo-article.md`.

| Source | Date | What it supports |
|---|---|---|
| **Princeton GEO study** ("GEO: Generative Engine Optimization," Aggarwal et al.) | 2024–2025 | Citation-magnet content patterns; statistics-with-context cited 3–4× more often. |
| **BrightEdge GEO benchmark** | 2025–2026 | LLM-citation patterns by content type. |
| **Sedestral 2026** | 2026 | ChatGPT referrals convert at ~14.2% vs. ~2.8% for traditional organic. |
| **Semrush** 10M-keyword AI Overview study | 2025 | 34.5% CTR decline at #1 organic when an AI Overview appears; AI Overviews trigger on 88% of informational queries. |
| **Ahrefs** LLM-citation analysis | 2025–2026 | Brand-mention patterns, third-party citation weight. |
| **r/SEO_LLM** ~10K-site `llms.txt` study | March 2026 | 6.8 vs. 6.7 average citations with/without `llms.txt` (p=0.85) — the empirical case for not over-investing in `llms.txt`. |
| **Jeremy Howard** — `llms.txt` proposal | September 2024 | Origin and intent of the `llms.txt` standard. |
| **Forrester** — B2B buying behavior | Q4 2025 | 38% of B2B buyers use AI search before talking to sales (up from 12% in 2024). |
| **Profound, Otterly.ai, AthenaHQ** (LLM-citation monitoring tools) | 2025–2026 | Brand-mention monitoring landscape. |
| Public AI search market-share aggregations (ChatGPT 64.5%, Gemini 21.5%, Perplexity ~6%, Claude ~3%, Grok ~3.4%) | early 2026 | `references/geo.md` market-share table. |

---

## 3. AI detection and style fingerprinting

Used in: `references/style-guide.md`, `references/output-formatting.md`.

| Source | What it supports |
|---|---|
| **Originality.ai** — perplexity + burstiness scoring | Why em-dash density, banned-word frequency, and sentence-length variance get flagged. |
| **GPTZero** — perplexity-based detection | Why high-frequency LLM words push perplexity into the AI-suspect zone. |
| **Copyleaks** — multi-signal detection | Triangulation rationale ("flagged by all three reads as AI to humans too"). |
| Informal corpus comparisons (creator-economy + B2B content, 2024–2026) | "Not X, but Y" appearing in ~3% of LLM output vs. <0.1% of human-edited prose. |
| Public AI-tell discourse on Hacker News, Bluesky, journalism Twitter | Reader-side recognition of *delve, tapestry, robust, intricate, navigate (metaphorical)*, em-dash overuse. |

---

## 4. Platform algorithms — primary / official sources

Used in: `references/linkedin.md`, `references/x-twitter.md`, `references/youtube-long-form.md`, `references/short-video.md`, `references/podcast.md`, `references/alt-social.md`.

| Source | What it supports |
|---|---|
| **`github.com/xai-org/x-algorithm`** — open-source X ranking weights, refreshed ~every 4 weeks since the January 2026 Grok-powered rewrite | Reply ≈ 27× like, conversation ≈ 150× like, bookmark weighting, Premium 2×/4× boosts, Grok sentiment layer reducing reach for negative-toned posts. |
| LinkedIn **"360Brew" model** + March 2026 "Authenticity Update" (independent reporting) | LLM-embedding interest graph replacing network-feed; ~50–60% organic-reach decline vs. 2024; saves and sends as analytics signals. |
| **YouTube official** — title/thumbnail A/B test expansion to three combinations, optimized on watch time per impression (not CTR) | December 9, 2025 |
| **YouTube official** — thumbnail file size cap raised to 50 MB | October 2025 |
| **YouTube official** — mandatory AI/synthetic-content disclosure | May 21, 2025 |
| **YouTube official** — "inauthentic content" rule (renamed from "repetitious content") | July 15, 2025 |
| **Neal Mohan** (YouTube CEO) public statements on satisfaction signals + "AI slop" | 2025–2026 |
| **TikTok C2PA Content Credentials** integration; auto-labeled 1.3B+ videos | January 2025 |
| **Apple Podcasts** — native auto-transcripts (English/French/Spanish/German) | March 5, 2024 |
| **Apple Podcasts** — native video episodes | early 2026 |
| **YouTube** — Weekly Top Podcast Shows chart launch (ranked by watch time) | May 15, 2025 |
| **Ghost 6.0** — native ActivityPub integration; pricing change to $15 / $29 | August 4, 2025 |
| **Spotify** — paid-promotion boost lane added; Comments auto-publish expanded | 2024–2025 |

---

## 5. Industry studies and benchmarks

Used in: `references/podcast.md`, `references/short-video.md`, `references/newsletters.md`, `references/reddit.md`, `references/dev-publishing.md`.

| Source | Date | What it supports |
|---|---|---|
| **Edison Podcast Metrics** (US podcast platform share) | October 2024 | YouTube ~31% > Spotify ~27% > Apple ~14–15%. |
| **Deloitte** — Digital Media Trends / podcast-revenue estimates | Fall 2025 / 2026 | 51% Americans watched a video podcast; ~$5B global ad revenue. |
| **Acast** *Podcast Pulse* | 2025 | Audio = trust/connection; video = reach. |
| **Podcast Marketing Academy / Lower Street** video-cost study | 2025 | Video alongside audio costs +77% and ~50% more staff. |
| **Listen Notes** "NotebookLM Detector" | 2024 | 280+ AI-generated podcasts flagged; founder Wenbin Fang public position. |
| **OpusClip** viral-video analysis (118k+ videos) | 2025–2026 | Hook → Problem → Solution → CTA architecture; 21–34s TikTok sweet spot. |
| **Beehiiv** *State of Newsletters 2026* | 2026 | Paid-sub revenue $8M (2024) → $19M (2025); 66-day median time-to-first-dollar. |
| **Athenic** alt-social engagement study | 2025 | Bluesky engagement ~4.2%, ~2.8× X. |
| **SimilarWeb** Reddit referral-traffic data | 2025 | Reddit referral traffic to SaaS sites doubled YoY. |
| **TechContentPro** dev-publishing benchmark | 2026 | Hashnode-on-your-domain canonical strategy. |
| **ContentIQ Analytics** cross-post study | 2025–2026 | ~65% organic-traffic drop on uncanonical cross-posts over 6 months. |

These are the named third-party studies referenced in the skill. Where a number was widely reported but not pinned to a single primary source ("~30% of search activity is AI-assisted by April 2026"), the skill cites it as a market estimate, not a study.

---

## 6. Compliance and disclosure

Used in: `references/compliance.md`, `references/short-video.md`, `references/youtube-long-form.md`, `references/podcast.md`, `references/reference-tables.md`.

| Source | Effective date | What it supports |
|---|---|---|
| **EU AI Act** — Article 50 transparency obligations | August 2, 2026 | Mandatory disclosure for AI-generated content appearing realistically human-authored that wasn't editorially reviewed; fines up to €15M or 3% global turnover. Treated as a *publisher* obligation regardless of platform enforcement. |
| **C2PA Content Credentials 2.1** | rolling 2024–2026 | Auto-labeling pipeline used by TikTok, Meta, YouTube. |
| **YouTube** AI/synthetic-content disclosure rules | March 2024 (toggle) → May 21, 2025 (mandatory) → July 15, 2025 (inauthentic-content rule) | Disclosure timeline. |
| **TikTok** Community Guidelines on synthetic media | 2024–2026 | Mandatory disclosure for realistic AI; deepfakes of real people banned outright. |
| **Podcasting 2.0** — proposed generative-AI disclosure tag in RSS namespaces | 2025–2026 (voluntary) | Emerging norm reference. |

---

## 7. Pattern sources — practitioners and publications cited as exemplars

Not authorities to *cite* but exemplars referenced for working 2026 patterns. Listed so the user can audit whether the comparison is fair.

- **Newsletters / Ghost migrations:** Casey Newton's *Platformer*, *404 Media*, *The Browser*, *Garbage Day*, *Blood in the Machine*. Lenny Rachitsky remains on Substack. Ben Thompson's *Stratechery* runs on a custom stack with Ghost-adjacent infrastructure.
- **Operator/founder podcasts:** Lenny's Podcast, Acquired (Ben Gilbert & David Rosenthal), Stratechery, BG2, All-In, Tim Ferriss Show, Patrick O'Shaughnessy's *Invest Like the Best*.
- **YouTube long-form pattern exemplars:** MrBeast (5-second-hook stair-step), Veritasium (open-loop), Marques Brownlee (minimalist thumbnail), Ali Abdaal, Asianometry, Karpathy, Fireship, Justin Welsh.
- **Reddit branded-subreddit pattern:** Eric Eden / "Thinking Deeply AI" — 25K subscribers and 21M reads in 11 months.
- **Substack content-moderation reference incidents:** December 2023 Nazi-newsletter incident, recurring push-notification controversies — context for the Ghost migration narrative.

---

## How to use this file

- When the skill flags a draft, **name the source from this file** in the explanation. "This trips Originality.ai's perplexity scoring" beats "this is bad."
- When a number in `SKILL.md` or `references/` looks suspicious, **trace it back here**. If it isn't here, it's likely an industry estimate rather than a primary source — push back accordingly.
- Numbers age fast. Before treating any 2025–2026 figure as current, check for a newer revision of the underlying source (especially Google QRG releases, YouTube policy updates, EU AI Act enforcement guidance, Ghost releases).
- Anything not on this list is either common practice, derivable from the platform's own docs, or operator pattern-matching — not a citable claim.
