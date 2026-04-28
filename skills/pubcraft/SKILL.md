---
name: pubcraft
description: Use this skill when the user asks for an article, blog post, long-form content, SEO content, or social posts for LinkedIn, X (Twitter), Reddit, or Product Hunt — any content intended for public publication. Trigger on requests like "write an article about X", "draft a blog post on Y", "write a LinkedIn / X / Reddit post", "create SEO content", "Product Hunt launch copy", "write a guide to Z", or when content will be published online. Produces researched, E-E-A-T-compliant, platform-native, human-reading content that ranks in Google and survives current spam/AI-content policies. Covers Google search articles, LinkedIn (360Brew algorithm), X (open-source Grok ranking, reply-weight economics), Reddit (community-fit and AI-search-citation), and Product Hunt (post-2024 curated featuring). Includes mandatory web research, source citation, anti-AI-slop style enforcement, and YMYL/regulated-vertical compliance handling. Do NOT use for internal docs, code comments, technical documentation, or transient chat answers.
---

# Pubcraft

Operating instructions for producing researched, publishable web content (articles, blog posts, LinkedIn posts) that ranks in Google, satisfies E-E-A-T, reads as authentically human, and complies with platform and regulatory constraints.

**Last research date:** April 2026.

---

## When to use this skill

Use it when:
- The user asks for an article, blog post, guide, explainer, comparison, how-to, listicle, or pillar page intended for a website.
- The user asks for a LinkedIn, X (Twitter), Reddit, or Product Hunt post intended for publication.
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

### 8.5 Cross-platform repurposing

If the user has an article or LinkedIn post and wants the same idea across X, Reddit, and Product Hunt, Pubcraft does **not** copy-paste it. Each platform requires structural rewrite:

- **Article → LinkedIn:** Pull the single most contrarian or specific finding. 1,300–1,900 chars. Hook with a number.
- **Article → X long-form:** Pull the data + a stance. 800–1,500 chars. Sentence-broken paragraphs.
- **Article → X thread:** Only if the article has 4–6 genuinely sequential beats. Otherwise long-form post.
- **Article → Reddit:** Total rewrite into first-person experience. Original framing required (don't link the article, *re-explain* in the platform's voice). Disclose authorship.
- **Article → Product Hunt:** Doesn't apply. Product Hunt is a launch event, not a content distribution channel.

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
   - Cross-platform repurposing → Part 8.5.
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
