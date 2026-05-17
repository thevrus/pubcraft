# GEO — Generative Engine Optimization

Load this reference when the user wants content cited by AI search engines and assistants (ChatGPT Search, Perplexity, Google AI Overviews, Claude, Copilot, Gemini), or asks about "AI SEO," "AEO," "GEO," "LLMO," or being surfaced in AI answers.

## What GEO is — and isn't

GEO (also called AEO — Answer Engine Optimization, or LLMO) is optimizing content so AI systems **cite and surface it** when generating answers. It overlaps with traditional SEO but the success metric is different:

- **Traditional SEO** = win the click. Ten blue links, user picks yours.
- **GEO** = win the citation. AI summarizes the answer; your URL appears in the citation list (or, increasingly, your *brand name* appears in the prose without a link).

By May 2026, AI-assisted search is roughly 30–35% of all search activity. Sites that rank well organically are *not* automatically cited by LLMs; the retrieval and ranking layers are different.

Google's official **AI Features and Your Website** guide (Search Central, refreshed May 2026) confirms the underlying mechanism: AI Overviews and AI Mode use **retrieval-augmented generation (RAG)**, which Google calls "grounding," to pull from "core Search ranking systems" before composing the answer. AI Overview eligibility is gated on organic rank in the top 10, plus a re-ranking pass for direct-answer extractability. Pages that are uncrawlable, JavaScript-walled, or blocked in `robots.txt` are categorically excluded.

**Why GEO matters in dollars, not just visibility:** ChatGPT referrals convert at ~14.2% versus ~2.8% for traditional organic search (Sedestral, 2026) — roughly 5× the per-visit conversion rate. AI Overviews now appear in 200+ countries across 40 languages, consume 42–48% of above-the-fold real estate, and trigger on 88% of informational queries. Pages ranking #1 organically saw a **34.5% CTR decline** when an AI Overview appeared (Semrush 10M-keyword study). Citations are becoming more valuable per-visit than rank.

## AI search market share (early 2026)

| Engine | Share of AI search |
|---|---|
| ChatGPT (incl. Search) | ~64.5% |
| Gemini | ~21.5% |
| DeepSeek | ~3.7% |
| Grok | ~3.4% |
| Perplexity | ~2.0% |
| Claude | ~2.0% |

ChatGPT processes 250–500M weekly queries; Perplexity ~50M but disproportionately influential among researchers, analysts, and developers. Optimize first for ChatGPT and Gemini; treat Perplexity as a high-leverage citation surface for B2B/research-led content.

## Query fan-out — the mechanism that changes how to structure an article

**Query fan-out** (Google's May 2026 guide): when a user submits an AI Overview or AI Mode query, the system generates **multiple concurrent related sub-queries** and retrieves results for each before composing the answer. Google's own example: "how to fix a lawn" triggers parallel retrieval for "best herbicides," "remove weeds," and similar.

The practical consequences:

- **Your article only needs to cite-magnet on *one* of the fanned sub-queries to appear in the final answer.** A page targeting "how to fix a lawn" can earn the citation by being the best page on "remove crabgrass" even if it doesn't rank for the head term.
- **Structure for sub-query coverage, not single-keyword density.** Each H2 should answer a distinct sub-question that a fan-out might emit. Use People Also Ask, "related searches," and your own AI Overview prompt-audits to identify them.
- **Do *not* spin off separate thin pages for each sub-query.** Google explicitly calls this "scaled content abuse" in the same guide: "Don't create separate content for every possible variation [of queries]. High quantity of pages doesn't make a website higher quality." Consolidate sub-query coverage into one substantive page.
- **The fan-out is why TL;DR-as-definition + 40–60 word answers under each H2 outperform monolithic prose.** Each sub-answer is an independent extraction candidate.

## What Google explicitly says you DO NOT need (May 2026 official guidance)

Pubcraft has been advising this for a year on empirical grounds; Google's May 2026 guide now confirms it on the record. Quote Google's framing when a user pushes for any of these:

- **No `llms.txt` file.** Google: "You don't need to create new machine readable files, AI text files, markup, or Markdown." See § "llms.txt" below for the empirical study and the hygiene case.
- **No AI-specific schema or markup.** Google: "Structured data isn't required for generative AI search." Continue to use `Article` / `Dataset` / `Organization` / `Person` schema for rich-result eligibility and traditional SEO; they remain high-leverage. Stop hunting for an "AI Overview schema type": none exists.
- **No content chunking for AI.** "There's no requirement to break your content into tiny pieces for AI. No ideal page length exists." Length should match intent, not LLM context windows.
- **No keyword-stuffed long-tail prose.** "AI systems understand synonyms and general meanings. Don't worry about long-tail keywords or capturing every variation." Write naturally; rely on query fan-out to handle the surface variations.
- **No inauthentic "mentions."** Google: "Seeking inauthentic 'mentions' across the web isn't as helpful." See § "Brand-mention optimization" below for the earned-vs-placed pattern and the FTC-liability angle.

## The four AI search surfaces (and how each picks citations)

1. **Google AI Overviews** — top-of-SERP generative answers. Heavily favors pages that already rank in the top 10 organic results, but adds its own re-ranking based on direct-answer extractability. **Practical implication:** rank organically *and* structure for snippet extraction (40–60 word direct answers under H2 questions).

2. **ChatGPT Search / SearchGPT** — uses a Bing-backed retrieval layer with custom re-ranking. Citation patterns favor: clear authorship, recent dateModified timestamps, structured data, and content that directly answers the verbatim user query. Reddit, Wikipedia, and Stack Overflow are massively over-represented.

3. **Perplexity** — most aggressive about citation transparency (4–6 numbered sources per answer on average). Favors fresh, statistics-dense, well-cited content. Indexes near-daily; freshness is weighted heavily. Clear patterns: pages with numbers, named experts, and explicit "as of [date]" framing get cited far more than evergreen prose. **93% zero-click rate** — being cited is brand exposure, not traffic; budget accordingly.

4. **Claude / Gemini / Copilot** — each has its own retrieval. Claude's web search (when enabled) prefers recent, well-structured pages with primary-source links. Gemini integrates Google's retrieval. Copilot uses Bing.

## What gets cited (the empirical patterns)

Google's May 2026 guide names the meta-pattern bluntly: **"non-commodity content that's helpful, reliable, and people-first."** The contrast Google uses matches what LLMs cite:

| Commodity (rarely cited) | First-hand (cite magnet) |
|---|---|
| "7 Tips for First-Time Homebuyers" | "Why We Waived the Inspection & Saved Money" |
| "Best Productivity Apps in 2026" | "I Tracked 6 Weeks on Linear, Notion, and Slate" |
| "How to Improve SEO" | "The 3 Audit Findings That Recovered 41% of Our Traffic" |

The left column is what every SEO-driven site already publishes. The right column is what Google now rewards and what every major LLM disproportionately cites.

Multiple studies through 2025–2026 (Princeton GEO study, BrightEdge GEO benchmark, Ahrefs LLM-citation analysis) converge on:

- **Quotation magnets.** Direct quotes from named sources get extracted and cited disproportionately. "According to [Name], [credential], 'specific quoted claim.'" — this exact structure is what LLMs grab.
- **Statistics with context.** A statistic with the source name, date, and a one-sentence explanation gets cited 3–4× more often than the same statistic naked. "**38% of B2B buyers** now use AI search before talking to sales (Forrester, Q4 2025) — up from 12% in 2024."
- **Definitions and explanations.** A clean 1–2 sentence definition placed near the top, before the H2 expansion, gets pulled into AI answers verbatim.
- **Comparison tables.** Side-by-side comparisons get reformatted and cited as authoritative summaries. The *table format itself* is a citation-magnet.
- **Step-by-step processes** with numbered ordered lists.
- **First-person authority signals.** "I tested 12 X tools over 6 weeks" beats "Many people compare X tools." LLMs increasingly prefer sources that signal lived experience.

## What doesn't work

- **Pure rephrasing of consensus.** If your post says what every other post says, LLMs have no reason to cite *you* specifically — they'll cite Wikipedia or the highest-authority duplicate.
- **No primary sources.** LLMs trace claims; pages without citations get treated as unreliable secondary sources.
- **JavaScript-only rendering.** ChatGPT Search and Perplexity crawl rendered HTML, but Bing's cache (which ChatGPT relies on) still struggles with client-only content. Server-render or use SSG.
- **Anonymous bylines on YMYL.** Same E-E-A-T pressure as Google.
- **Outdated dateModified.** AI systems weight freshness aggressively for time-sensitive queries. Update + re-stamp annually at minimum.

## llms.txt — officially unnecessary, structurally fine

The proposed `llms.txt` standard (a structured markdown file at root, modeled on robots.txt, proposed by Jeremy Howard in Sept 2024) is adopted by ~2% of sites as of 2025–2026. **Empirical effect on citations: not statistically significant** (r/SEO_LLM ~10K-site study, March 2026: 6.8 vs. 6.7, p=0.85). Google's May 2026 official guidance ratifies this: "You don't need to create new machine readable files, AI text files, markup, or Markdown." Implement it as 30 minutes of structural hygiene if you want; do *not* treat it as GEO strategy. Focus instead on rendering, structured data, and citation-magnet content patterns covered above.

## Technical bare minimum for GEO eligibility

- **Server-rendered HTML** (or SSG) — content visible to crawlers without JS.
- **Article schema** with author (Person), datePublished, dateModified, publisher, image. (See `references/seo-article.md`.)
- **Person schema** on author pages with credentials, sameAs (LinkedIn, Twitter, etc.), jobTitle, knowsAbout.
- **Clean canonical URLs** — no session params, no fragmented duplicates.
- **`robots.txt`** that does *not* block GPTBot, ClaudeBot, PerplexityBot, Google-Extended unless you have a strategic reason. Blocking them removes you from training and (often) retrieval.
- **Sitemap.xml** with lastmod timestamps.

## Content patterns to deliberately add

When drafting an article that should attract citations:

1. **Open with a TL;DR-as-definition.** "X is [precise 1–2 sentence definition]. [One sentence on why it matters.]" Place above any H2.
2. **Include 2–4 named-expert quotes** with credentials. Real people, real titles, real quotes. Synthesize from interviews if you have them; otherwise cite published quotes.
3. **Embed at least one statistic per major section** with source name, date, and a sentence of context.
4. **Add a comparison table** when the topic admits one. Tables get reformatted by every major LLM.
5. **End each H2 section with a one-sentence summary** that could stand alone as a citation.
6. **Maintain a "Last updated" + "Last reviewed" stamp** at the top, updated honestly.

## Brand-mention optimization (the 2026 frontier)

LLMs increasingly cite *brand names in prose* without linking — "tools like Linear, Notion, and Slate handle this differently." A widely-cited 2026 finding: **brands are ~6.5× more likely to be cited via third-party mentions (Reddit, Hacker News, comparison reviews, trade press, Wikipedia) than via their own domain.** This reframes the brand-mention strategy: the highest-leverage GEO work is often *not* on your own site.

Getting mentioned this way requires:

- **Clear, specific positioning** (Slate = the meeting-decision capture tool, not "the AI productivity platform").
- **Earned mentions across high-authority third-party sources** — Reddit threads, Hacker News comments, comparison reviews, podcast appearances, Wikipedia where eligible.
- **PR and earned media** as a GEO channel, not just a brand channel — the citation graph LLMs build leans heavily on third-party signal.
- **A llms-friendly "About" page** with one-paragraph plain-language description of what the product is and isn't.

The word *earned* is load-bearing. Google's May 2026 guide explicitly warns: "Seeking inauthentic 'mentions' across the web isn't as helpful." Paid Reddit upvote rings, AI-generated comparison roundups built to seed your brand into the citation graph, purchased Wikipedia edits, and link-scheme cross-mentions are detected and don't compound. In regulated verticals they also expose the site to FTC endorsement-rule liability. The high-leverage pattern is genuine third-party signal, generated by being worth talking about, not staged.

This is reputation work, not on-page work. It compounds over 6–18 months.

## Agentic experiences — the 2027 surface

Google's May 2026 guide flags a forward-looking layer: **AI agents** performing autonomous tasks on behalf of users. Early agent traffic uses three primary entry points to a page:

- **Visual renderings** (screenshots of the page passed to a vision-language model).
- **DOM structure** (parsed HTML).
- **Accessibility tree** (the same tree screen readers use).

Google is investing in the **Universal Commerce Protocol (UCP)** for transactional flows; the AI Overviews / AI Mode retrieval layer will incrementally treat agent-friendly pages as a first-class surface. The practical guidance is mostly things that are already best practice:

- Server-render the meaningful content so the DOM and the visual rendering agree.
- Use **semantic HTML** (`<article>`, `<nav>`, `<main>`, `<button>` not `<div onclick>`). The accessibility tree is built from it.
- Keep **descriptive `alt` text, real `<label>` elements on form controls, and `aria-*` only where native semantics fall short**. Agents read the accessibility tree the way blind users do.
- Avoid layout that requires hover or animation to expose content.
- Verify the site in **Google Search Console**. Agent-quality signals will surface there before anywhere else.

Don't redesign for agents in 2026. Build so a 2027 retrofit is a config change, not an architecture change.

## Measurement

You can't directly query "did Perplexity cite me?" at scale, but proxies work:

- **Manual prompt audits.** Run 20–50 queries representative of your ICP through ChatGPT Search, Perplexity, AI Overviews. Track: are you cited, by what URL, in what position?
- **Referrer analytics.** ChatGPT, Perplexity, and Gemini referrers now show in Google Analytics 4 (`chatgpt.com`, `perplexity.ai`, `gemini.google.com`). Track sessions and conversions.
- **Brand-mention monitoring.** Tools like Profound, Otterly.ai, and AthenaHQ specifically monitor LLM citations of your brand. Worth subscribing if GEO is a strategic channel.

## Verdict

GEO is real, growing, and undermeasured. The good news: most of the work overlaps with strong traditional SEO and E-E-A-T (named authors, citations, structured answers, fresh content). The new work is **structuring for extractability** (clean definitions, named quotes, dated statistics, tables) and **monitoring brand mentions** in LLM outputs.

For 2026 content strategy: every article should be drafted with both "will this rank?" and "would a model cite this?" in mind.
