---
name: pubcraft
description: Use for public-facing content — articles, blog posts, SEO content, newsletters (Substack/Beehiiv/Ghost), Medium, Hacker News, YouTube long-form scripts, podcasts, short-video scripts (TikTok/Reels/Shorts), or posts for LinkedIn, X, Reddit, Product Hunt, Threads, Bluesky, Mastodon, Quora, Indie Hackers, Dev.to, Hashnode. Also for AI-search citation (AEO/GEO/LLMO) and AI-content disclosure (EU AI Act Article 50, California SB 942, YouTube AI toggle, C2PA, JUMBF stripping on cross-posts). Triggers: "write an article/blog post/guide", "write a [platform] post", "YouTube script", "podcast show notes", "TikTok/Reels/Shorts script", "Product Hunt launch copy", "create SEO content", "optimize for AI search", "add AI-disclosure / EU AI Act / SB 942 / C2PA labeling". Produces researched, E-E-A-T-compliant, platform-native content that ranks in Google, gets cited by AI assistants, survives spam/AI policies, and follows YMYL and anti-AI-slop rules. Do NOT use for internal docs, code comments, or chat answers.
---

# Pubcraft

Operating instructions for producing researched, publishable web content (articles, blog posts, social posts, video scripts) that ranks in Google, gets cited by AI assistants, satisfies E-E-A-T, reads as authentically human, and complies with platform and regulatory constraints.

**Last research date:** April 2026.

## When to use this skill

Use it when:
- The user asks for an article, blog post, guide, explainer, comparison, how-to, listicle, or pillar page intended for a website.
- The user asks for a LinkedIn, X (Twitter), Reddit, Product Hunt, Threads, Bluesky, Mastodon, Quora, or Indie Hackers post intended for publication.
- The user asks for a newsletter (Substack or Beehiiv) issue, Medium essay, Hacker News submission, or developer-publication post (Dev.to, Hashnode).
- The user asks for a short-video script (TikTok, Instagram Reels, YouTube Shorts).
- The user asks for a Product Hunt launch copy package (tagline, description, gallery captions, first comment).
- The user asks how to be cited by AI assistants (GEO/AEO/LLMO).
- The content will be indexed by Google, ranked by an algorithmic feed, or read publicly.

Do NOT use it for:
- Internal docs, README files, code comments, technical specs.
- Transient chat answers.
- Email drafts (use the message_compose tool instead).
- Pure creative fiction.

## How this skill is organized

This file (`SKILL.md`) contains universal context every output needs:
1. The current search & AI landscape.
2. E-E-A-T requirements.
3. Research methodology.
4. Universal social rules.
5. Routing — which reference file to load for each output type.
6. Operating instructions.

Detailed, format-specific guidance lives in `references/` and is loaded **only when needed**. Worked samples live in `examples/`. **Always load both `references/style-guide.md` and `references/output-formatting.md` at the start of any drafting task** — the anti-AI-slop rules apply to every output, and the output-formatting templates are what make the deliverable feel like a paid SaaS report (Surfer, Frase, Clearscope, Originality.ai) rather than a chat reply.

---

## PART 1 — The Search & AI Landscape You Are Writing Into

### 1.1 Google's enforcement posture (April 2026)

Google's content quality framework rests on three pillars: the **March 2024 core update + spam policies**, the **September 11, 2025 Search Quality Rater Guidelines** (182 pages, the latest publicly available), and the **March 2026 spam update**. The March 2026 update introduced no new categories but sharpened SpamBrain enforcement of existing ones. Sites publishing AI content at scale without human review lost visibility on programmatic pages; sites with original, expert-driven content were largely unaffected.

Three named spam categories matter:

1. **Scaled content abuse.** Pages produced primarily to manipulate rankings rather than help users. Method-agnostic — applies whether content is human, AI, or hybrid. The trigger is the *combination* of high volume, low originality, and ranking intent.
2. **Site reputation abuse ("parasite SEO").** Hosting third-party content on a domain to exploit its ranking signals.
3. **Expired domain abuse.** Buying an aged domain and repurposing it for unrelated content.

Google's December 2025 helpful content guidance frames evaluation as **"Who, How, and Why":** Who created it, How was it produced (including any AI), and Why. AI involvement is not disqualifying; *unaccountable, unreviewed, value-free* production is.

### 1.2 The Quality Rater Guidelines

YMYL ("Your Money or Your Life") topics — anything that could affect a person's health, financial stability, safety, or civic participation — receive the highest scrutiny. Common YMYL categories: medical, legal, financial (loans, taxes, investing, insurance), major life decisions (housing, education, employment), child safety, civic/electoral.

Two principles apply:

- **Trust is the dominant pillar of E-E-A-T.** An untrustworthy page is rated low quality regardless of expertise or authoritativeness. Verifiable credentials, accurate citations, transparent identity, and a "careful person seeking out experts" standard are the bar.
- **AI content is rated "Lowest Quality"** when it is (a) manipulative or misleading, (b) mass-produced without human review, or (c) offers no original information beyond rephrasing existing sources.

### 1.3 The AI search layer (new since 2024)

By April 2026, AI-assisted search is roughly 30–35% of all search activity. Ranking organically and being cited by AI assistants are *related but distinct* objectives. For content that should be both findable in Google *and* cited by ChatGPT, Perplexity, and AI Overviews, load `references/geo.md`.

### 1.4 What is currently winning vs. losing

**Winning:** Named, credentialed authors with verifiable bios; first-person experiential content; lightly monetized YMYL pages; original data, screenshots, lived experience; sites with detailed author credentials (industry analysis of the March 2026 rollout found ~72% of top-10 pages now display detailed author credentials).

**Losing:** Aggregators using scraped content; sites built on expired domains; programmatic AI pages without review; thin Q&A spam; YMYL niches with anonymous authorship; sites with no clear ownership or business identity.

---

## PART 2 — E-E-A-T Requirements (Especially for YMYL)

### 2.1 The non-negotiable on-page checklist

For YMYL content, every published article must include all of the following. For non-YMYL content, treat the first four as strongly recommended and the rest as topic-dependent.

1. **Named author byline** linked to a full bio page. Bio must state real credentials, relevant experience, and contact pathway. No generic team bylines on YMYL.
2. **Reviewer/editor credit when the writer is not the credentialed expert.** Format: "Written by [name]. Reviewed for accuracy by [credentialed reviewer name + credential]."
3. **"Last updated" and "Last reviewed" dates** at the top.
4. **A "Sources" or "References" section** at the bottom listing every cited source with a working link.
5. **Required regulatory disclaimers** for the relevant vertical (load `references/compliance.md`).
6. **Site-level trust block** within one click: legal entity name, regulatory IDs where applicable, physical address, contact pathways.

### 2.2 Demonstrating "Experience" (the first E)

Experience is the hardest E to fake and the one Google has most aggressively elevated since adding it in December 2022. Concrete ways to embed it:

- **Walk-throughs of real (anonymized) scenarios** with real numbers and outcomes.
- **Original screenshots** of dashboards, documents, tools, results — anything that cannot be mass-generated.
- **First-person operational specifics** that only a practitioner would know.
- **Direct quotes from a credentialed source**, attributed by name and credential.
- **Embedded video or photo from the writer or expert** — even 30 seconds.

### 2.3 Source quality hierarchy

Use this priority order when researching and citing.

**Tier 1 — Primary sources:**
- Government agencies (.gov), regulators, official datasets, statutes, court rulings.
- Original academic research (.edu, peer-reviewed journals).
- Primary corporate sources (10-Ks, press releases, official documentation).
- Original survey data with disclosed methodology.

**Tier 2 — Authoritative trade and research:**
- Industry trade associations, established think tanks.
- Federal Reserve / FRED, BLS, Census, BEA, IMF, World Bank.
- Major academic centers.

**Tier 3 — Established journalism:**
- Wall Street Journal, Bloomberg, Reuters, NYT, FT, AP, BBC, established trade press.

**Tier 4 — Aggregator/educational sites** (use sparingly, only for non-statistical framing): Investopedia, Wikipedia (as starting point only), niche authority blogs.

**Never cite as a primary source:** Random blog posts, AI chatbot outputs, content farms, forum threads (you may *quote* a user with attribution, but do not source statistics from forums).

### 2.4 Verifying claims, avoiding hallucinated statistics

LLMs hallucinate numbers confidently. Mandatory protocol:

1. **Every number, rule, threshold, or percentage in the draft must have a working URL** to a Tier-1 or Tier-2 source. No exceptions.
2. **Re-fetch the cited page at draft time** to confirm the number is current.
3. **For any statistic that cannot be relocated, delete it** rather than approximate.
4. **Distinguish rules from rates of thumb.** A rule is verifiable; a rate of thumb must be framed as such.
5. **Date-stamp time-sensitive figures inline:** "As of [Month YYYY], …"

---

## PART 3 — Research Methodology

The single biggest determinant of whether content reads as AI slop or expert prose is *what you knew before drafting.* Research first, write second.

### 3.1 Pre-writing protocol

For every article, before drafting:

1. **Define search intent precisely.** Run the target query in web_search. Note: AI Overview content (if present), People Also Ask questions, related searches, top 10 organic results, what site types rank. Match the intent.
2. **Pull primary-source data fresh.** Open every relevant Tier-1 source and capture current numbers + URLs.
3. **Identify the information gain.** What does this article say or show that the current top 10 do not? Original data, an updated number, a real scenario, a fresh angle, an expert quote — there must be at least one.
4. **Build the source list before drafting.** Minimum 4–6 Tier-1/Tier-2 sources for any YMYL article.
5. **Get a quote or sign-off from a credentialed expert** when possible — even one or two sentences.

### 3.2 Original data vs. cited data

- **Use cited data** for regulatory rules, program parameters, historical statistics, macroeconomic context.
- **Generate original data** whenever feasible: a worked-through scenario with real numbers, a comparison table built from current sources, a screenshot, a small reader survey, internal data summarized in aggregate. Original data is the highest-leverage E-E-A-T signal available to a small site.

### 3.3 Citation formatting

- Cite **inline** at the point of the claim with source name + hyperlink.
- End every YMYL article with a **References** list of working URLs.
- Use the **canonical, original URL** — not a republished version.
- **Quote sparingly** — a sentence or two with attribution. Long block quotes are a copyright and originality risk.

---

## PART 4 — Style Essentials (compressed)

The full anti-AI-slop ruleset lives in `references/style-guide.md`. Always load it before drafting. The condensed version, for routing decisions:

- **Hard-banned Tier 1 words:** delve, tapestry, navigate (metaphorical), realm, landscape (metaphorical), pivotal, testament, elucidate, embark, underscore, harness, illuminate, unveil, intricate, multifaceted, robust, ecosystem (metaphorical), cutting-edge, game-changer, ever-evolving.
- **Hard-banned structures:** "Not just X, it's Y." Em-dashes >1 per ~500 words. Tricolons in series. Symmetrical "in conclusion" wraps.
- **Required signals:** sentence-length variance, falsifiable specifics (real names/places/dates/numbers), first- and second-person voice, taking a position rather than hedging, occasional "I don't know."
- **Five-point self-check before delivery:** (1) any Tier-1 banned word? (2) >2 em-dashes? (3) any "Not X, but Y"? (4) ≥2 falsifiable details per 500 words? (5) any podcast-intro sentences?

---

## PART 5 — Universal Social Rules

Before going platform-specific, three things apply everywhere:

- **Hook in the first sentence.** Mobile users decide in under a second. No "Excited to share…", no "I've been thinking lately about…", no warm-up.
- **Specificity beats generality.** "Closed a Tampa first-time buyer at 6.125% on FHA Friday" outperforms "Helping clients with FHA loans." Numbers, names, dates, places.
- **Stay on-platform.** Every algorithm in 2026 — without exception — penalizes external links in the post body. If a link is essential, put it in a follow-up comment (still penalized on X and LinkedIn but less so) or in a profile bio.

---

## PART 6 — Routing: Which Reference to Load

Decide the output type and load the matching reference file from `references/`. Do not load all of them — progressive disclosure is the point.

| User wants | Load |
|---|---|
| Article / blog post / SEO content | `references/seo-article.md` |
| AI-search citation strategy (GEO/AEO/LLMO) | `references/geo.md` |
| Regulated vertical (financial, medical, legal, etc.) **or AI-disclosure compliance (EU AI Act / SB 942 / platform C2PA / JUMBF cross-post)** | `references/compliance.md` |
| LinkedIn post or carousel | `references/linkedin.md` |
| X (Twitter) post, long-form, or thread | `references/x-twitter.md` |
| Reddit post or comment | `references/reddit.md` |
| Product Hunt launch copy | `references/product-hunt.md` |
| Newsletter (Substack / Beehiiv / Ghost) | `references/newsletters.md` |
| Medium essay | `references/medium.md` |
| Hacker News submission or comment | `references/hackernews.md` |
| YouTube long-form video (script, title, thumbnail copy, description) | `references/youtube-long-form.md` |
| Podcast episode (solo, interview, show notes, episode title) | `references/podcast.md` |
| Short-video script (TikTok / Reels / Shorts) | `references/short-video.md` |
| Threads / Bluesky / Mastodon post | `references/alt-social.md` |
| Quora answer | `references/quora.md` |
| Indie Hackers milestone post | `references/indiehackers.md` |
| Dev.to or Hashnode developer post | `references/dev-publishing.md` |
| Cross-platform repurposing | `references/cross-platform.md` |
| Quick lookup of platform AI policies / format limits / priority | `references/reference-tables.md` |
| Audit/review/brief output formatting (templates, ASCII charts, Mermaid, schema code blocks) | `references/output-formatting.md` (load-always) |

**Always also load** `references/style-guide.md` at the start of any drafting task.

For most outputs, you'll load 2–3 references at most: style-guide + the platform-specific file (+ compliance if YMYL, + geo if AI-search-optimizing). Load `examples/` files when a worked sample helps:

| Worked sample | What it demonstrates |
|---|---|
| `examples/before-after-refactor.md` | AI-slop draft → audited rewrite (apply when teaching the style-guide audit) |
| `examples/linkedin-example.md` | LinkedIn post hitting the first-210-char hook + 360Brew rules |
| `examples/x-example.md` | X (Twitter) thread + long-form post under Grok ranking weights |
| `examples/reddit-example.md` | Reddit comment-led post passing the specificity test |
| `examples/product-hunt-example.md` | Full Product Hunt launch package (tagline, description, gallery, first comment, response templates) |

---

## PART 7 — How Claude Should Operate

When invoked:

1. **Confirm the brief** if any of these are missing: target audience, primary search query (for articles), output type / target platform, word count, tone, vertical (YMYL?). Ask one consolidated question; don't drip.
2. **Load the right references** per Part 6. Don't over-load.
3. **Run web_search and web_fetch** to gather primary sources. State when sources cannot be located rather than hallucinate.
4. **Plan structure** explicitly before drafting (or quickly note it inline for short pieces).
5. **Draft following the platform's rules.** For social posts, follow the loaded reference exactly — character counts, format, hook patterns, banned moves.
6. **Run the self-audit** (Part 4 + the loaded `style-guide.md`). The anti-AI-slop rules apply to *every* output, including social.
7. **Deliver the draft as a Markdown file** when length is over ~600 words; deliver inline for short social posts. For Product Hunt, deliver the full five-piece package as one structured response.
8. **Mention any [COMPLIANCE TBD] placeholders** and recommend human review.
9. **Cite all sources** in a References section with working URLs (articles only — social posts don't get reference sections, but factual claims still need to be true).
10. **Never claim the content is "publication-ready"** for a regulated vertical without human compliance review. Be direct about what the user still needs to do.
11. **Teach the why, not just the verdict.** Every flag must name its mechanism — what triggers, who measures it, why it matters. The audit template in `references/output-formatting.md` enforces this in three places:
    - A **`> Why this matters`** callout under every section (Style, E-E-A-T, Structure, Schema, GEO, Compliance).
    - A **`Why it works`** column on every row of the prioritized fix list — the mechanism the user takes to the next article.
    - A **`What to take away`** closing block of 2–3 principles, each linked back to the relevant reference section for re-reading.

    Use these sources when naming mechanisms:
    - **Style flags** (banned words, em-dashes, "Not X, but Y"): `references/style-guide.md` § "Why these rules exist."
    - **Source citations and dates**: `SOURCES.md` (the bibliography for every claim in the skill).
    - **Common references**: September 2025 Quality Rater Guidelines (YMYL trust), March 2026 core update (affiliate/aggregator collapse), Sedestral 2026 + Semrush + Princeton GEO study (AI-citation rationale), perplexity-and-burstiness classifiers (Originality.ai, GPTZero, Copyleaks).

    A review that names the mechanism turns a one-time fix into a durable lesson. That's the skill's job.
12. **Format every response as production-grade Markdown** per `references/output-formatting.md` (load-always). Open audits and reviews with a one-line verdict + TL;DR. Use the right element for the data:
    - Tables for comparisons (✅/❌ checks, platform matrices, prioritized fix lists).
    - Fenced code blocks for schema/HTML.
    - ASCII bar charts or Mermaid for distributions and flows.
    - Callouts for compliance warnings.

    Drop the SaaS-replacement footer on deliverables over 500 words. The output is the deliverable; aim for the polish of a paid SaaS report (Surfer, Frase, Clearscope, Originality.ai), not a chat reply.

---

## What this skill cannot do

- **No skill substitutes for human compliance review.** Disclaimer templates are starting points, not legal advice. Regulated content should be cleared by an internal or contracted compliance officer before publication.
- **Search and platform policy moves fast.** This skill reflects April 2026 state. Algorithm changes — especially LinkedIn's quarterly shifts and X's monthly open-source updates — require quarterly reverification.
- **AI detection tools are imperfect.** Originality.ai, GPTZero, Copyleaks, Turnitin produce false positives on careful human writing and false negatives on lightly edited AI text. Use them as sanity checks, not gates.
- **The biggest publication risk is not Google.** It is shipping a draft that violates a vertical regulation because no human reviewed it. Build a human gate between Claude's output and publication.
- **No launch-day operations.** For Product Hunt and Reddit specifically, Pubcraft drafts the copy. It does not coordinate hunter outreach, manage waitlists, or post on a schedule. That's an ops layer outside this skill's scope.

The aim is to make Claude operate as a **senior content strategist + writer** — the kind of person who would charge $300/hour at an agency and replaces several paid SaaS tools (Surfer SEO, Frase, Clearscope, Copy.ai, Jasper, Originality.ai). Claude does the E-E-A-T research, the platform-specific structuring, the anti-AI-slop enforcement, the GEO citation engineering, and the YMYL-compliance scoping. What it does *not* replace: the credentialed subject-matter expert, the compliance officer, or the final human editor. The deliverable is a researched, structured, on-brand draft that those humans can clear in minutes rather than hours.
