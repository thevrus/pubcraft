# SEO article structure & production checklist

Load this reference when drafting a long-form article, blog post, guide, comparison, how-to, or pillar page intended to rank in Google.

## March 2026 core update — what to flag to the user

The March 2026 core update was the most volatile since 2023 (3.2× the volatility of December 2025). Two patterns from that update should shape advice on any new article:

- **Sites with original research and named credentialed authors gained 15–25% organic visibility.**
- **Thin affiliate / comparison / aggregator pages collapsed:** ~71% of affiliate sites took a visibility hit; 24% of top-10 pages dropped out of the top 100. If the user's brief is a comparison or roundup page, the page must contain genuine first-party testing or it is structurally exposed.

If the user is asking for a thin comparison/affiliate-style page, push back: recommend either committing to original testing/data or reframing as a different content type.

Google's May 2026 AI-Features guidance reframes this in plain language: write **"non-commodity content that's helpful, reliable, and people-first."** See the commodity-vs-first-hand contrast table in `references/geo.md` § "What gets cited." If a brief admits only the commodity treatment, surface the gap before drafting and offer the user a path to a real angle: a worked scenario, a proprietary number, a named expert.

## Length by intent

These are working ranges, not minimums. Padding to length is itself a scaled-content-abuse signal.

- **Informational/definitional** ("What is X?"): 1,200–1,800 words. Direct answer in the first 60 words for AI Overview eligibility.
- **Comparison** ("X vs. Y"): 1,800–2,800 words with a real comparison table, scenario examples, decision framework.
- **How-to/process**: 1,500–2,500 words with numbered steps, screenshots, downloadable artifact.
- **Transactional/product page**: 800–1,400 words. Heavy on specific eligibility and tradeoffs, light on filler.
- **Pillar/hub guide**: 3,000–5,000 words, only when you have the depth.
- **Original-data report**: 3,000–6,000 words when reporting on first-party data. See "Original-data articles" below.

## Original-data articles

When the user has access to first-party data — internal analytics, support-ticket analysis, a proprietary survey, A/B test results, anonymized customer-database aggregations, internal benchmarks — default to this format unless they decline. It's the highest-trust E-E-A-T signal a site can produce, and AI assistants disproportionately cite it.

**The five required elements:**

1. **A `Dataset` JSON-LD schema** declaring the underlying data (creator, temporalCoverage, spatialCoverage, variableMeasured, license). Citation magnet — see `references/output-formatting.md` for the code block and rationale.
2. **Comparative-baseline framing for every statistic.** Never report a raw number; always pair it with the relevant baseline. Weak: "29.5% of users do X." Strong: "29.5% of [our cohort] do X — 1.35× the rate of [the broader baseline]." A statistic without a baseline is half a citation magnet; with one, LLMs quote the whole construction verbatim.
3. **A methodology block** that names the data source, the time window, the unit of analysis, the inclusion criteria, and how categories were derived. Place near the bottom but link from the article opener.
4. **A Limits sub-block** within the methodology that explicitly acknowledges selection bias, response-rate caveats, generalizability constraints, and what the data does not capture. The single highest-trust signal in an original-data article. Google's Quality Rater Guidelines explicitly reward "careful person seeking out experts" framing — a writer who states their data's limits reads as careful, not promotional.
5. **A "this is what we see, not what we claim" stance** in the prose. Frame findings as observations from your specific population, not universal truths. "Across [N] events in our dataset, we saw…" beats "All [population] do X…"

## On-page metadata: title, description, H1 alignment

The three highest-leverage tags are the most often misconfigured. Treat as a pre-publication blocker.

**Title tag**
- 50–60 characters / ~575 px. Past the budget gets truncated in SERPs.
- Front-load the primary keyword in the first 30 characters.
- Include one differentiator the SERP doesn't already have (a proprietary cohort size, a fresh date, a numeric specificity, a brand modifier when warranted).
- Sentence case for editorial sites; Title Case for traditional publishers and product pages. Match site convention.

**Meta description**
- 120–158 characters. Mobile truncates around 120; desktop allows around 158.
- Problem-Solution-CTA in one sentence: what the user is trying to do, what the article delivers, the lift they get.
- Primary keyword in the first 90 characters so the snippet bolds it before truncation.
- Skip if you don't have a strong one. Google rewrites missing descriptions from page content; that's often better than a weak custom description.

**H1↔title alignment**
- The H1 should share the primary keyword phrase with the title. Different wording is fine; the keyword anchor must match.
- When title and H1 diverge, Google rewrites the displayed SERP title from the H1 about 61% of the time (Zyppy 2024 study, ~80,000 SERPs). Aligning them protects what gets shown.
- One H1 per page; primary keyword appears naturally.

**Other title-rewrite triggers** (Google reads from `<title>`, H1, `og:title`, large prominent text, anchor text, and WebSite structured data; any of these can override the `<title>`):
- Half-empty titles like `| Site Name` or `Untitled — Site Name`.
- Boilerplate-duplicated titles across many pages.
- Language or script mismatch between title and body content.
- Stuffed titles (>3 repeated keywords).
- Brand-name signal absent or inconsistent. Define your site name once via `WebSite` structured data on the home page with an ordered `alternateName` list; this controls the brand string shown above the title link in SERPs and AI citations.

For original-data reports and recurring topic hubs, the title should preserve the ownable differentiator (the cohort size, the data window, the proprietary methodology). Generic titles cede the SERP to aggregators; specific titles win citations from AI assistants.

## Header structure

- **One H1 only**, containing the primary query phrase naturally.
- **H2s** correspond to subtopics that map to People-Also-Ask and "related searches." Use a real SERP scrape, not assumptions.
- **H3s** under H2s for sub-questions and stepwise breakdowns.
- Avoid H4+ unless genuinely needed; deep nesting is an SEO-template tell.

## Featured snippet / AI Overview optimization

- Place a **40–60 word direct answer** immediately after the H1 (above any H2).
- Use a **40–60 word answer paragraph** under each H2 question, then expand.
- Include at least one **real comparison table** for comparison content.
- For lists, use 5–8 items, each a complete short sentence (snippet-friendly).

For optimizing for AI search engines (ChatGPT, Perplexity, Google AI Overviews citations), also load `references/geo.md`.

## Schema markup (post-2025 reality)

Google's May 2026 guidance is explicit: **"Structured data isn't required for generative AI search."** No AI-Overview-specific schema type exists, and none is coming. Use schema the same way you used it before AI search, to earn traditional rich-result eligibility. AI-citation lift is a secondary benefit (real, but not the reason to ship the JSON-LD).

**Structured-data policy violations that trigger manual actions** (Search Central):
1. **Mark up only content visible to readers.** Hiding FAQs in collapsed accordions and marking them up regardless violates the spam-policy rule "Don't mark up content that is not visible to readers of the page."
2. **Markup must be a true representation of the page.** An Article schema on a thin tag-archive page, or a Dataset declaration on a page with no actual dataset, is a misrepresentation.
3. **All image URLs in structured data must be crawlable and indexable.** Blocking them in `robots.txt` or putting them behind authentication invalidates the rich-result eligibility.
4. **Place identical markup on every duplicate URL** if the same content lives at multiple URLs (en/fr variants, AMP, print views).

- **Use Article (or NewsArticle for timely posts)** with author, datePublished, dateModified, publisher, image. Core to AI Overview eligibility.
- **Use BreadcrumbList.** Still supported. Multiple `BreadcrumbList` arrays per page are allowed when a page is reachable via several navigation paths — common when the article sits under both `/research/` and `/[topic-hub]/`.
- **Use Organization schema sitewide** with logo, sameAs, address, contactPoint.
- **Use Person schema on author bio pages** with credentials, sameAs, jobTitle, knowsAbout.
- **Use Dataset schema whenever the article reports on first-party data.** Citation magnet — see `references/output-formatting.md` for fields and rationale.
- **FAQPage schema:** Still valid but Google has restricted FAQ rich result *visibility* primarily to government and well-known health sites since August 2023. Add FAQ schema only if you have genuine on-page FAQs. When you do, build the question set from People-Also-Ask on the target query (6–8 questions), not invented prompts. PAA-mined FAQs are AI-Overview citation magnets even when they don't earn a SERP rich result. Each answer 50–150 words, fact-grounded in the article's own data or sources.
- **HowTo schema: effectively deprecated.** Google removed HowTo rich results September 13, 2023. Do not add HowTo JSON-LD. Use Article schema and ordered HTML lists instead.
- **Avoid:** Course Info, Estimated Salary, Claim Review, Vehicle Listings (deprecated through Google's June 12, 2025 simplification).

**Schema stacking is fine.** An original-data article may ship with `Article` + `Dataset` + `FAQPage` + `Organization` (plus any vertical-specific type that genuinely applies) in the same document. Each describes a different facet; AI assistants extract from all of them. For vertical-specific types check `schema.org/docs/full.html`. Common picks: `MedicalWebPage` for clinical/health content, `FinancialProduct` for loans/cards/insurance, `RealEstateListing` for property, `Recipe`, `Course`, `Event`, `Product`. Stack alongside `Article`, never replacing it.

## Images, links, performance

**Images:**
- At least one original or licensed hero image per article; original screenshots/diagrams strongly preferred over stock.
- Compressed WebP/AVIF. Specify width/height attributes (CLS).
- Descriptive alt text — never keyword-stuffed.
- Lazy-load below-the-fold images.
- **Filenames are a signal.** `my-new-black-kitten.jpg` is read; `IMG00023.JPG` is not. Use lowercase, hyphenated, descriptive filenames.
- **Captions and surrounding text matter.** Google extracts image subject matter from `<figcaption>`, image titles, and the prose around the `<img>`. Place each image near the paragraph that explains it.

**Internal linking:**
- Length-scaled: 3–6 contextual links for ≤1,500 words; 6–10 for 1,500–3,000; 10–15 for 3,000+ original-data reports and pillar pages.
- Descriptive anchor text (never "click here"). Vary anchors across the page: keyword-match ~30%, partial-match ~40%, descriptive or branded ~30%. Avoid identical anchors pointing to the same destination.
- Build topic clusters: pillar page linking down to spokes, each linking back up.
- Link to author bio and disclosures from every article.

**Charts and tables:**
- Pair every SVG/Canvas chart with a parallel HTML table carrying the same numbers. AI assistants extract HTML tables far more reliably than they parse SVG. Either visible or visually hidden but crawlable (`<table aria-label="..." class="visually-hidden">`).
- Bar widths must represent the underlying value, not normalize to the top value in the set. A bar showing 66% should occupy 66% of the track, not 99% because it happens to be the largest value charted. If a chart is intentionally indexed (top = 100), label it that way.
- Comparison tables get reformatted by every major LLM as authoritative summaries. Use real comparison tables on comparison content; the table format itself is a citation magnet.

**External linking:**
- Tier-1 sources should open in new tab with `rel="noopener"`.
- Do not nofollow legitimate authoritative outbound links — outbound linking to good sources is a positive helpful-content signal.
- **Do** apply `rel="nofollow"` (or `ugc` / `sponsored`) to: user-generated content links (comments, forum posts, profile fields), paid placements, affiliate links, and any link to a source you cannot vouch for. Google's May 2026 Starter Guide names this explicitly: untrusted outbound links without `nofollow` are a passable spam signal.

**Canonicalization and crawl hygiene:**
- Every page accessible at more than one URL (tracking params, alternate paths, http/https, www/non-www) must declare a `<link rel="canonical" href="…">` to the preferred URL. Without it, link equity and AI-citation weight fragment across duplicates.
- Do **not** block CSS, JavaScript, or image resources in `robots.txt`. Google must render the page the way a user does; blocking renderables hides the page from the indexer. The most common technical-SEO regression in 2025–2026 audits.
- Avoid intrusive interstitials, full-screen modals on page load, and ad layouts that push main content below the fold on mobile. Google explicitly flags these as a ranking-negative page-experience signal in the Starter Guide.

**Core Web Vitals targets (April 2026):**
- LCP: < 2.5s
- INP: < 200ms (replaced FID March 2024)
- CLS: < 0.1

INP is the metric most sites currently fail; it requires JavaScript discipline. Lazy-load third-party scripts; defer non-critical work.

## Localized versions (hreflang)

If the article ships in multiple languages or regional variants, declare the alternates with `hreflang`. Three rules silently void the entire `hreflang` block when broken:

- **Reciprocity.** Every page in the set must point to every other page in the set, including itself. If `en-US` links to `fr-FR` but `fr-FR` doesn't link back, Google ignores both tags.
- **ISO codes only.** Language is **ISO 639-1** (`en`, `fr`, `pt`); region is **ISO 3166-1 Alpha 2** (`US`, `FR`, `BR`). `EU`, `UK`, and `LATAM` are not valid; use `GB` for the United Kingdom. Region-only without language is invalid.
- **`x-default` fallback.** Include `<link rel="alternate" hreflang="x-default" href="…">` pointing to the page that handles unmatched users (typically the global/English version with a language-picker).

Minimum block for an English-and-French article:

```html
<link rel="alternate" hreflang="en-US" href="https://example.com/article/" />
<link rel="alternate" hreflang="fr-FR" href="https://example.com/fr/article/" />
<link rel="alternate" hreflang="x-default" href="https://example.com/article/" />
```

Place in `<head>`, in the HTTP header, or in the XML sitemap. Pick one location and apply consistently. Per-page canonical tag should still point to the same language version, not across languages.

## Per-article indexing controls (robots meta + on-page directives)

Set these at the article level, not site-wide. They give the writer surgical control over how Google and AI assistants treat the page:

- **`<meta name="robots" content="max-image-preview:large">`** — required for Google Discover eligibility and improves AI Overview thumbnail selection. Default to `large` for any article with a hero image.
- **`<meta name="robots" content="max-snippet:-1">`** — `-1` removes the SERP-snippet length cap. Use for in-depth pieces you want fully extractable; use a positive integer to cap snippet length on press-release-style pages.
- **`<meta name="robots" content="unavailable_after:YYYY-MM-DDThh:mm:ss±hh:mm">`** — auto-deindex after a date. Use for event pages, time-limited offers, and announcements that age into misleading.
- **`<meta name="robots" content="noindex">`** — on staging, thank-you pages, internal-search results, and thin tag-archive pages. Combine with `follow` if internal links from the page should still flow.
- **`<meta name="robots" content="notranslate">`** — when translation produces misleading or non-equivalent meaning (regulated content, branded terminology).
- **`data-nosnippet`** HTML attribute on a specific `<span>`/`<div>`/`<section>` — blocks that region from snippet extraction without de-indexing the page. Use to keep a quoted client name, a price, or a regulated disclaimer out of SERP snippets while leaving the rest extractable.
- **`indexifembedded`** alongside `noindex` — allows the page to appear when embedded in another indexed page (third-party widget host pattern).
- **`noimageindex`** — keep page indexed but exclude its images from Google Images. Use sparingly; original images are usually a positive signal.

These are page-level signals, not robots.txt directives. Robots.txt blocks crawling (resulting in a snippet-free SERP entry); robots meta blocks indexing or snippet extraction *after* the crawler has fetched the page.

## URL and IA placement

Where the article lives shapes how it compounds. Three viable structures, in order of strategic weight:

- **`/research/[slug]`** — best when the article is part of a series of original-data reports. Compounds across future reports and creates an entity association ("this site publishes original research") that competitors can't easily replicate. Default for original-data formats.
- **`/[topic-hub]/[slug]`** — best when the topic deserves a permanent annually-updated hub (regulatory explainers for evergreen rules, category guides, durable how-tos). Captures the head-term query directly.
- **`/blog/[slug]`** — default for one-off pieces and timely commentary. Captures long-tail well but compounds less.

The decision is hard to reverse without redirect work, so commit to a structure before publication. For original-data reports specifically, default to `/research/` even on the first one — the hub establishes itself faster than retrofitting later.

---

## End-to-end production checklist

Before delivering any article, every item must be checked.

**Research phase**
- [ ] Search intent verified against current SERP for the target query.
- [ ] Information gain identified (what's new vs. top 10).
- [ ] Minimum 4 Tier-1/Tier-2 sources identified with URLs.
- [ ] All numbers verified against primary sources today.
- [ ] Quote or sign-off from a credentialed source obtained (where possible).

**Drafting phase**
- [ ] Direct 40–60 word answer in the lead.
- [ ] H2/H3 structure maps to PAA and related queries.
- [ ] At least one original asset (table, screenshot, scenario, chart) present.
- [ ] All statistics inline-cited with hyperlinks.
- [ ] First-person/second-person voice; lived-experience detail present.
- [ ] No Tier-1 banned word.
- [ ] Em-dash count below one per ~500 words.
- [ ] No "Not X, but Y" constructions.
- [ ] Sentence-length variance visible at a glance.

**On-page metadata phase**
- [ ] Title tag 50–60 chars, primary keyword in first 30 chars, includes a differentiator.
- [ ] Meta description 120–158 chars, primary keyword in first 90 chars, Problem-Solution-CTA pattern.
- [ ] H1 shares the primary keyword with the title (alignment protects the SERP-rewrite path).
- [ ] One H1 per page.
- [ ] URL placement decided (`/research/`, `/[topic-hub]/`, or `/blog/`).

**Charts and tables phase** (when the article includes data visualizations)
- [ ] Every SVG/Canvas chart paired with a parallel HTML table.
- [ ] Bar widths represent the underlying percentage, not normalized to the top value, or the chart is explicitly labeled as indexed.
- [ ] Comparison tables present where the topic admits one.

**Original-data phase (only when reporting first-party data)**
- [ ] Every statistic paired with the relevant baseline (comparative framing).
- [ ] Methodology block names: source, time window, unit of analysis, inclusion criteria, how categories were derived.
- [ ] Limits sub-block acknowledges selection bias, response-rate caveats, what the data does not capture.
- [ ] Findings framed as observations from your population, not universal claims.

**Compliance phase (regulated verticals only — see `references/compliance.md`)**
- [ ] Author byline + reviewer credentials + relevant license IDs present.
- [ ] Required vertical disclaimers present.
- [ ] If rate/price shown: date/time stamp, change-subject-to disclosure.
- [ ] No prohibited language (guaranteed, immediate, government-implication, fiduciary).
- [ ] No discriminatory imagery.
- [ ] Jurisdictional scope statement present.
- [ ] [COMPLIANCE TBD] flag where needed; human review recommended in delivery.

**Technical phase**
- [ ] Article schema (JSON-LD) with author, dates, publisher, image — supplied as a code block.
- [ ] Person schema on author bio (if applicable) — supplied as a code block.
- [ ] BreadcrumbList schema — supplied as a code block.
- [ ] Dataset schema if first-party data is reported — supplied as a code block.
- [ ] Image guidance: WebP/AVIF, width/height set, descriptive alt text, lazy-load.
- [ ] Internal links: 3–6 contextual, descriptive anchors.
- [ ] External links: open in new tab, `rel="noopener"`.
- [ ] No HowTo schema. FAQ schema only if real on-page FAQs exist.
- [ ] "Last updated" / "Last reviewed" dates set. **Do not bump `datePublished` without a substantive content update**; bumping the original publication date is named as a quality red flag in Google's May 2026 helpful-content guidance. Use `dateModified` for refreshes.
- [ ] Server-rendered HTML (content visible without JavaScript execution).
- [ ] Semantic HTML elements (`<article>`, `<main>`, `<nav>`, real `<button>`/`<label>`).
- [ ] Property verified in Google Search Console.

Rationale for the three items above: `references/geo.md` § "Agentic experiences."
