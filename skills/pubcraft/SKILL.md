---
name: pubcraft
description: Use this skill when the user asks for an article, blog post, long-form content, SEO content, newsletter (Substack/Beehiiv), Medium post, Hacker News submission, short-video script (TikTok / Instagram Reels / YouTube Shorts), or social posts for LinkedIn, X (Twitter), Reddit, Product Hunt, Threads, Bluesky, Mastodon, Quora, Indie Hackers, Dev.to, or Hashnode — any content intended for public publication. Trigger on requests like "write an article about X", "draft a blog post on Y", "write a LinkedIn / X / Reddit / Substack / Medium / Dev.to / Hashnode / Indie Hackers / Threads / Bluesky / Mastodon / Quora post", "draft a Hacker News submission", "write a TikTok / Reels / Shorts script", "create SEO content", "Product Hunt launch copy", "write a guide to Z", or when content will be published online. Produces researched, E-E-A-T-compliant, platform-native, human-reading content that ranks in Google and survives current spam/AI-content policies. Covers Google search articles, LinkedIn (360Brew algorithm), X (open-source Grok ranking), Reddit, Product Hunt, newsletters, Medium, Hacker News, short-video, alt-social (Threads/Bluesky/Mastodon), Quora, Indie Hackers, and developer publishing (Dev.to/Hashnode). Includes mandatory web research, source citation, anti-AI-slop style enforcement, YMYL/regulated-vertical compliance handling, and 2026-current AI-content disclosure rules (TikTok C2PA, EU AI Act). Do NOT use for internal docs, code comments, technical documentation, or transient chat answers.
---

# Pubcraft

Operating instructions for producing researched, publishable web content (articles, blog posts, LinkedIn posts) that ranks in Google, satisfies E-E-A-T, reads as authentically human, and complies with platform and regulatory constraints.

**Last research date:** April 2026.

---

## When to use this skill

Use it when:
- The user asks for an article, blog post, guide, explainer, comparison, how-to, listicle, or pillar page intended for a website.
- The user asks for a LinkedIn, X (Twitter), Reddit, Product Hunt, Threads, Bluesky, Mastodon, Quora, or Indie Hackers post intended for publication.
- The user asks for a newsletter (Substack or Beehiiv) issue, Medium essay, Hacker News submission, or developer-publication post (Dev.to, Hashnode).
- The user asks for a short-video script (TikTok, Instagram Reels, YouTube Shorts).
- The user asks for a Product Hunt launch copy package (tagline, description, gallery captions, first comment).
- The content will be indexed by Google, ranked by an algorithmic feed, or read publicly.

Do NOT use it for:
- Internal docs, README files, code comments, technical specs.
- Transient chat answers.
- Email drafts (use the message_compose tool instead).
- Pure creative fiction.

---

## How to use this skill

Follow this process in order. Do not skip steps.

1. **Clarify scope** if any of the following are missing: target audience, primary search query (for articles), content type (article vs. social), word count, tone, whether the topic is YMYL.
2. **Research the topic on the live web** using web_search and web_fetch. Build a source list before drafting.
3. **Plan structure** based on the actual SERP for the query (for articles) or the format conventions (for social).
4. **Draft** following the style and structural rules in Part 3.
5. **Self-audit** against the checklist in Part 7 before delivering.

---

## PART 1 — The Search & AI Landscape You Are Writing Into

### 1.1 Google's enforcement posture (as of April 2026)

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

### 1.3 What is currently winning vs. losing

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
5. **Required regulatory disclaimers** for the relevant vertical (see Part 6).
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

## PART 3 — Style: Producing Content That Doesn't Read as AI

### 3.1 Why this matters

Two distinct concerns are conflated and need separating:

1. **Algorithmic detection.** Google does not run a public binary "AI penalty." What it penalizes is *low-quality, unoriginal, ranking-motivated content* — which AI happens to produce by default. Generic AI prose loses because it lacks information gain and trust signals, not because a "delve" was detected.
2. **Reader perception.** Readers, journalists, and prospective clients *can* recognize AI slop. A YMYL brand reading as AI-generated is a trust catastrophe. Originality.ai, GPTZero, and Copyleaks use perplexity and burstiness as core signals. None are reliable enough for legal decisions, but a piece flagged by all three reads as AI to humans too.

Optimize for #2 and #1 takes care of itself.

### 3.2 Banned words

These words are statistical fingerprints of LLM output. Hard-avoid:

**Tier 1 (strongest tells):** delve, tapestry, navigate (as a metaphor — fine when literal), realm, landscape (as a metaphor — fine when literal), pivotal, testament, elucidate, embark, underscore, harness, illuminate, unveil, intricate, multifaceted, robust, ecosystem (as a metaphor), cutting-edge, game-changer, ever-evolving.

**Tier 2 (moderate tells):** leverage (as a verb), seamless, comprehensive, crucial, essential (as filler), key (as filler — "a key consideration"), indeed, furthermore, moreover, additionally (in clusters), in essence, in conclusion, ultimately (as a transition), it's important to note, it's worth noting, it goes without saying, when it comes to, in today's [X] world, in the world of, in the realm of.

**Tier 3 (transition spam — fine in isolation, AI-ish in clusters):** Furthermore + Moreover + Additionally appearing within 200 words of each other.

### 3.3 Banned structural patterns

**"Not just X, it's Y" construction.** "It's not just a tool — it's a movement." Hard ban. Strongest AI structural fingerprint in 2026.

**Tricolons (rule of three) in series.** "Fast, reliable, and affordable." Limit to one per article.

**Em-dash overuse.** AI loves em-dashes. **Hard limit: one em-dash per ~500 words.** Default to commas, periods, semicolons.

**Mirror Q+A rhetoric.** "But what does this mean? It means…" — sparingly, fine; as a recurring opener, a tell.

**Synonym cycling within close proximity.** AI varies word choice ("borrower… purchaser… aspiring owner…") more than humans do. If "X" is the right word, use "X" three times in a row.

**Comma-linked -ing modifiers.** "Rates rose, making affordability harder." Once or twice fine; as a tic, a fingerprint.

**Symmetrical conclusions** that summarize and end with a forward-looking platitude. Either say something new or stop.

**Bullet lists where every item is the same length and starts with the same part of speech.** Vary it or use prose.

### 3.4 Pro-human signals to deliberately include

- **Sentence-length variance.** Mix 4-word sentences with 30-word sentences. Burstiness is what humans have and AI doesn't by default.
- **Specific, falsifiable detail.** "Last Tuesday in Pinellas County" beats "recently in Florida." Real names, real places, real dates, real numbers.
- **Opinions and stance.** Take a position. AI hedges; humans commit.
- **First-person and second-person voice.** "I had a client last month who…"; "Your DTI is the deciding factor here."
- **Mild imperfection.** A trailing thought, a parenthetical aside, a "look —" or "honestly."
- **Pop-culture, regional, timely references.** AI cannot generate these convincingly without prompting.
- **Concrete examples over abstractions.** Always.
- **"I don't know"** when relevant. AI never says this; humans do.

### 3.5 Self-check before delivering

Run every draft through this five-point audit:

1. Did I use any Tier 1 banned word? (Find/replace.)
2. More than two em-dashes total? (Replace most.)
3. Any "Not X, but Y" structure? (Rewrite.)
4. At least two pieces of falsifiable detail per 500 words?
5. Any sentence sound like podcast intro voice? (Cut it.)

---

## PART 4 — Research Methodology

The single biggest determinant of whether content reads as AI slop or expert prose is *what you knew before drafting.* Research first, write second.

### 4.1 Pre-writing protocol

For every article, before drafting:

1. **Define search intent precisely.** Run the target query in web_search. Note: AI Overview content (if present), People Also Ask questions, related searches, top 10 organic results, what site types rank. Match the intent.
2. **Pull primary-source data fresh.** Open every relevant Tier-1 source and capture current numbers + URLs.
3. **Identify the information gain.** What does this article say or show that the current top 10 do not? Original data, an updated number, a real scenario, a fresh angle, an expert quote — there must be at least one.
4. **Build the source list before drafting.** Minimum 4–6 Tier-1/Tier-2 sources for any YMYL article.
5. **Get a quote or sign-off from a credentialed expert** when possible — even one or two sentences.

### 4.2 Original data vs. cited data

- **Use cited data** for regulatory rules, program parameters, historical statistics, macroeconomic context.
- **Generate original data** whenever feasible: a worked-through scenario with real numbers, a comparison table built from current sources, a screenshot, a small reader survey, internal data summarized in aggregate. Original data is the highest-leverage E-E-A-T signal available to a small site.

### 4.3 Citation formatting

- Cite **inline** at the point of the claim with source name + hyperlink.
- End every YMYL article with a **References** list of working URLs.
- Use the **canonical, original URL** — not a republished version.
- **Quote sparingly** — a sentence or two with attribution. Long block quotes are a copyright and originality risk.

---

## PART 5 — Article Structure That Ranks in 2026

### 5.1 Length by intent

These are working ranges, not minimums. Padding to length is itself a scaled-content-abuse signal.

- **Informational/definitional** ("What is X?"): 1,200–1,800 words. Direct answer in the first 60 words for AI Overview eligibility.
- **Comparison** ("X vs. Y"): 1,800–2,800 words with a real comparison table, scenario examples, decision framework.
- **How-to/process**: 1,500–2,500 words with numbered steps, screenshots, downloadable artifact.
- **Transactional/product page**: 800–1,400 words. Heavy on specific eligibility and tradeoffs, light on filler.
- **Pillar/hub guide**: 3,000–5,000 words, only when you have the depth.

### 5.2 Header structure

- **One H1 only**, containing the primary query phrase naturally.
- **H2s** correspond to subtopics that map to People-Also-Ask and "related searches." Use a real SERP scrape, not assumptions.
- **H3s** under H2s for sub-questions and stepwise breakdowns.
- Avoid H4+ unless genuinely needed; deep nesting is an SEO-template tell.

### 5.3 Featured snippet / AI Overview optimization

- Place a **40–60 word direct answer** immediately after the H1 (above any H2).
- Use a **40–60 word answer paragraph** under each H2 question, then expand.
- Include at least one **real comparison table** for comparison content.
- For lists, use 5–8 items, each a complete short sentence (snippet-friendly).

### 5.4 Schema markup (post-2025 reality)

- **Use Article (or NewsArticle for timely posts)** with author, datePublished, dateModified, publisher, image. Core to AI Overview eligibility.
- **Use BreadcrumbList.** Still supported.
- **Use Organization schema sitewide** with logo, sameAs, address, contactPoint.
- **Use Person schema on author bio pages** with credentials, sameAs, jobTitle, knowsAbout.
- **FAQPage schema:** Still valid but Google has restricted FAQ rich result *visibility* primarily to government and well-known health sites since August 2023. Add FAQ schema only if you have genuine on-page FAQs; do not invest heavily in it as a ranking play.
- **HowTo schema: effectively deprecated.** Google removed HowTo rich results September 13, 2023. Do not add HowTo JSON-LD. Use Article schema and ordered HTML lists instead.
- **Avoid:** Course Info, Estimated Salary, Claim Review, Vehicle Listings (deprecated through Google's June 12, 2025 simplification).

### 5.5 Images, links, performance

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

## PART 6 — Compliance Handling for Regulated Verticals

Some verticals require mandatory disclosures. The skill should recognize the vertical and apply the right framework.

### 6.1 Vertical detection

When the topic falls into any of these categories, treat as regulated and surface compliance requirements before delivering:

- **Financial / mortgage / lending:** TILA/Reg Z, RESPA, ECOA, Fair Housing Act, SAFE Act/NMLS, state mortgage statutes.
- **Investment advice:** SEC, FINRA, state securities boards.
- **Health / medical:** FDA labeling, FTC health-claim rules, HIPAA when applicable.
- **Legal:** State bar advertising rules, unauthorized practice of law.
- **Insurance:** State DOI rules.
- **Cannabis, gambling, alcohol:** State-by-state.
- **Children's products / education:** COPPA, FTC.

### 6.2 Universal regulated-content rules

For any regulated vertical:

- **No "guaranteed" or absolutist language.** "Guaranteed approval," "guaranteed returns," "best in [country]" — out. UDAAP / FTC deception risk.
- **No government-affiliation implications.** No language, seals, or design implying endorsement by an agency unless it's literally true.
- **No fiduciary implication** unless the writer/business genuinely is a fiduciary.
- **Professional advice outside license:** Do not provide tax, legal, medical, or investment advice in voice. Direct readers to consult their own qualified advisor.
- **Discriminatory language or imagery:** Imagery should be representative; targeting may not be based on protected classes (Fair Housing, ECOA, ADA, etc.).
- **Date-and-rate currency:** Any rate, price, or program parameter must be date-stamped and accompanied by a "subject to change" disclosure.

### 6.3 The disclaimer block (template — adapt to vertical and entity)

Drop into the footer of every regulated article and link from a `/disclosures` page:

> **[Vertical-specific seal — Equal Housing Lender / Investment Advisor / Member SIPC / etc.].** [Legal Entity Name], [License or Registration ID] #[XXXXXX]. Licensed by [regulator] under [statute]. Verify at [regulator's licensee lookup URL].
>
> **Not a commitment / not advice.** This article is for informational purposes only and does not constitute [an offer / professional advice / a commitment]. All [products/services] are subject to [eligibility/qualification/approval]. [Rates / prices / terms] are subject to change without notice.
>
> **No professional advice.** [Legal Entity Name] does not provide [tax / legal / medical / investment] advice. Consumers should consult their own qualified advisors regarding individual circumstances.
>
> **Jurisdictional scope.** [Legal Entity Name] is currently authorized to [operate / originate / advise] in [list of states/jurisdictions].

Append vertical-specific disclosures as needed (e.g., for mortgage: Reg Z rate-display block, refinance "total finance charges" disclosure, HMDA notice). The user should confirm exact language with their compliance officer.

### 6.4 What to do when the user is in a regulated vertical

1. **Tell them** which compliance frameworks apply.
2. **Insert a [COMPLIANCE TBD]** placeholder where vertical-specific disclaimers belong, and include template language.
3. **Recommend human compliance review** before publication. State this clearly. Do not pretend the draft is publication-ready.

---

## PART 7 — End-to-End Production Checklist

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

**Compliance phase (regulated verticals only)**
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

---

## PART 8 — Platform-Specific Social Content (April 2026)

Each platform has its own algorithm logic, format conventions, and reader expectations. Generic "social copy" gets buried on every one of them. Pick the right platform first, then write to *that* platform.

### 8.0 Universal social rules

Before going platform-specific, three things apply everywhere:

- **Hook in the first sentence.** Mobile users decide in under a second. No "Excited to share…", no "I've been thinking lately about…", no warm-up.
- **Specificity beats generality.** "Closed a Tampa first-time buyer at 6.125% on FHA Friday" outperforms "Helping clients with FHA loans." Numbers, names, dates, places.
- **Stay on-platform.** Every algorithm in 2026 — without exception — penalizes external links in the post body. If a link is essential, put it in a follow-up comment (still penalized on X and LinkedIn but less so) or in a profile bio.

---

### 8.1 LinkedIn

#### Algorithm reality (April 2026)

LinkedIn's algorithm shifted materially in late 2025 and again with the March 2026 "Authenticity Update." The platform now uses an LLM-embedding-based interest graph (the "360Brew" model) rather than a network-based feed, and ruthlessly deprioritizes engagement bait, automation patterns, and external links. Independent reporting indicates organic reach is down ~50–60% versus 2024 baselines, with engagement concentrated in formats the algorithm rewards.

**Rewarded:**
- **Dwell time** — the dominant quality signal.
- **Saves and sends** — LinkedIn explicitly added these to post analytics in late 2025.
- **Comment depth** — multi-sentence, substantive replies. Comments carry ~15x the weight of likes.
- **Topic-DNA match** — your profile and post content map to a specific professional cluster.
- **Native, zero-click content.**

**Penalized:**
- External links in the post body (~60% reach reduction).
- "Link in first comment" — now also penalized.
- Engagement bait ("Comment YES if you agree"; "Type 1 or 2"; vague "Thoughts?").
- Generic AI-generated text patterns (LinkedIn runs its own classifier).
- Wall-of-text with no white space on mobile.

#### Format and length

- **Optimal text post length:** 1,300–1,900 characters.
- **Hook (first 210–235 characters)** is everything — visible before "see more." Lead with a specific number, concrete claim, contrarian take, or named scenario.
- **Document carousels (PDF, 5–10 slides, 1080×1350 portrait):** highest-engagement format in 2026. Frameworks, checklists, side-by-sides perform best.
- **Native video, 30–90 seconds, with captions:** strong dwell-time generator. Show face/logo in first 4 seconds.
- **Single images:** underperforming text-only by ~30%.
- **Polls:** algorithmically deprioritized.

#### Post structures that work

- **The named-scenario teardown.** Specific case, real numbers, lesson at the end.
- **The myth-bust.** "Three things people in [field] still believe that aren't true in 2026."
- **The market-data take.** One chart from a Tier-1 source + one paragraph of interpretation.
- **The behind-the-scenes.** What the work actually looks like, not the marketing version.
- **The vertical-specific intel** — local, niche, or insider knowledge that no national brand can match.

#### Engagement and CTAs

- **Specific question** that requires informed thought, not "Thoughts?" or "Agree?"
- **Reply to every comment in the first 2 hours.** Posts where the creator replies see ~30% higher lifetime engagement.
- **Hashtags:** 3–5 max, at the end. Over-hashtagging (6+) reduces engagement.

---

### 8.2 X (Twitter)

#### Algorithm reality (April 2026)

X's algorithm is the only major social algorithm that is **open-source** (github.com/xai-org/x-algorithm, refreshed every ~4 weeks since the January 2026 Grok-powered rewrite). This means engagement weights are knowable, not guessed. The architecture: Home Mixer (orchestration) + Thunder (in-memory storage) + Phoenix (Grok ranking) + Candidate Pipeline. Grok now reads every post and watches every video, and applies sentiment analysis: combative or negative-toned posts get *reduced* distribution even when engagement is high.

**Engagement weights from the open source (treat as approximate):**
- **Like** = 1x baseline
- **Retweet** ≈ 20x like
- **Reply** ≈ 27x like
- **Conversation (reply + author reply)** ≈ 150x like
- **Bookmark** is now an explicit ranking signal (added 2024, weighted heavily in 2025–2026)
- **Dwell time** factored independently

The takeaway: optimize for replies and conversations. A post with 10 replies in the first 30 minutes will dramatically outperform one with 100 likes and zero replies.

**Premium subscription** is no longer optional for serious creators. Premium gets a documented **2x boost on out-of-network reach and 4x on in-network reach**, plus their replies are ranked higher in conversation threads. Without Premium in 2026, link posts get near-zero median engagement (since March 2026, free accounts posting external links are effectively invisible).

**Formats by performance (2026):**
- **Long-form posts (Premium, up to 25,000 chars)** are now favored over multi-tweet threads. The algorithm rewards dwell time.
- **Threads** still work but no longer outperform a tight long-form post. Use threads only when the structure genuinely needs steps.
- **Native video <60s** gets a distribution boost.
- **Original images** outperform stock; multi-image posts (2–4) outperform singles.
- **Pure text** is the baseline; competitive but no boost.
- **External links:** 50–90% reach reduction for Premium, near-zero engagement for non-Premium.

#### Format and length

- **Single tweet:** 240–270 characters is the sweet spot for engagement. The 280 char limit invites truncation in feed previews.
- **Long-form post (Premium):** 800–2,500 characters, structured with line breaks. Punchy lead. One idea per paragraph. Specific.
- **Thread:** 4–7 tweets. First tweet must work as a standalone. Number them ("1/" or "1." in the first line, optional). Last tweet should restate the value, not include a CTA to follow.

#### Hook patterns that work

- **Specific number lead:** "I closed 23 deals in Q1 using one rule: …"
- **Contrarian:** "Everyone says X. They're wrong, and here's the data."
- **Named scenario:** "A founder DM'd me Friday about [problem]. My answer:"
- **Question-as-thesis:** "Why is [counterintuitive thing] true? Three reasons:"

Avoid: "🧵 thread on…" (signals length without value), "I'll keep it short:" (don't announce structure), "Hot take:" (overused).

#### Sentiment notes

Grok's sentiment layer reduces reach for posts that are dunky, negative, or attack-oriented even when they get high engagement. Constructive disagreement is fine; calling people stupid is reach-suicide in 2026.

#### Engagement and timing

- **First 30–60 minutes determines distribution.** Post when your most engaged followers are online — for B2B, weekday 9–11 AM PT or 1–3 PM ET tends to work.
- **Reply to every reply** in the first 2 hours, including disagreement. Replies generate the conversation weight that's worth 150x a like.
- **Quote-tweets > retweets.** Add commentary when amplifying.

---

### 8.3 Reddit

#### Reality check (April 2026)

Reddit is the highest-leverage and highest-risk channel covered in this skill. Why high-leverage: post-2025-IPO, Reddit threads dominate AI-search citations (ChatGPT, Perplexity, Google AI Overviews pull heavily from Reddit), driving massive long-tail discovery. SimilarWeb's 2025 data showed Reddit referral traffic to SaaS sites doubled YoY. Why high-risk: spam filters and moderator enforcement tightened dramatically. One badly framed promotional post and your account gets shadowbanned across the platform.

The September 2025 algorithm update made the platform's incentives explicit: **engagement velocity in the first hour, dwell time, scroll depth, and comment quality** drive ranking. Promotional content without value gets buried by AutoMod or moderators within minutes.

#### The Reddit decision tree

Before writing a single Reddit post, answer these:

1. **Have I read the top 20 posts of all time in this subreddit?** Each subreddit has a culture. r/personalfinance demands data and citations. r/sysadmin tolerates zero sales pitches. r/Entrepreneur upvotes specific failures and downvotes generic listicles. Don't post until you know which.
2. **Does this subreddit's rules permit my content?** Read the sidebar. Many subs require a [Question], [Discussion], or [Case Study] tag. Many ban link posts entirely. A few require X karma/account age before posting.
3. **Am I posting from a real account with non-zero history?** New accounts with zero karma posting promotional content get auto-removed everywhere worth posting in. Aim for 100+ comment karma in the target sub before any post.

#### Title craft

The title is 80% of Reddit performance. Apply the **specificity test:**

- ❌ "How to do Reddit marketing." — generic, listicle voice.
- ✅ "We hit 50K subscribers on r/ourniche in 6 months. Here's what worked and what wasted time." — specific, signals lived experience, invites replies.

Patterns that consistently work:
- **The "I tried X" story:** "I tried [specific thing] for [specific time]. Here's what happened."
- **The contrarian-but-defensible:** "[Common belief] is wrong. Here's why."
- **The named-failure:** "We spent $40K on [thing] and got nothing. Lessons."
- **The genuine question:** "Why do [audience] still use [tool]? I'm missing something."

Avoid: clickbait numbers ("5 ways to…"), all-caps, emoji in titles, anything that feels like a marketing email subject line. Reddit's BS detector is the most calibrated of any platform.

#### Body craft

- **Lead with the specific scenario, not setup.** "Three weeks ago a customer cancelled because…" not "I want to talk about churn today."
- **First-person and lived-experience.** "I built/I tried/I spent/I learned." AI-voiced posts ("It's important to note that…") get downvoted reflexively.
- **Length:** 200–800 words for most subs. Some technical subs (r/ExperiencedDevs, r/sysadmin) reward 1,500+. Match the sub's average.
- **Format:** short paragraphs (2–4 sentences), occasional bold for scanning, sparing bullets. Reddit reads on mobile — wall of text dies.
- **No CTA at the end.** No "Hope this helps!" No "What do you think?" The post itself is the contribution. Add a question only if it's genuinely open-ended and you can't answer it yourself.
- **Disclose any commercial interest in the first paragraph.** "Disclosure: I work on [product]" or "I'm the founder of [X]." Concealed promotion is the fastest path to a permaban.

#### The first hour

Reddit's algorithm is even more first-hour-dependent than X. Stay online. Reply to every comment. Upvote good replies. Active OPs get algorithmic boost; passive ones don't.

#### The comment-driven strategy (often more valuable than posts)

Thoughtful comments on existing high-traffic threads frequently outperform original posts. They stay visible longer (until the thread dies), get cited in AI summaries, and bypass the title-craft challenge. For B2B and SaaS in 2026, comment-led marketing is often the highest-ROI Reddit play.

When to post vs. comment: post when you have an original story or unique data; comment when there's already a thread asking the question your expertise answers.

#### The branded subreddit play (for serious operators)

The Eric Eden / "Thinking Deeply AI" pattern: create your own subreddit (free, you set the rules, you moderate), post 20–30 high-quality pieces of content, let Reddit's search surface you. Subscribers grow not through sharing but through search. Eden grew to 25K subscribers and 21M reads in 11 months. The key: pick a subreddit name with the right keyword in it (treat it like a domain name).

This is a months-long play, not a quick win. Realistic timeline: 0–100 subscribers in weeks 1–4, 1K in months 2–4, 10K+ in months 6–12 if content is consistent and quality.

#### Banned moves

- Asking for upvotes anywhere (auto-removable).
- Cross-posting the same content to 5+ subs in one day (spam filter).
- Vote manipulation, reciprocal upvoting, upvote services. AutoMod and Reddit's spam team will catch this and the ban is account-wide.
- Posting from accounts under 30 days old to high-traffic subs.

---

### 8.4 Product Hunt

#### Reality check (April 2026)

Product Hunt is not a feed-based content platform. It's a **launch event**. Content for Product Hunt is the launch package itself: tagline, description, gallery captions, first comment, and the comment-thread responses you'll write on launch day. The skill's job here is to draft the *copy*, not run the launch.

Two big shifts that change how you write:

1. **January 2024: featuring rate dropped from 60–98% to ~10%.** Featuring is now curator-judged on four criteria: **usefulness, novelty, craft, creativity.** This isn't an algorithm to game; it's a human judgment call.
2. **2025–2026: ranking is points-based, not upvote-based.** Verified active users' votes carry more weight than fresh-account upvotes. Coordinated mass-voting is detectable and now actively penalized.

What this means for the copy: clarity and craft beat hype. A clear tagline that promises a specific outcome will out-feature a clever one that requires a click to decode.

#### The launch copy package

A complete Product Hunt launch package contains five pieces. Pubcraft drafts all five.

**1. Tagline (under 60 characters, single sentence)**

Answer the question "What is this?" in plain language. Benefit-driven. Not clever.

- ✅ "Schedule Slack messages in advance"
- ✅ "Secure everything you build, host, and run"
- ✅ "Turn meeting notes into action items in 2 minutes"
- ❌ "The future of work, reimagined"
- ❌ "Communication, simplified"
- ❌ Anything with "AI-powered," "next-generation," or "revolutionary"

**2. Description (under 260 characters)**

Lead with the *problem*, not the solution. 2–3 short sentences max.

> Your team spends 30 minutes daily re-explaining decisions in Slack. Slate captures those decisions automatically and surfaces them when someone asks. No more "wait, what did we decide?"

**3. Gallery captions (5–8 images / GIFs)**

Each caption is a short factual sentence describing what the image shows. No hype. Show the workflow. Before/after frames perform well. A 60–90 second demo video (no talking head, just product) is gold.

**4. First comment (the founder story)**

This is the second-most-important piece of copy after the tagline. It's a pinned comment from the maker. Keep it short (200–400 words), honest, useful.

Template:

> Hey Product Hunt 👋
>
> I'm [name] and I built [product] because [specific problem you personally hit].
>
> Today we're [what we're shipping]. Specifically, [one or two concrete things].
>
> What I'd genuinely value feedback on: [specific question — onboarding, pricing, a feature decision].
>
> If you try it and something feels confusing or broken, tell me here — I'll respond to every comment today. Thanks for checking it out.

What this is *not*: a press release, a fundraising-deck pitch, or a "we're so excited" announcement. It's a maker talking to other makers about a specific problem.

**5. Comment-response templates (for launch day)**

Pre-draft 6–8 response patterns to anticipated comments:
- "How is this different from [competitor]?" — direct, concrete, no trash-talking.
- "Is there a free tier?" — clear answer, link to pricing.
- "Feature request: X" — acknowledge, commit to specifics if you can.
- "I tried it and [bug]" — apologize, fix-or-ETA, follow up by DM.
- "This is just [reductive comparison]" — don't get defensive. Acknowledge the partial truth, explain the differentiator.

#### Tagging and category

Choose **3 categories**. Pick the most specific applicable ones, not the biggest. "AI Coding Assistants" beats "Productivity." Specific categories have less competition and reach an audience already filtering for your space.

#### Timing

- **Launch at 12:01 AM PT.** This gives you the full 24-hour window.
- **Tuesday or Wednesday** is standard. Thursday is acceptable. Avoid Monday (catch-up day) and Friday (low traffic).
- **Avoid major industry-event days** (WWDC, ProductCon, Y Combinator Demo Day) — you'll get buried.

#### What Pubcraft will not do

- Provide a launch coordination plan (timing, hunter outreach, waitlist mobilization). That's an ops problem, not a copy problem.
- Recommend specific hunters by name.
- Promise a featuring outcome. Featuring is curator judgment.

---

### 8.5 Substack / Beehiiv (newsletters)

#### Reality check (April 2026)

Newsletters are alive and growing. Beehiiv's State of Newsletters 2026 reports paid-subscription revenue across the platform jumped from ~$8M in 2024 to **$19M in 2025 (138% YoY)**, with median time-to-first-dollar for newsletters launched in 2025 down to **66 days**. Niche/specialist publications outperformed generalist ones. The two platforms are not interchangeable:

- **Substack** has shifted from email tool to recommendation network. Distribution comes from three surfaces: (1) **Notes** (algorithmic short-post feed inside the app, reply-weighted; functions like a Threads/X clone), (2) **writer recommendations** (a larger publication recommending you can deliver hundreds of subscribers in a day), and (3) the **app's Inbox/Discover** home (weighted by reading time, restacks, recommendations from followed writers). Substack still takes 10% of paid subs + ~3% Stripe. SEO-weak. Strong for *writers, essayists, journalists*.
- **Beehiiv** has effectively no internal social feed. Distribution comes from (1) **Boosts** — a paid CPA marketplace where other newsletters earn $1–$6+ per subscriber referred, (2) **Recommendations** (free reciprocal cross-promotion), (3) the **Beehiiv Ad Network** (monetization, not growth), (4) **SEO** of the public web archive (indexable structure, sitemaps, custom domains), and (5) referral programs you build yourself. Flat $34–$99/mo, 0% take-rate on subscriptions. Strong for *operators, B2B, ad/sponsorship-monetized newsletters, anyone who wants ownership and SEO*.

#### Open-rate norms (post-MPP, 2025–2026)

Apple Mail Privacy Protection has inflated reported opens; verified-open rates from Beehiiv's filtered analytics are the more honest number.

- **Healthy engaged niche:** 35–45% verified open rate.
- **Average:** 20–30%.
- **Below 20%:** deliverability red flag.
- **Click-through:** 6–14% for top performers; clicks > opens as the trust metric in 2026.

#### Format and length

- **Subject line:** 30–50 characters. Lower-case-ish. Curiosity or specific number. Plain-text, not headline-y.
- **Preview text** (~90 chars) is a *second subject line*. Never leave it auto-generated.
- **First line above the fold** must work as a third hook — many readers see only the inbox preview.
- **Body length:**
  - Substack paid post: 800–2,500 words.
  - Substack free post / Notes: 300–800 words / 280–500 chars respectively.
  - Beehiiv retention sweet spot: 600–1,500 words with one CTA.
- **Notes:** image attachments lift restacks substantially.
- **Pattern that works:** strong personal subject line → 1-line hook → bolded TL;DR → scannable subheads → one image or chart → single primary CTA. Avoid more than 2 links above the fold.

#### What works vs. fails

- **Working:** niche/specialist publications, weekly cadence, recommendations from 2–5 aligned writers, paid posts with a free preview ~30%, "build in public" revenue/learning posts, deeply personal essays, straight-news rewrites.
- **Failing:** generalist "thoughts on tech" newsletters, Substack growth without Notes participation, low-effort AI rewrites of other people's posts (deboosted on Notes), Beehiiv newsletters that buy too many Boost subscribers (engagement collapses, deliverability suffers).

#### Community norms / banned moves

- **Substack:** writer/reader culture is anti-spam, tolerant of self-promotion *if you give first*. Cross-posting hot takes from X is acceptable on Notes but seen as low-effort if it's your only output.
- **Beehiiv:** there is no "community" — readers are your list. The deliverability system enforces: don't deceive in subject lines, don't bait-and-switch links, don't import lists you didn't earn. Cold imports tank sender score.

#### AI content

- **Substack** does not ban AI but deboosts obviously templated AI prose on Notes; pure-AI publications get fewer recommendations. Reader culture is *strongly* anti-AI in literary, essay, and journalism niches; in technology and finance niches, "I used AI to research X" is fine.
- **Beehiiv** bundles an AI writer as a feature — explicitly pro-AI-assistance. No detection, no labeling.

#### Compliance

- **Financial newsletters:** SEC Investment Adviser rules can apply if you publish individualized advice. Standard disclosure: *"Not investment advice. For educational purposes only."* + FTC affiliate disclosure on any link.
- **Medical/supplements:** *"Not medical advice. Consult your physician."* + *"These statements have not been evaluated by the FDA"* on any structure-function claim.
- **Crypto:** FTC + state-level treatment of newsletter promos as endorsements. Disclose holdings, paid placements; *"This is not financial advice"* near-universal in the finance niche.
- **EU AI Act (effective Aug 2, 2026):** EU readers must see a disclosure if AI-generated text appears realistic-human-authored and was not editorially reviewed.

#### Hooks that work in 2026

- "I spent 90 days running both Beehiiv and Substack. Here's the math nobody shows you."
- "There's a reason your open rate dropped in March. It wasn't your subject lines."
- "Three weeks ago I almost shut this newsletter down. Here's what changed my mind."
- "The chart that broke my Q4 strategy" (image-led)
- "I lost 412 subscribers last month. Worth it. Here's why."

#### AI-tells / banned phrases on these platforms

Subscribers and Notes commenters call out: *"In today's fast-paced world,"* *"navigate the complexities,"* *"unleash/unlock the power of,"* *"delve into,"* *"it's important to note,"* *"in conclusion,"* *"Let's dive in!"*, em-dash-heavy three-clause sentences, and *"Have you ever wondered…?"*. The **"Picture this:"** opener and tri-colon list patterns ("It's not just X. It's Y. It's Z.") are mocked.

#### Verdict

Both platforms growing. Pick **Substack** for writers, essayists, journalists, anyone who wants instant network discovery. Pick **Beehiiv** for operators, B2B, anyone monetizing through ads/sponsorships, anyone who wants SEO and ownership.

---

### 8.6 Medium

#### Algorithm and distribution (2025–2026)

**Boost** is the only meaningful distribution lever. Human nominators (boost editors) flag stories; if accepted, the story gets a distribution multiplier *and* an earnings multiplier in the Partner Program. Earnings calculation (per Medium Help Center, 2025) combines: member read time + engagement (claps, highlights, replies, follows from the story) + Boost bonus + **+5% bonus for member reads from external sources (effective Oct 1, 2025)** + a member-read-ratio multiplier. Non-Boosted stories earn very little.

**"Friends of Medium"** gives select writers a higher base earning rate. Selection is opaque.

Medium's 2026 stance is explicitly anti-quantity. Their product team has said "tell your story rather than churn out content." Daily-publish strategies have collapsed in earnings.

**AI-only accounts are bannable.** Medium's TOS now reads: *"Exclusively using AI-generated content to earn money for stories and responses in the Partner Program"* is misuse and triggers suspension without appeal. January 2025 saw a mass-suspension wave.

#### Format and length

- **Optimal:** 1,200–2,000 words for general non-fiction; 1,500–3,000 for analytical/expert; 700–1,200 for personal essays.
- **Structure that gets boosted:** specific hook → personal stake → 3–5 H2 subheads with concrete claims → at least one image or pull quote → a non-clickbait conclusion that does not ask for claps.
- **Headlines:** specific number + time + outcome. ("How I Built a $2M SaaS in 18 Months" beats "My Startup Journey.") Test 5–10 variants.
- **Reading time on the page should match.** The algorithm rewards finished reads (member-read ratio).

#### What works vs. fails

- **Works:** deeply personal essays with a clear lesson; "I did X for N days" structured experiments; expert technical breakdowns by people with real credentials; well-edited essays with images and pull quotes.
- **Fails:** listicles ("10 ChatGPT prompts that will…"), AI-laundered Medium-on-Medium meta-posts, daily publishing, aggressive outbound linking (kills member-read time), pure SEO grind. Boost rate for "tools and prompts" content has cratered.

#### Community norms / banned moves

- **Engagement farming, follow-for-follow, mutual-clapping rings, comment-for-comment deals** are bannable.
- Self-promotion in-line (outside your bio link) is tolerated but boost-disqualifying.
- Reposting your own content from elsewhere without canonical noting.
- Asking readers to bypass the paywall.

#### AI content

Medium's policy is the **strongest of any major platform**: AI-only earning accounts get suspended without appeal. Mixed human+AI is allowed, but Boost editors visibly downrank obvious GPT prose. Commenters are unforgiving of AI-tells.

#### Compliance

- Financial: standard "not investment advice." Affiliate links use FTC disclosure. Medium's TOS bans payday-loan and crypto-promotion patterns; low-quality crypto airdrop posts get nuked.
- Medical: same FDA/FTC standards as newsletters.

#### Hooks that work

- "I made $25,000 on Medium in five years. Here's what nobody tells new writers."
- "My doctor told me I had six months. That was four years ago."
- "I spent three months trying to get boosted. Here's the pattern that finally worked."
- "Medium's algorithm changed in February. My earnings dropped 73%. Then I noticed this."

#### AI-tells / banned phrases

Medium readers are merciless on: *"In today's digital landscape,"* *"the world of [X],"* *"unlock,"* *"delve,"* *"crucial,"* *"navigate the intricacies,"* *"in this article, we'll explore,"* the GPT four-paragraph essay rhythm, and *"In conclusion, [topic] is more important than ever."* Headers labeled "Introduction" and "Conclusion" instead of substantive subheads are an instant tell. Avoid 🚀 and 💡 emoji bullets.

#### Verdict

Still viable for **personal essayists and credentialed experts** in 2026. Not viable as a content-mill side hustle — that game is over. Best as a *secondary* publishing surface paired with your own newsletter or blog.

---

### 8.7 Hacker News

#### Algorithm and ranking (2026)

Front-page score decays roughly as `(upvotes - 1)^0.8 / (hours_since + 2)^1.8`, plus moderator interventions: flamewar penalties, software-defined "controversy" penalties, off-topic penalties, and the **second-chance pool** (`/pool`) — a moderator-curated list where deserving-but-missed submissions get random front-page placement. You can email `hn@ycombinator.com` to nominate a story. The **/invited** list lets mods invite a writer to repost.

**Karma** unlocks features at thresholds (downvote ~500). Vote rings get nuked.

Editorialized titles are **rewritten by mods** automatically. HN's stance (per pg) is that titles are common property and the article's own title is the default. "[VIDEO]", "I made", or marketing language gets reverted.

**Show HN, Ask HN, Launch HN** are official categories. Launch HN is reserved for active YC startups (announced via YC partner). Show HN requires the project to be something users can *actually try*; the URL must lead to a working demo, repo, or downloadable artifact.

#### Format conventions

- **Title:** maximum 80 characters. No clickbait, no company-name brackets, no ALL CAPS, no "[2025]" unless it's in the original title.
- **Show HN body:** 2–6 short paragraphs. What it is, why you built it, what's interesting technically, what feedback you want. **Don't post a press release.**
- **Comments:** average upvoted comment is 2–6 sentences with a specific, often contrarian or experiential, claim. Long comments work *if* dense.

#### What works vs. fails

- **Front-page winners (recurring patterns from 2025–2026):** technical writeups (reverse engineering, deep dives, retro-computing), policy critiques on tech regulation, interesting failure modes, "I built this thing and learned X" pieces, original research, academic papers, deep open-source releases. AI critiques and AI tools both feature heavily.
- **Buried/flagged:** "We raised $XM" without substance, generic SaaS launch posts, listicles, AI-generated SEO blog spam, marketing-coded prose, Medium URLs (lower flag bar), reposts within ~6 months. **State of Show HN 2025** consensus: the bar has risen because of AI-coded launch volume; signal/noise of submissions has degraded.

#### Community norms / banned moves

- **Don't ask for upvotes** anywhere (post body, Twitter, Slack). Voting rings kill the post and flag the account.
- **Don't editorialize the title.** Use the article's own title; if no good title exists, factual descriptive only.
- **Don't reply combatively.** "Please don't be snarky" is in the official guidelines and is enforced.
- **Don't post the same URL twice within ~6 months.**
- **Show HN must be your own project.** Posting someone else's project as Show HN is a flag-out.
- **Don't downvote disagreement.** (You can; the culture polices it.)
- Tuesday–Thursday morning Pacific is the optimum window. Weekends underperform.

#### Comment craft (what gets upvoted vs. downvoted)

- **Upvoted:** specific lived experience ("I worked on this exact problem at $COMPANY in 2018, here's what we found"), correcting an error in the post with citation, technical clarification, counter-example with details, dry humor, niche expertise.
- **Downvoted/flagged:** "this," "+1," "OP is missing the point" without an argument, ad-hominem, political jabs, generic LLM-tone replies, *"Have you considered just using $LIBRARY?"* without context.

#### AI content

Heavily controversial through 2024–2026. Mods deboost obvious AI-generated articles. AI-generated *comments* are aggressively flagged. The community broadly tolerates AI-assisted code but is hostile to AI-written prose, especially AI-summary articles about HN itself.

#### Compliance

Pump-and-dump crypto submissions get flagged immediately. Affiliate links in submissions get flagged. Financial advice from anonymous accounts gets dismissed.

#### Hooks/titles that work in 2026

- "Show HN: I rewrote git in Rust to learn Rust. It's faster than I expected."
- "What fork() actually copies"
- "The 1.5M GitHub PRs that had ads injected by Copilot"
- "Closed-source AI is neofeudalism"
- "Ask HN: How do you stay productive when the model improves weekly?"

#### AI-tells / banned phrases

HN comments will brutally call out: *"Great question!"*, *"That's a fascinating point,"* *"In summary,"* *"It's worth noting that,"* the *"Certainly! Here are…"* opener, bullet-point-with-bold-keyword formatting, and any comment that pattern-matches GPT default voice. Em-dashes and triple-clause "It's not X — it's Y — it's Z" structure get sniffed instantly.

#### Verdict

Still the highest-quality tech audience on the internet. Viable in 2026, but the bar has risen. Treat HN as a place where you submit *one* deeply considered thing per quarter; don't farm it.

---

### 8.8 Short-video scripts (TikTok / Reels / Shorts)

#### Algorithm differences (2026)

- **TikTok:** interest-graph; first ~60 minutes is a stress test on a small initial sample; if retention >70% it scales globally. 2026 has **expanded taste for 1–3-min long-form storytelling**, predictive search via metadata/captions, and prioritization of videos using TikTok Shop. Originality score (late-2025/2026) penalizes reposts with watermarks.
- **Instagram Reels:** social-graph weighted *plus* a separate Reels AI ranker. 2026's biggest change: **DM shares are the #1 signal**, surpassing saves, comments, and likes. Saves and shares > likes. Watermarked TikTok reposts are explicitly deboosted. Originality Score flags duplicate audio+format combinations.
- **YouTube Shorts:** session-watch-time on YouTube as a whole; Shorts that drive viewers into long-form are favored. Searchable titles matter more than on TikTok or Reels (Shorts inherits YouTube search). Engagement rate is highest of the three (~5.9%); CPM/RPM via YPP is best.

#### Length sweet spots (verified for 2026)

- **TikTok:** 21–34 seconds achieves the highest completion rate (~62% avg in 2025–2026). Above 60 sec needs exceptional structure. Max is 10 minutes; completion drops sharply over 90 sec.
- **Instagram Reels:** **7–30 seconds for new-audience reach** (loop math: a 7-sec video looped 3× counts as 300% retention). 30–60 sec for educational/talking-head. Max 3 minutes.
- **YouTube Shorts:** **50–60 seconds** averages highest views (~4.1M per data study); 60–90 sec is the new sweet spot per multi-platform 2026 trend reports. Max 3 minutes.
- **Universal benchmark:** target ≥70% completion to trigger viral distribution.

#### Hook patterns (first 3 seconds — 2026)

The 3-second hook is non-negotiable. Templates that consistently work:

- **Visual-first text hook** (text on screen ~0.5s before voiceover): "I tried [X] for 30 days." / "Don't do [common mistake] until you watch this."
- **Pattern interrupt:** unusual visual + bold claim ("This $4 tool replaced my $400 setup.")
- **Curiosity gap with payoff promise:** "There's a reason nobody talks about [X]. I'll show you."
- **Stake/loss-aversion:** "If you're a founder and you're still doing [X], stop."
- **Specificity:** "I lost $11,000 in three weeks. Here's the email that did it."
- **Negation:** "Everyone says [common advice]. They're wrong."

#### Script architecture (Hook → Problem → Solution → CTA)

Dominant 2026 framework (per OpusClip data on 118k+ viral videos). For a 30-sec video:

- **0–3 sec:** hook
- **3–8 sec:** problem/stakes
- **8–25 sec:** payoff/solution with B-roll variety every 1–3 sec
- **25–30 sec:** CTA + loop-back line that makes the start replayable (rewatch >15% is "excellent")

#### Caption conventions

- **TikTok:** 1–2 sentence caption, 3–5 hashtags, niche + broad mix. First 100 chars = in-app search keywords.
- **Reels:** captions matter more in 2026 — Instagram now indexes caption text for Explore. 125 chars before "more"; 3–5 hashtags max (Meta has explicitly said large hashtag stacks no longer help and may hurt).
- **Shorts:** title is the primary search vector. Description is secondary but indexed. **#shorts** is no longer required (since 2024) but doesn't hurt.

#### What works vs. fails (B2B / educational / founder content)

- **Working:** founder talking-head with clear text overlay; before/after demonstrations; "I tested 5 tools so you don't have to" comparison montages; 30–60 sec teardowns of a competitor product; "I built X, here's the demo" with screen capture.
- **Failing:** corporate brand intro videos, anything over 90 sec without strong pacing, generic "tips" listicles voiced by AI, low-resolution uploads (Reels deboosts <1080×1920), reposted TikToks with the watermark on Reels.

#### Banned moves and shadowban triggers

- **TikTok:** spam-like behavior (repeated hashtags, mass-following), undisclosed paid promotion (Branded Content toggle required), unlabeled AI-generated synthetic media of real people, off-platform-promotion in livestreams. Live requires 1,000 followers and 16+ age.
- **Instagram:** engagement bait ("comment YES if you agree"), reposted TikToks with watermark, low-res uploads, sensitive (political/violent/medical-misinformation) content gets reach-suppressed.
- **YouTube Shorts:** YPP requires 1,000 subs + 10M Shorts views in 90 days OR 4,000 hours long-form. Reused content (compilations of someone else's clips with no commentary) is demonetized.

#### AI-content disclosure (2026 — verified, mandatory in many cases)

- **TikTok:** strictest. Mandatory disclosure for AI-generated/significantly-altered *realistic* depictions of people, places, or events. Auto-detects via **C2PA Content Credentials integrated Jan 2025** — auto-labeled 1.3B+ videos. AI-assisted *text* (scripts, hashtags, captions) is exempt. Deepfakes of real public figures used for endorsement are **prohibited entirely**, even with a label. Synthetic media of private individuals is banned even with a label.
- **Meta (Instagram/Facebook Reels):** auto-detects via C2PA metadata, applies "AI Info" label automatically; also accepts manual self-declaration. Does not typically demote labeled AI content.
- **YouTube Shorts:** since early 2025, creators must toggle "altered or synthetic content" disclosure during upload for realistic AI content. Failure can lead to content removal and channel-level penalties for repeat violations.
- **EU AI Act (effective Aug 2, 2026):** EU-targeted content with significant AI generation must be disclosed regardless of platform; fines up to €15M or 3% global turnover.

#### Compliance

- **Financial:** SEC, FINRA on US side. *#NotFinancialAdvice* is not legal cover; UK FCA requires "this is a financial promotion" label on any solicitation.
- **Medical/supplements:** FDA structure-function disclaimer; FTC requires substantiation. TikTok additionally bans certain supplement claims outright (weight loss, fertility, etc.).
- **Crypto:** UK FCA, EU MiCA, US SEC. "This is a financial promotion" is standard. Influencer disclosure required.
- **Branded content:** all three platforms require their native disclosure toggle. Hashtags like #ad alone are not sufficient on TikTok in 2026.

#### Hooks that work in 2026 (specific examples)

- "I built a SaaS that hit $10K MRR. Here's the dashboard."
- "POV: you're 27 and you finally understand compound interest."
- "Three things every junior dev should stop doing in 2026."
- "I asked GPT-5 to do my actual job. This is what happened."
- "The reason your Reels stopped getting views isn't your content."

#### AI-tells / banned phrases creators get roasted for

*"Imagine this:"*, *"Did you know that…"*, *"In a world where…"*, ElevenLabs-default monotone without prosody, AI b-roll that doesn't match the script, GPT-style three-clause structure ("It's not just a tool. It's a mindset. It's a movement."), and any video that ends with *"…and that's why you should follow me!"*. Calling out an "AI face" (Synthesia/HeyGen avatar) is a reliable comment-bait moment.

#### Verdict

All three are essential and growing in 2026. **TikTok** for raw reach; **Reels** for purchase-intent and DM shares; **Shorts** for SEO + funnel into long-form + best monetization. B2B founders increasingly favor Shorts > Reels > TikTok in that order; consumer/lifestyle the reverse.

---

### 8.9 Threads / Bluesky / Mastodon (alt-social)

#### Threads

- **Algorithm:** centralized, AI-personalized "For You" via Meta's "Dear Algo" layer. Heavy weight on follower-graph from Instagram, predicted engagement, and (now in 2026) reply quality. Vertical native video gets boosted.
- **Scale:** ~400M MAU by Sep 2025, outpacing X's mobile DAU. Daily reach is real but reach-per-post is volatile.
- **Fediverse integration:** still partial as of 2026. Threads can publish out to ActivityPub but accepts only limited inbound interactions.
- **Format:** 500-char limit. Posts that get reach: 1 strong opening sentence (provocative or contrarian), vertical video, thread-of-replies-to-self for context. Hashtags exist but are weak signals.
- **Works:** quick takes on tech/news, replying to large accounts (Threads heavily surfaces good replies in others' feeds — the "Now" tab and reply-discovery are real growth levers), trending-topic posts within minutes of news.
- **Fails:** corporate brand voice, link-led posts (links are deboosted), recycled X content (engagement is meaningfully lower).
- **AI content:** Meta auto-labels AI-detected content via C2PA. Cultural tolerance is moderate.

#### Bluesky

- **Architecture:** AT Protocol; no single algorithm. Distribution is via **Following feed** (chronological, reverse-chrono), **Discover feed** (light algorithmic), **custom feeds** (user-created, e.g. Filmsky, Science — your hashtags and keywords determine which feeds you appear in), and **Starter Packs** (curated bundles of accounts new users mass-follow with one click; inclusion in a strong Starter Pack is the single fastest growth lever).
- **Scale:** ~6M active users (Q1 2026), small but engaged. Engagement rate ~4.2% is **2.8× higher** than X's (per Athenic 2025 study).
- **Format:** 300-char limit per post; threads work well; markdown-style links with previews work; 4-image grid supported. Hashtags work (added Feb 2024).
- **Works:** technical posts, science writing, journalist commentary, leftist-political and arts communities.
- **Fails:** crypto, "build in public" hustle-coded SaaS marketing, growth-hacker tone, unlabeled AI art. **Bluesky has explicitly stated it will not allow user content to train AI**, and the community is *strongly* anti-AI; AI prose and AI art draw immediate replies and blocks.
- **Banned moves:** mass-following Starter Packs and immediately unfollowing (gets you on shared block-lists), engagement bait, posting NSFW without proper labeling.
- **Compliance:** crypto promotion is community-suicide; financial newsletters work with full "not advice" framing; medical claims face the same scrutiny as elsewhere.

#### Mastodon

- **Architecture:** ActivityPub federated; thousands of independent instances, each with its own moderation policy. **No algorithm** — chronological only.
- **Distribution mechanics:** **boosts** (the only way content reaches beyond your followers — quote-posts were added in late 2024 but are culturally controversial), **hashtags** (the *primary* discovery mechanism — hashtags are searchable but body text largely is not, by design), **federated/local timelines**, and **introduction posts** (`#introduction` — a strong cultural ritual).
- **Format:** 500-char default (some instances allow more). 4 attachments. Polls supported. **Content Warnings (CWs)** are a cultural cornerstone — used not just for NSFW but for spoilers, long posts, politics, and topics like Twitter/Musk.
- **Cultural rules (strongly enforced socially and by admins):**
  - **Always add alt-text to images.** Posts without get publicly called out; some instance admins remove them.
  - **Use CamelCase hashtags** (#TodayIsMyDay, not #todayismyday) so screen readers can parse them.
  - **Use CWs liberally** for politics, food, eye-contact, spoilers, long threads.
  - **Boost generously** — boosts are the "currency" since there's no algorithm. Likes are nearly invisible.
  - **No screenshots of others' posts to other platforms** without consent.
  - **No engagement-bait, no growth hacking.** "Following for follow-back" is treated as antisocial.
  - **Marketing accounts** are tolerated only if they participate genuinely; ads and tracking pixels get instances defederated.
- **Works:** academic threads, tech deep dives, open-source project updates, photography (with alt-text), data viz, journalist commentary. `#FediTips`, `#introduction`, `#rstats`, `#MacAdmin`, `#BookToot` get reliable discovery.
- **Fails:** brand-voice posts, unlabeled marketing, anything cross-posted from X with X formatting, AI-generated art (instances actively defederate AI-art servers), "thread-of-30-replies" growth-hacker style.
- **AI content:** the most anti-AI of the three. Many instances explicitly defederate AI-art servers and ban AI training on user content. Posting AI prose without a CW will draw rebukes; admins can and do ban accounts they perceive as AI-driven.

#### Hooks across all three

- **Threads:** "[Specific contrarian claim]. Reasons in reply." (drives Now-tab visibility)
- **Bluesky:** "[Specific niche observation that an expert would notice]." (rewarded by custom feeds)
- **Mastodon:** First an `#introduction` post; then content like "I've been working on [project] for 18 months. Here's what I learned about [specific technical detail]. (1/n) #DevToot #OpenSource"

#### AI-tells / community-specific peeves

- **Threads:** Meta-wide AI tells; users mock GPT-default tone.
- **Bluesky:** anti-AI community blocks accounts emitting *"In today's,"* *"Let's explore,"* or three-clause GPT structure; AI emoji clusters (🚀💡✨) are an instant tell.
- **Mastodon:** any post that reads like marketing draws silent unfollows. Cultural test: "would this same content appear on LinkedIn?" If yes, rewrite.

#### Verdict

- **Threads:** worth posting if you already cross-post from Instagram; not worth a dedicated strategy.
- **Bluesky:** worth real investment for tech, science, journalism, B2B SaaS targeting developers; engagement quality significantly higher than X.
- **Mastodon:** worth investment for open-source maintainers, academics, technologists targeting indie/privacy-conscious audiences. *Not* worth investment for brand marketing — culture rejects it and the math doesn't justify.

---

### 8.10 Quora

#### State of the platform (2026)

- **Traffic:** ~837M monthly visits in 2025, **down ~8% YoY** from 910M (June 2024). Daily visitors steady around 27M. ~75% mobile. Bounce rate ~65%, session ~2:39.
- **Most traffic is organic search** (~82%) — Quora's value is essentially as a Google long-tail destination. Direct ~17%, social <1%.
- **Valuation:** marked down from $1.8B (2017) to **$500M** in the Jan 2024 a16z $75M raise — almost entirely directed to Poe, not core Quora. Excluding Poe, Quora is cash-flow positive.
- **Poe** is the strategic focus: ~31.5M monthly visitors (Sep 2024), >1M custom bots by 2026, $5/$19.99/$199.99 plans. Quora's identity in 2026: "Poe + a legacy Q&A site that feeds Poe."

#### Algorithm and distribution (2026)

- Answer ranking weights: question-author asks, upvotes from credentialed users (Quora attempts to weight credibility from your bio), recency on trending questions, view-through rate, and on-platform engagement.
- **AI bot integration:** Quora ranks Poe-bot answers alongside human ones in some surfaces, which is widely controversial. Many top-writers have left because of this. Reader trust has eroded.
- **Spaces** still exist but engagement has flatlined — most active Spaces are Poe-related.
- Google's AI Overviews and Perplexity continue to cite Quora answers as sources for long-tail conversational queries; getting cited there is a meaningful side benefit, but it favors *long, well-cited* answers, not snappy ones.

#### Format and length

- **Optimal answer:** 250–600 words. One personal anecdote/credential establishing why you can answer, then a structured response with sub-bullets, then a one-line summary.
- Headlines aren't yours — you're answering an existing question.
- Images and embedded video improve dwell time.

#### What works vs. fails

- **Works:** medical questions (when written by an actual MD with credentials in profile), specific niche-expertise answers, location-specific questions (immigration, regional cost-of-living), software dev troubleshooting where Stack Overflow's auto-close has rejected the question.
- **Fails:** generic life-advice answers (drowned in AI), business/marketing answers (low signal), opinion-on-current-events (ranked low, often suppressed for civility).

#### Community norms / banned moves

- BNBR ("Be Nice, Be Respectful") policy is aggressively enforced — sarcasm gets you collapsed/banned.
- Self-promotion in answers without disclosure violates ToS.
- Heavy outbound linking to your own site triggers spam detection.
- Republished answers from your blog can get auto-flagged.

#### AI content

The community is **deeply ambivalent**. Quora itself integrates AI bot answers into the experience, but user-submitted AI answers without disclosure get flagged and removed. Dominant 2025–2026 sentiment: "Quora is becoming AI-content-overwhelmed." Disclosure norm if you used AI to draft: prefix with "(I used AI for the structure of this answer; the substance is from my experience as a [credential])."

#### Compliance

- Medical answers without credentials get flagged or buried; medical professionals get badge support that lifts ranking.
- Financial answers: standard "not advice" — Quora's policy auto-adds context warnings on certain financial-advice questions.
- Affiliate/promotional links get aggressively detected and removed; FTC disclosure isn't enough.

#### Hooks/openings that work

- "I've been a [credentialed role] for [N] years. Here's what people get wrong about [topic]:"
- "I asked this exact question to three experts. They disagreed. Here's the synthesis:"
- "Short answer: [specific claim]. Long answer below."

#### AI-tells / banned phrases

*"Great question!"* (mocked in every Quora answer thread), *"It's important to note,"* *"There are several factors,"* *"Hope this helps!"*. The community now treats these as proof of GPT drafting.

#### Verdict

**Declining but not dead.** Best understood in 2026 as: (a) a long-tail SEO surface that Google AI Overviews still cites, (b) a place credentialed experts can build a small audience, (c) an on-ramp to Poe. **Not viable** as a primary content channel for serious creators in 2026. Ship important content elsewhere; cross-post to Quora only when there's a perfect-match question with high view count.

---

### 8.11 Indie Hackers

#### State of the platform (2026)

- **Spun back out of Stripe in April 2023.** The Allen brothers (Courtland & Channing) are now majority owners; Stripe remains an investor. The site is independent.
- **Activity:** lower than 2019–2021 peak, but the homepage has remained active, daily new "milestone" posts continue, growth in 2025 has been steady (the @IndieHackers X account ~142k followers; r/indiehackers ~115–117k members; the IH homepage gets daily $X-MRR posts).
- The community has fragmented across X "build in public," r/SaaS, r/Entrepreneur, the IH forum, and Discord servers. Indie Hackers itself is now the *long-form* surface; X is where the daily conversation happens.

#### Algorithm and distribution

- Homepage lists posts by recency + upvotes + comment activity. **Milestones** feed (`/milestones`) for product-revenue updates.
- The most reliable distribution path in 2026: post a milestone → get into the daily/weekly newsletter (still ~85k+ subs) → that drives the bulk of comment activity.
- Posts that hit homepage almost always have a specific revenue number, a specific time period, a specific takeaway, and the founder *engaging in comments*.

#### Format conventions ("I built X in N months and it makes $Y")

The canonical 2026 format (verified from 2025–2026 hit posts like *"Hitting $23k MRR in six months after five failures,"* *"From $0 to $1K MRR in 8 Months,"* *"My 2 Year Journey to $10K MRR"*):

1. **Title:** specific outcome + duration. ("From $0 to $10k MRR in 4 Months: My Indie Hacker Journey.")
2. **Opening:** TL;DR sentence, then "I'm [name], building [product]." Establish ICP fast.
3. **Backstory:** vulnerability is *required* — failures, layoffs, runway anxiety, prior flops. The community trusts founders who've lost.
4. **The pivot/insight:** the specific pattern recognition that worked.
5. **The numbers:** revenue dashboard, customers, growth rate, ideally a Baremetrics screenshot.
6. **Lessons (3–7):** specific, actionable; *no* generic "stay consistent" advice.
7. **What's next:** a specific revenue or product goal.
8. **CTA:** a question to the community ("Curious — for those of you past $10K MRR, did pricing or distribution drive you the most?")

#### What works vs. fails

- **Works:** raw revenue transparency, screenshots of dashboards, specific channels ("X organic + Reddit + SEO"), "I tried 12 startups and 11 failed" series, AI-product builder transparency.
- **Fails:** "How to grow your SaaS" generic playbook posts, posts without numbers, posts that read like LinkedIn humblebrags, AI-written posts (immediately roasted in comments), posts where the founder doesn't engage with replies.

#### When to use Indie Hackers vs. r/SaaS vs. r/Entrepreneur

- **Indie Hackers:** when you have a *specific, vulnerable, numbers-backed* milestone post. Higher-quality discussion, smaller audience, often leads to interviews/podcasts.
- **r/SaaS** (~250k members): when you have a *technical/product* SaaS question or a launch announcement. Less tolerant of generic content. Mods quick to remove low-effort posts.
- **r/Entrepreneur** (~4M+ members): big reach, low signal. Best for genuinely entertaining/dramatic stories. Be ready for "show me the numbers or this didn't happen."

#### Community norms / banned moves

- Don't post pure marketing with no transparency.
- Don't claim revenue you can't back up — comments will press; if you stonewall, you lose credibility.
- Don't repost the same milestone every week.
- Don't ghost comments — the community expects founder replies within 24h.
- Don't @mention or DM-spam users to upvote.

#### AI content

The community is *extremely* AI-fluent (most products discussed *are* AI products), but they hate AI-written *posts*. Dominant 2025–2026 reaction to AI-prose milestone posts: mockery and downvotes. Disclose if you used AI to outline; never let it write the personal sections.

#### Compliance

- Affiliate disclosures expected.
- Crypto/get-rich-quick filtered out by mods.
- "Revenue" must be MRR, not lifetime revenue or revenue run-rate, without explicit labeling.

#### Hooks that work in 2026

- "From desperation and dwindling runway to $10k MRR"
- "I launched 12 startups in 12 months. 11 flopped. The 12th is at $23k MRR."
- "I gave 7 AI agents $100 each to build a startup. Here's Day 1."
- "I launched on Product Hunt today with 0 followers, 0 network, and 0 users."
- "How I reached $4,000 MRR in two months — and the pricing mistake I almost made"

#### AI-tells / banned phrases

*"In the ever-evolving SaaS landscape,"* *"key takeaways,"* *"leverage,"* *"unlock growth,"* *"actionable insights,"* the four-bullet summary at the end of every section, and any post with zero "I" statements.

#### Verdict

**Alive and worth using selectively.** Not as central to indie SaaS culture as 2019–2021, but still the best long-form home for milestone posts. Pair Indie Hackers + X for distribution; treat Reddit r/SaaS and r/Entrepreneur as secondary surfaces.

---

### 8.12 Dev.to / Hashnode (developer publishing)

#### Dev.to

- **Algorithm:** tag-feed + home-feed + weekly/monthly trending ("top posts of the week"). Editor-curated trending lists. Reactions (♥ 🦄 🔖) and comments both feed visibility; in 2025–2026 the **save (🔖 bookmark) is the strongest "quality" signal**.
- Distribution lives inside the dev.to domain — your post stays on their URL, but they support **canonical URLs** so you don't lose SEO from your own blog.
- **Format:** Markdown editor; cover image (1000×420 ideal); 3–4 tags max (`#javascript`, `#webdev`, `#beginners`, `#tutorial` are highest-traffic); TL;DR at top works.
- **Works:** "I built X with Y" project posts, beginner-friendly tutorials with extensive screenshots and code blocks, "X things I wish I knew when I started [role]" lists, hot-take career posts, post-mortems on bugs/incidents.
- **Fails:** marketing-coded posts, AI-written tutorials with hallucinated APIs (the comment section is brutal — devs run code), short opinion pieces, content with broken/outdated code blocks.
- **Optimal length:** 800–2,000 words for tutorials; 400–800 for opinion/career. Code blocks should be ≥30% of visible content for tutorials.

#### Hashnode

- **Architecture:** hybrid — your posts live on **your own custom domain** (free domain mapping is the killer feature) AND distribute through the Hashnode network feed.
- **Distribution:** Hashnode **Featured** section, topic feeds (#oracle, #aws, etc.), and SEO from your own domain (long-term compounding).
- **2026 working patterns:** technical deep dives, AI/ML implementation walkthroughs, "X days of [topic]" series, framework-specific tutorials. Hashnode 2026 data: posts with code snippets and diagrams achieve **2× engagement vs. text-only**.
- **Fails:** opinion-only posts (less audience), career-advice posts (less engagement than dev.to), short pieces.
- **Trade-off vs. Dev.to:** Hashnode's traffic per featured post is generally lower than dev.to's, *but* it builds your owned domain authority instead of dev.to's. Multiple developer-survey 2025–2026 posts concur: **Hashnode for ownership, Dev.to for reach.**

#### Cross-posting strategy (2026)

The best practice (cited in TechContentPro 2026 benchmark): publish first on **your own blog** (Hashnode-mapped or self-hosted), then cross-post with `canonical_url` set to your blog on Dev.to and Medium. ContentIQ Analytics shows verbatim cross-posts without canonical see ~65% drop in organic traffic over 6 months.

#### Optimal article length and structure for technical tutorials (2026)

- 1,200–2,500 words for tutorials.
- One H1, H2 every ~300–500 words.
- Code-block ratio: ~30% for tutorials, ~15% for conceptual posts.
- Cover image 1200×630 (OG-card friendly).
- TL;DR at top; "what you'll learn" bullet list; numbered steps for tutorials; final "what's next/related reading" section.
- Embed working examples (CodeSandbox, StackBlitz) when possible — boosts retention significantly.

#### AI content (developer-specific reception)

This is the platform category where AI-content reception is **most hostile** — because developers can run the code:

- **Hallucinated APIs**, made-up library functions, or syntactically-clean-but-wrong examples get torn apart in comments.
- "ChatGPT wrote this" is the most cutting Dev.to comment.
- Hashnode is slightly more permissive (the platform itself ships AI-writing features), but the audience remains skeptical.
- Best practice: if you used AI, *say so*, and explicitly state that you ran every code block. Disclose AI involvement at the top.

#### Community norms / banned moves

- **Dev.to** has an active Code of Conduct; harassment/dismissiveness is moderated.
- Don't paste affiliate links without disclosure.
- Don't post "click here for full article on my site" stub posts (community calls these out; mods may unpublish).
- Don't auto-post from RSS without canonical handling.
- Don't use `#beginners` tag for advanced content (tag editors will downrank).

#### Compliance

- For developer audiences, the relevant compliance is **license disclosure** for code samples (MIT, Apache, etc.) and security-disclosure norms for vulnerability writeups (responsibly-disclosed and patched before publication).
- For tools/services you promote: disclose any commercial relationship at the top, not the bottom.

#### Hooks/titles that work in 2026

- "I built a Postgres clone in 1,200 lines of Rust"
- "What `fork()` actually copies (with strace traces)"
- "7 Days of Docker in 2026 — Day 4: when containers need to talk and remember"
- "I migrated 4M rows from MongoDB to Postgres with zero downtime. Here's the runbook."
- "Why I'm moving my blog from Dev.to to Hashnode" (a perennial format)

#### AI-tells / banned phrases that get developers especially mad

*"Let's dive in!"*, *"In the ever-evolving world of [tech],"* the *"What is [X]? Why is it important?"* H2 ladder, code samples without imports, code that uses fictional methods (e.g. `array.shuffle()` in JS), captions like *"This simple trick will make you 10x faster"*, the closing *"By following these best practices, you'll be well on your way to..."* sentence, and the signature `console.log("Hello, World!");` in a tutorial about an unrelated topic (it's a meme tell now).

#### Where developers should publish in 2026 (honest assessment)

- **Your own blog (custom domain) → primary canonical.** Best long-term SEO, ownership, brand.
- **Hashnode with custom domain mapping → equivalent to your own blog**, with bonus discovery from the network. Excellent default for devs without DevOps appetite.
- **Dev.to → cross-post for reach.** Larger audience, more comments, better top-of-funnel.
- **Medium → cross-post only if you have a non-developer adjacent audience.** Medium's developer audience has shrunk; not worth being primary.
- **Substack → only if your dev content is opinion/essay-shaped, not tutorial-shaped.** Tutorials don't render well in email.
- **Hacker News → submit your *best* original-research piece, once per quarter, to your own blog URL.**

#### Verdict

**Both alive and worth using.** Best 2026 stack for developer content: **Hashnode-on-your-domain (canonical) → cross-post to Dev.to → submit milestone pieces to HN.**

---

### 8.13 Cross-platform repurposing

If the user has an article or LinkedIn post and wants the same idea across multiple platforms, Pubcraft does **not** copy-paste it. Each platform requires structural rewrite:

- **Article → LinkedIn:** Pull the single most contrarian or specific finding. 1,300–1,900 chars. Hook with a number.
- **Article → X long-form:** Pull the data + a stance. 800–1,500 chars. Sentence-broken paragraphs.
- **Article → X thread:** Only if the article has 4–6 genuinely sequential beats. Otherwise long-form post.
- **Article → Reddit:** Total rewrite into first-person experience. Original framing required (don't link the article, *re-explain* in the platform's voice). Disclose authorship.
- **Article → Product Hunt:** Doesn't apply. Product Hunt is a launch event, not a content distribution channel.
- **Article → Newsletter (Substack/Beehiiv):** Lead with the *one* finding that's most personally interesting to you. Add a paragraph of behind-the-scenes context the article didn't include. Subject line is a fresh hook, not the article headline. Single primary CTA.
- **Article → Medium:** Re-frame as a personal essay. Open with stake, add personal scenario, keep the data. Set canonical URL back to your blog. Without canonical, expect ~65% organic-traffic drop on the original over 6 months.
- **Article → Hacker News:** Submit *only* the original research/data piece, with the article's own title (no editorializing). One submission per quarter, max. Don't ask for upvotes anywhere.
- **Article → Short-video (TikTok/Reels/Shorts):** Pull *one* finding. Build a 21–34s script (Hook → Problem → Solution → CTA). Visual-first text hook in first 0.5s. Disclose AI involvement if synthetic media of real people is used.
- **Article → Threads/Bluesky/Mastodon:** Threads — single contrarian sentence with "reasons in reply." Bluesky — niche-expert observation; lean technical. Mastodon — start with `#introduction` if new; CW long posts; alt-text every image; CamelCase hashtags.
- **Article → Quora:** Find a *perfect-match* high-view question. Open with credentials. 250–600 words. Don't link to the source article in-line.
- **Article → Indie Hackers:** Only if the article is a *milestone* (revenue, product) post. Rewrite into the canonical format (title with $ and time, vulnerable backstory, numbers, lessons, what's next, community question).
- **Article → Dev.to / Hashnode:** Set canonical URL back to your blog. Add a TL;DR, "what you'll learn" bullets, working code blocks (≥30% of visible content for tutorials), CodeSandbox/StackBlitz embed when possible.

---

## PART 9 — How Claude Should Operate

When invoked, Claude should:

1. **Read this entire skill** before starting.
2. **Confirm the brief** (audience, query, length, tone, vertical, **target platform**) if any are missing.
3. **Route to the right part of the skill based on output type:**
   - Article / blog post / SEO page → Parts 1–7.
   - LinkedIn post → Part 8.1.
   - X (Twitter) post or thread → Part 8.2.
   - Reddit post or comment → Part 8.3.
   - Product Hunt launch copy → Part 8.4.
   - Newsletter (Substack or Beehiiv) → Part 8.5.
   - Medium essay → Part 8.6.
   - Hacker News submission or comment → Part 8.7.
   - Short-video script (TikTok / Reels / Shorts) → Part 8.8.
   - Threads / Bluesky / Mastodon post → Part 8.9.
   - Quora answer → Part 8.10.
   - Indie Hackers milestone post → Part 8.11.
   - Dev.to or Hashnode developer post → Part 8.12.
   - Cross-platform repurposing → Part 8.13.
   - Cross-platform AI-disclosure or priority decisions → Part 10.
4. **Run web_search and web_fetch** to gather primary sources. State when sources cannot be located rather than hallucinate.
5. **Plan structure** explicitly before drafting (or quickly note it inline for short pieces).
6. **Draft following the platform's rules.** For social posts, follow Part 8 conventions exactly — character counts, format, hook patterns, banned moves.
7. **Run the self-audit (Part 3.5 + Part 7).** The anti-AI-slop style rules in Part 3 apply to *every* output, including social.
8. **Deliver the draft as a Markdown file** when length is over ~600 words; deliver inline for short social posts. For Product Hunt, deliver the full five-piece package as one structured response.
9. **Mention any [COMPLIANCE TBD] placeholders** and recommend human review.
10. **Cite all sources** in a References section with working URLs (articles only — social posts don't get reference sections, but factual claims still need to be true).
11. **Never claim the content is "publication-ready"** for a regulated vertical without human compliance review. Be direct about what the user still needs to do.

### What this skill cannot do

- **No skill substitutes for human compliance review.** Disclaimer templates are starting points, not legal advice. Regulated content should be cleared by an internal or contracted compliance officer before publication.
- **Search and platform policy moves fast.** This skill reflects April 2026 state. Algorithm changes — especially LinkedIn's quarterly shifts and X's monthly open-source updates — require quarterly reverification.
- **AI detection tools are imperfect.** Originality.ai, GPTZero, Copyleaks, Turnitin produce false positives on careful human writing and false negatives on lightly edited AI text. Use them as sanity checks, not gates.
- **The biggest publication risk is not Google.** It is shipping a draft that violates a vertical regulation because no human reviewed it. Build a human gate between Claude's output and publication.
- **No launch-day operations.** For Product Hunt and Reddit specifically, Pubcraft drafts the copy. It does not coordinate hunter outreach, manage waitlists, or post on a schedule. That's an ops layer outside this skill's scope.

The aim is to make Claude an effective junior writer for a high-quality publication — not to replace the credentialed expert, the compliance officer, or the editor. Claude's job is to produce researched, structured, accurate, on-brand drafts that humans can clear in minutes rather than hours.

---

## PART 10 — Cross-Platform Reference Tables

Use these tables for fast lookups during routing decisions. They summarize content already covered in Parts 6 and 8; the per-platform sections remain authoritative on conflict.

### 10.1 AI-content policy and community sentiment (April 2026)

| Platform | Platform policy | Detection | Community sentiment |
|---|---|---|---|
| Substack | Allowed; deboosted on Notes if obvious | None automated | Mixed (anti in literary/journo niches) |
| Beehiiv | Allowed and tooled (built-in AI writer) | None | Neutral |
| Medium | AI-only earning is bannable | Boost-editor judgment | Strongly anti AI-prose |
| Hacker News | Allowed but flagged | Community flagging | Strongly anti |
| TikTok | Mandatory disclosure for realistic AI; deepfakes of real people banned | C2PA + auto-detect; 1.3B+ auto-labeled | Mixed |
| Instagram Reels | Auto-labels via C2PA | Automated | Mixed |
| YouTube Shorts | Mandatory toggle for realistic AI | Manual + automated | Mixed |
| Threads | Auto-labels via Meta C2PA | Automated | Moderate |
| Bluesky | No platform AI labeling; community-driven | None | Strongly anti |
| Mastodon | Instance-by-instance; many ban AI art | Manual reporting | Strongly anti |
| Quora | Mixed (Quora itself uses Poe bots); user-AI must disclose | Spam detection | Anti and fatigued |
| Indie Hackers | Allowed with disclosure | None | Anti AI-prose, pro AI-products |
| Dev.to | Allowed with disclosure norm | None | Strongly anti hallucinated code |
| Hashnode | Allowed; AI features built in | None | Skeptical |
| LinkedIn | Allowed; classifier deboosts generic AI patterns | Automated classifier | Anti AI-prose |
| X (Twitter) | Allowed; Grok layer reads every post | Automated (sentiment) | Mixed |
| Reddit | Allowed; subreddit-by-subreddit | AutoMod + community | Strongly anti in most subs |
| Product Hunt | Allowed; doesn't affect featuring | None | Skeptical of AI-only products |

**EU AI Act (effective Aug 2, 2026):** every platform serving EU readers must disclose AI-generated content that appears realistically human-authored and was not editorially reviewed. Non-compliance: up to €15M or 3% global turnover. This is a *publisher* obligation — apply it regardless of whether the platform itself enforces.

### 10.2 Effort-investment priority (April 2026, honest take)

**Definitely worth the effort:**
- Beehiiv or Substack (own audience).
- Hashnode-on-your-domain + Dev.to (developer audience).
- Bluesky (technical / journo / B2B SaaS targeting devs).
- Hacker News (one shot per quarter, original work only).
- Indie Hackers (milestone posts only).
- Short-video (TikTok / Reels / Shorts) — pick 1 primary, 2 secondary based on audience.
- LinkedIn (B2B; document carousels and named-scenario teardowns).
- X (Premium required for serious creators in 2026).
- Reddit (highest leverage *if* the subreddit decision tree is followed).

**Selectively worth it:**
- Medium — only for credentialed essayists; not as a content-mill side hustle.
- Threads — only as cross-post from Instagram; not a dedicated strategy.
- Mastodon — only for open-source / academic / privacy-conscious audiences; *not* for brand marketing.
- Product Hunt — only when there's a real launch event.

**Largely not worth it as a primary channel:**
- Quora — declining; cross-post only when a perfect long-tail question exists with high view count.

### 10.3 Format quick-reference

| Platform | Body limit | Optimal length | Hero/cover image | Native video |
|---|---|---|---|---|
| Substack post | none | 800–2,500 words (paid) / 300–800 (free) | 1456×816 | up to 90 min audio/video |
| Substack Notes | ~5,000 chars | 280–500 chars | 1080×1080 | 60s |
| Beehiiv post | none | 600–1,500 words | 1200×600 | n/a (embed) |
| Medium article | none | 1,200–2,000 words | 1500×750 | embed only |
| HN submission | 80-char title | n/a (link) | n/a | n/a |
| HN comment | none | 2–6 sentences | n/a | n/a |
| TikTok | 2,200-char caption | 21–34s video | n/a | up to 10 min |
| Reels | 2,200-char caption | 7–30s (reach) / 30–60s (educational) | n/a | up to 3 min |
| YouTube Shorts | 100-char title, 5,000-char description | 50–60s | 1280×720 thumb | up to 3 min |
| Threads | 500 chars | 1 strong sentence | n/a | vertical native |
| Bluesky | 300 chars | full | up to 4 images | up to 60s |
| Mastodon | 500 chars (default) | full + CW for long | up to 4 attachments | up to 60s (instance-dep) |
| Quora answer | none | 250–600 words | embed | embed |
| Indie Hackers post | none | 600–1,800 words | 1200×630 | embed |
| Dev.to | none | 800–2,000 words (tutorials) | 1000×420 | embed |
| Hashnode | none | 1,200–2,500 words (tutorials) | 1200×630 | embed |
| LinkedIn text | 3,000 chars | 1,300–1,900 chars | 1200×627 | up to 10 min |
| LinkedIn carousel | n/a | 5–10 slides | 1080×1350 portrait | n/a |
| X single post | 280 chars | 240–270 chars | up to 4 images | up to 2 min 20s |
| X long-form (Premium) | 25,000 chars | 800–2,500 chars | up to 4 images | up to 3 hr |
| Reddit post | 40,000 chars | 200–800 words (most subs) | inline | inline |
| Product Hunt tagline | 60 chars | < 60 chars | n/a | n/a |
| Product Hunt description | 260 chars | < 260 chars | n/a | n/a |
