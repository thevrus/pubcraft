# SEO article structure & production checklist

Load this reference when drafting a long-form article, blog post, guide, comparison, how-to, or pillar page intended to rank in Google.

## March 2026 core update — what to flag to the user

The March 2026 core update was the most volatile since 2023 (3.2× the volatility of December 2025). Two patterns from that update should shape advice on any new article:

- **Sites with original research and named credentialed authors gained 15–25% organic visibility.**
- **Thin affiliate / comparison / aggregator pages collapsed:** ~71% of affiliate sites took a visibility hit; 24% of top-10 pages dropped out of the top 100. If the user's brief is a comparison or roundup page, the page must contain genuine first-party testing or it is structurally exposed.

If the user is asking for a thin comparison/affiliate-style page, push back: recommend either committing to original testing/data or reframing as a different content type.

## Length by intent

These are working ranges, not minimums. Padding to length is itself a scaled-content-abuse signal.

- **Informational/definitional** ("What is X?"): 1,200–1,800 words. Direct answer in the first 60 words for AI Overview eligibility.
- **Comparison** ("X vs. Y"): 1,800–2,800 words with a real comparison table, scenario examples, decision framework.
- **How-to/process**: 1,500–2,500 words with numbered steps, screenshots, downloadable artifact.
- **Transactional/product page**: 800–1,400 words. Heavy on specific eligibility and tradeoffs, light on filler.
- **Pillar/hub guide**: 3,000–5,000 words, only when you have the depth.

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

- **Use Article (or NewsArticle for timely posts)** with author, datePublished, dateModified, publisher, image. Core to AI Overview eligibility.
- **Use BreadcrumbList.** Still supported.
- **Use Organization schema sitewide** with logo, sameAs, address, contactPoint.
- **Use Person schema on author bio pages** with credentials, sameAs, jobTitle, knowsAbout.
- **FAQPage schema:** Still valid but Google has restricted FAQ rich result *visibility* primarily to government and well-known health sites since August 2023. Add FAQ schema only if you have genuine on-page FAQs; do not invest heavily in it as a ranking play.
- **HowTo schema: effectively deprecated.** Google removed HowTo rich results September 13, 2023. Do not add HowTo JSON-LD. Use Article schema and ordered HTML lists instead.
- **Avoid:** Course Info, Estimated Salary, Claim Review, Vehicle Listings (deprecated through Google's June 12, 2025 simplification).

## Images, links, performance

**Images:**
- At least one original or licensed hero image per article; original screenshots/diagrams strongly preferred over stock.
- Compressed WebP/AVIF. Specify width/height attributes (CLS).
- Descriptive alt text — never keyword-stuffed.
- Lazy-load below-the-fold images.

**Internal linking:**
- 3–6 contextual internal links per article with descriptive anchor text (never "click here").
- Build topic clusters: pillar page linking down to spokes, each linking back up.
- Link to author bio and disclosures from every article.

**External linking:**
- Tier-1 sources should open in new tab with `rel="noopener"`.
- Do not nofollow legitimate authoritative outbound links — outbound linking to good sources is a positive helpful-content signal.

**Core Web Vitals targets (April 2026):**
- LCP: < 2.5s
- INP: < 200ms (replaced FID March 2024)
- CLS: < 0.1

INP is the metric most sites currently fail; it requires JavaScript discipline. Lazy-load third-party scripts; defer non-critical work.

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
- [ ] Image guidance: WebP/AVIF, width/height set, descriptive alt text, lazy-load.
- [ ] Internal links: 3–6 contextual, descriptive anchors.
- [ ] External links: open in new tab, `rel="noopener"`.
- [ ] No HowTo schema. FAQ schema only if real on-page FAQs exist.
- [ ] "Last updated" / "Last reviewed" dates set.
