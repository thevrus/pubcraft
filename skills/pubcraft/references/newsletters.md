# Substack / Beehiiv / Ghost (newsletters)

Load this reference when drafting a newsletter issue.

## Reality check (April 2026)

Newsletters are alive and growing. Beehiiv's State of Newsletters 2026 reports paid-subscription revenue across the platform jumped from ~$8M in 2024 to **$19M in 2025 (138% YoY)**, with median time-to-first-dollar for newsletters launched in 2025 down to **66 days**. Niche/specialist publications outperformed generalist ones. The two platforms are not interchangeable:

- **Substack** has shifted from email tool to recommendation network. Distribution comes from three surfaces: (1) **Notes** (algorithmic short-post feed inside the app, reply-weighted; functions like a Threads/X clone), (2) **writer recommendations** (a larger publication recommending you can deliver hundreds of subscribers in a day), and (3) the **app's Inbox/Discover** home (weighted by reading time, restacks, recommendations from followed writers). Substack still takes 10% of paid subs + ~3% Stripe. SEO-weak. Strong for *writers, essayists, journalists*.
- **Beehiiv** has effectively no internal social feed. Distribution comes from (1) **Boosts** — a paid CPA marketplace where other newsletters earn $1–$6+ per subscriber referred, (2) **Recommendations** (free reciprocal cross-promotion), (3) the **Beehiiv Ad Network** (monetization, not growth), (4) **SEO** of the public web archive (indexable structure, sitemaps, custom domains), and (5) referral programs you build yourself. Flat $34–$99/mo, 0% take-rate on subscriptions. Strong for *operators, B2B, ad/sponsorship-monetized newsletters, anyone who wants ownership and SEO*.

## Open-rate norms (post-MPP, 2025–2026)

Apple Mail Privacy Protection has inflated reported opens; verified-open rates from Beehiiv's filtered analytics are the more honest number.

- **Healthy engaged niche:** 35–45% verified open rate.
- **Average:** 20–30%.
- **Below 20%:** deliverability red flag.
- **Click-through:** 6–14% for top performers; clicks > opens as the trust metric in 2026.

## Format and length

- **Subject line:** 30–50 characters. Lower-case-ish. Curiosity or specific number. Plain-text, not headline-y.
- **Preview text** (~90 chars) is a *second subject line*. Never leave it auto-generated.
- **First line above the fold** must work as a third hook — many readers see only the inbox preview.
- **Body length:**
  - Substack paid post: 800–2,500 words.
  - Substack free post / Notes: 300–800 words / 280–500 chars respectively.
  - Beehiiv retention sweet spot: 600–1,500 words with one CTA.
- **Notes:** image attachments lift restacks substantially.
- **Pattern that works:** strong personal subject line → 1-line hook → bolded TL;DR → scannable subheads → one image or chart → single primary CTA. Avoid more than 2 links above the fold.

## What works vs. fails

- **Working:** niche/specialist publications, weekly cadence, recommendations from 2–5 aligned writers, paid posts with a free preview ~30%, "build in public" revenue/learning posts, deeply personal essays, straight-news rewrites.
- **Failing:** generalist "thoughts on tech" newsletters, Substack growth without Notes participation, low-effort AI rewrites of other people's posts (deboosted on Notes), Beehiiv newsletters that buy too many Boost subscribers (engagement collapses, deliverability suffers).

## Community norms / banned moves

- **Substack:** writer/reader culture is anti-spam, tolerant of self-promotion *if you give first*. Cross-posting hot takes from X is acceptable on Notes but seen as low-effort if it's your only output.
- **Beehiiv:** there is no "community" — readers are your list. The deliverability system enforces: don't deceive in subject lines, don't bait-and-switch links, don't import lists you didn't earn. Cold imports tank sender score.

## AI content

- **Substack** does not ban AI but deboosts obviously templated AI prose on Notes; pure-AI publications get fewer recommendations. Reader culture is *strongly* anti-AI in literary, essay, and journalism niches; in technology and finance niches, "I used AI to research X" is fine.
- **Beehiiv** bundles an AI writer as a feature — explicitly pro-AI-assistance. No detection, no labeling.

## Compliance

- **Financial newsletters:** SEC Investment Adviser rules can apply if you publish individualized advice. Standard disclosure: *"Not investment advice. For educational purposes only."* + FTC affiliate disclosure on any link.
- **Medical/supplements:** *"Not medical advice. Consult your physician."* + *"These statements have not been evaluated by the FDA"* on any structure-function claim.
- **Crypto:** FTC + state-level treatment of newsletter promos as endorsements. Disclose holdings, paid placements; *"This is not financial advice"* near-universal in the finance niche.
- **EU AI Act (effective Aug 2, 2026):** EU readers must see a disclosure if AI-generated text appears realistic-human-authored and was not editorially reviewed.

## Hooks that work in 2026

- "I spent 90 days running both Beehiiv and Substack. Here's the math nobody shows you."
- "There's a reason your open rate dropped in March. It wasn't your subject lines."
- "Three weeks ago I almost shut this newsletter down. Here's what changed my mind."
- "The chart that broke my Q4 strategy" (image-led)
- "I lost 412 subscribers last month. Worth it. Here's why."

## AI-tells / banned phrases on these platforms

Subscribers and Notes commenters call out: *"In today's fast-paced world,"* *"navigate the complexities,"* *"unleash/unlock the power of,"* *"delve into,"* *"it's important to note,"* *"in conclusion,"* *"Let's dive in!"*, em-dash-heavy three-clause sentences, and *"Have you ever wondered…?"*. The **"Picture this:"** opener and tri-colon list patterns ("It's not just X. It's Y. It's Z.") are mocked.

## Ghost — the third major option (April 2026)

Ghost is the **self-hosted, full-control, professional publication platform** alongside Substack and Beehiiv. Distinct positioning, distinct trade-offs.

**Pricing (post-Ghost 6.0, August 2025 increase):** Ghost Pro starts at **$15/month and $29/month** (up from $9 and $25). Self-hosted is free if you operate your own infrastructure (Ubuntu 24, Node 22, MySQL 8 stack as of Ghost 6.0). Ghost takes **0% transaction fee** — Stripe processes payments directly into your account at ~2.9% processing. Substack takes 10%; Beehiiv has tiered platform pricing.

**Ghost 6.0 (released August 4, 2025) is the major story.** Ghost shipped:

- **Native ActivityPub integration** — every Ghost publication is a followable profile (`@you@yourdomain.com`) in the fediverse. Posts and short-form Notes can be discovered, followed, liked, and replied to from Bluesky (via Bridgy Fed), Mastodon, Threads, Flipboard, WordPress, Pixelfed, and any ActivityPub-compatible client. Ghost's answer to Substack Notes and Beehiiv Boost — but on an open protocol you don't depend on a single platform for.
- **Native first-party analytics** (built on Tinybird) — real-time visitor data, traffic sources, newsletter performance, member growth, all without Google Analytics or third-party trackers. Cookie-free.
- **Notes** — short-form content type so Ghost publishers can post to the social web without a separate platform.

**Ghost as a business in 2026:** Ghost reports $8.5M annual revenue (up from $4M at Ghost 5.0 in 2022); publishers on Ghost have collectively earned **$100M+** in subscription revenue. Independent non-profit; 100% of revenue is reinvested.

**The "Lenny / Casey Newton / Stratechery moved to Ghost" narrative is partially true and ongoing.** Casey Newton's Platformer, 404 Media, The Browser, Garbage Day, Blood in the Machine, and many others run on Ghost. Lenny Rachitsky remains on Substack. Ben Thompson's Stratechery runs on a custom stack with parts powered by Ghost-adjacent infrastructure. The August 2025 ActivityPub release accelerated migrations, especially among publications uncomfortable with Substack's content-moderation track record (the December 2023 Nazi-newsletter incident, recurring push-notification controversies).

### Distribution mechanics

Pre-Ghost-6.0, Ghost had **no built-in social network** — distribution was 100% SEO + your existing audience + manual cross-promotion. **Post-Ghost-6.0, Ghost has the open social web (ActivityPub) as its discovery layer**, but it is not a Substack-Notes-style internal recommendation engine. There is no algorithmic boost lane, no "Network" recommending you to other Ghost publications. Distribution remains substantially **SEO-driven** plus whatever you bring.

**Honest assessment:** This is an advantage (no platform tax, no algorithm suppressing your links, no platform that can change terms on you) **and** a disadvantage (no organic-discovery flywheel from day 1 the way Substack Notes can produce). Ghost is excellent for writers with an existing audience; it is a slower start for anyone needing platform-driven cold-start growth.

### Format and length

Ghost publications skew **longer-form and more professional** than the median Substack — the Stratechery / Newcomer / Garbage Day / 404 Media / Platformer model. Working word-count range: **1,500–4,000 words for flagship posts**, with a separate cadence of shorter Notes via ActivityPub.

**Email + web parity:** Ghost publishes every issue as both an email and a webpage with full SEO control (custom meta tags, canonical URLs, XML sitemaps, JSON-LD schema, full Google Search Console integration). This is Ghost's structural advantage over Substack and Beehiiv, both of which have weaker web/SEO infrastructure.

**Member-only paywall mechanics:** Built-in. Free tier, paid tier, and tiered pricing supported natively. Stripe direct connection means you own the billing relationship — there is no Ghost middleman to remove.

### AI-content stance

Ghost is **platform-neutral on AI**. No Ghost-side AI-content policy, no required disclosure, no detection. The community of Ghost publishers skews **professional/serious/B2B**, and the implicit norm is that AI-assisted writing is fine but AI-generated mass content is reputationally damaging — the same calculus as the rest of serious media.

## Verdict — Substack vs. Beehiiv vs. Ghost

**Choose Substack when:**
- You need organic discovery from day 1 (Notes + recommendations are the fastest cold-start engine of the three).
- Simplicity is non-negotiable.
- You don't mind the 10% revenue cut as the price of distribution.

**Choose Beehiiv when:**
- Your model is growth-obsessed and ad-supported (the Boost referral network and ad marketplace are unmatched).
- You're operating a newsletter as a business (not a publication brand).
- You want better automation/segmentation than Substack and don't need Ghost's level of SEO/CMS depth.

**Choose Ghost when:**
- You already have an audience you can bring (newsletter list, social following, existing readership).
- Your publication is long-form, professional, or B2B.
- You want SEO as a primary growth channel — Ghost's website is a real CMS that ranks; Substack's web presence is comparatively weaker.
- You want full ownership: your content, your domain, your data, your billing.
- You are comfortable with basic infrastructure (or you use Ghost Pro).
- You're operating a **media company**, not just a newsletter.

**One-sentence summary:** Ghost is the right answer for serious independent publishers who already have an audience and want to own their stack; Substack is the right answer for writers who need built-in discovery and accept the 10% fee; Beehiiv is the right answer for growth-stage newsletter operators who need referral networks and ad-monetization tooling.
