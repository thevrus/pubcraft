# Pubcraft ✍️

> **The Claude skill that operates like a senior content strategist — and replaces $400+/month of SaaS in the process.**

Pubcraft turns Claude into a senior writer + SEO strategist with current 2026 knowledge of every major publishing surface.

That includes: Google's E-E-A-T rules, LinkedIn's 360Brew algorithm, X's open-source Grok ranking, Reddit's culture-by-subreddit, YouTube's stair-step hook architecture, podcasting's now-mandatory cold-open teaser, Ghost's ActivityPub layer, Perplexity's citation patterns, Hacker News mod logic, the EU AI Act, and 16 other surfaces.

It does the research. It cites every number. It enforces a banned-words list. It explains *why* it flags each issue, naming the source: the September 2025 Quality Rater Guidelines, the March 2026 core update, AI-detection classifiers (Originality.ai, GPTZero), platform-specific community norms. It delivers production-grade Markdown reports: comparison tables, ✅/❌ audits, prioritized fix lists, schema code blocks, before/after diffs.

It tells you when a draft isn't publication-ready and exactly what a compliance officer still needs to review.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-skill-orange)](https://www.anthropic.com/claude-code)
[![Version](https://img.shields.io/badge/version-0.4.2-blue)](./CHANGELOG.md)

---

## Why this exists

Default LLM output is statistically the most-penalized content on the internet right now.

Google's March 2026 spam update sharpened SpamBrain enforcement; AI content farms lost 60–90% of organic visibility. Page #1 organic CTR drops by 34.5% when an AI Overview appears (Semrush, 10M-keyword study). Medium suspends accounts for AI-only earning. LinkedIn deboosts generic GPT prose with its own classifier. Reddit downvotes the moment "It's important to note that…" hits the page.

Yet most "AI writing" tools optimize for the wrong thing: producing text that *looks* finished. That's the trap.

Pubcraft optimizes for content that **survives the platform**, **reads as authentically human**, **gets cited by AI search**, and **doesn't get the user sued in regulated verticals**. The output is sometimes shorter than you expected, opinionated, and structurally different from the blog post you typed in.

That's intentional. That's what works in 2026.

---

## What it replaces (free vs. paid)

If you've been paying for any of these, pubcraft + Claude does the equivalent (or better) with no monthly fee. The skill is open-source and free to install on Claude Code, Claude.ai, or any Anthropic-SDK runtime.

| Paid SaaS | Monthly cost (2026) | What pubcraft does instead |
|---|---|---|
| **Surfer SEO** | $89–$249/mo | E-E-A-T-compliant article structure, SERP-mapped H2s/H3s, snippet-optimized 40–60-word answers, Core Web Vitals 2026 targets |
| **Clearscope** | $189–$1,200/mo | Topic coverage scoring via the live SERP scrape Claude runs before drafting; cited-source hierarchy enforcement |
| **Frase** | $14.99–$115/mo | SEO content briefs + draft + on-page audit, all in one pass |
| **MarketMuse** | $149–$999/mo | Topical-cluster planning + content gap analysis |
| **Copy.ai / Jasper** | $49–$249/mo | Platform-native copy that doesn't sound like Copy.ai or Jasper. 16+ surfaces with platform-specific algorithm rules |
| **Originality.ai / GPTZero** | $14.95–$179/mo | Built-in style-classifier audit (banned words, em-dash density, "Not X, but Y," burstiness) — and explains *why* each flag fires, citing the underlying detection mechanism |
| **Outranking** | $79–$219/mo | SEO-graded outlines + drafts |
| **AthenaHQ / Profound (GEO monitoring)** | $99–$499/mo | GEO citation strategy (citation-magnet patterns, brand-mention engineering, AI-search market share guidance for ChatGPT/Gemini/Perplexity/Claude) |
| **WriterAccess / agency content** | $500–$5,000/article | Structured drafts a human editor + credentialed reviewer can clear in minutes, not hours |

**Total stack you'd otherwise be paying for:** ~$400–$2,500/month, depending on tier and seat count.
**What pubcraft costs:** $0. (Claude usage is metered separately, but a typical full article + audit + GEO review runs cents per output.)

The point isn't that pubcraft is free. The point is that the actual *content-quality logic* in those SaaS tools is mostly knowable rules and 2026-current platform research — which is exactly what a well-engineered Claude skill encodes.

---

## What pubcraft does that "AI writers" don't

**🔬 Mandatory web research before drafting.**
Runs `web_search` and `web_fetch` against the live SERP, the actual People-Also-Ask, and primary sources (BLS, Federal Reserve, regulatory filings, peer-reviewed research). Every number in the output has a working URL. Statistics that can't be verified get deleted, not approximated.

**🎯 Platform-native, not "social copy."**
A LinkedIn post and a Reddit post share zero structural conventions. Pubcraft loads only the rules for the surface you asked for: 1,300–1,900 chars on LinkedIn, 240–270 chars on X, 200–800 words on Reddit (most subs), 21–34 seconds on TikTok, 80-char title on Hacker News, full five-piece launch package on Product Hunt.

**🚫 An anti-slop style guide that actually bites.**
Hard-banned words: *delve, tapestry, pivotal, leverage, robust, multifaceted, cutting-edge, ever-evolving, navigate (metaphorical), unlock,* and 30+ others. Hard-banned structures: "It's not just X — it's Y." Em-dashes capped at one per 500 words. Mandatory falsifiable specifics: at least two real names, places, dates, or numbers per 500 words. Self-audit runs before delivery.

**⚖️ YMYL and regulated-vertical compliance, surfaced automatically.**
Ask for a mortgage article and pubcraft surfaces TILA, Reg Z, RESPA, ECOA, Fair Housing, SAFE Act/NMLS, inserts `[COMPLIANCE TBD]` placeholders for vertical disclaimers, and tells you a human compliance officer needs to review before publishing. Same for medical (FDA/FTC), legal (state bar), investment (SEC/FINRA), insurance (state DOI), cannabis, gambling.

**🤖 Built for AI search citation, not just clicks.**
Dedicated GEO (Generative Engine Optimization) reference covers what gets cited by ChatGPT (~64.5% of AI search), Gemini (~21.5%), Perplexity, Claude, and Google AI Overviews. ChatGPT referrals convert at ~14.2% versus ~2.8% from organic. Being cited matters more per visit than ranking. Includes the empirical pattern that brands are ~6.5× more cited via third-party mentions than their own domain.

**📜 2026-current AI disclosure rules.**
TikTok C2PA. YouTube synthetic-content toggle. Meta auto-labeling. EU AI Act (effective Aug 2, 2026, fines up to €15M or 3% global turnover). Pubcraft knows which apply per surface and per audience.

**📦 Progressive-disclosure architecture.**
The skill is split across 21 reference files and loaded on demand. Per-task context is ~400 lines, not 1,300. Faster, cheaper, more focused.

---

## See it in action

A real LinkedIn post, generic-AI vs pubcraft:

### ❌ Generic AI

> Excited to share some thoughts on the evolving landscape of B2B marketing in 2026. In today's fast-paced world, it's more crucial than ever to leverage data-driven insights and craft compelling narratives that resonate with your target audience.
>
> Through my work with several pivotal clients, I've come to believe that authentic engagement is the cornerstone of sustainable growth. By harnessing the power of personalization and embracing a multifaceted approach, brands can navigate the complexities of today's marketplace and unlock unprecedented opportunities.
>
> What are your thoughts? Drop a comment below! 👇

LinkedIn's 360Brew classifier deboosts this on sight. Tier-1 banned words (leverage, harness, navigate, unlock, multifaceted, pivotal, evolving). Tricolons. Zero specifics. Engagement bait.

### ✅ Pubcraft

> A founder DM'd me Tuesday with the same problem I've now seen 11 times this quarter:
>
> They're spending $14K/month on paid LinkedIn, getting solid CTR (1.8%), and closing zero deals.
>
> Their dashboard says the campaign works. Their bank account says it doesn't.
>
> Here's what's actually happening in 2026, and why it's getting worse:
>
> LinkedIn's targeting got materially better in late 2024. The 360Brew model knows who your ICP is. The clicks you're paying for are real ICP humans.
>
> The problem isn't reach. It's that those same humans are seeing 40+ B2B ads a week and the bar for "this is worth a 30-min call" has moved.
>
> What's working for the three clients I have at >$80K MRR right now:
>
> – Cutting paid spend by 60–70%.
> – Reallocating to one well-researched comparison post per week.
> – Pinning that post for two weeks while reps share it 1:1 with named prospects.
>
> One client went from 4 demos/month at $11K spend to 23 demos/month at $3K spend over Q1. Same ICP. Different shape.
>
> Curious if anyone running paid LI right now is seeing the inverse — meaning, paid is still pulling weight without an organic substance layer underneath. If so, what's working?

Specific scenario in the first 210 chars (the "see more" cutoff). Real numbers. Takes a position. Genuine question, not engagement bait. Zero Tier-1 banned words. Em-dash count: 0.

Same brief. Different planet.

More worked examples in [`skills/pubcraft/examples/`](./skills/pubcraft/examples/) for X, Reddit, and Product Hunt.

---

## Coverage

| Surface | What pubcraft knows |
|---|---|
| **SEO articles** | 2024–2026 spam policies, Sept 2025 Quality Rater Guidelines, E-E-A-T, schema (Article in, HowTo out, FAQ-from-PAA, Dataset for first-party data), Core Web Vitals 2026 targets, on-page metadata (title 50–60 chars, meta 120–158 chars, H1↔title alignment), length-scaled internal linking, URL/IA placement (`/research/`, `/[hub]/`, `/blog/`), original-data report format with methodology + Limits |
| **GEO / AEO / LLMO** | Citation-magnet patterns for ChatGPT, Perplexity, AI Overviews, Claude, Gemini; technical floor (server rendering, schema, robots.txt for AI crawlers); brand-mention strategy |
| **LinkedIn** | 360Brew algorithm, dwell-time priority, link penalties, document carousels, named-scenario teardowns |
| **X (Twitter)** | Open-source Grok ranking weights (reply ≈ 27× like, conversation ≈ 150× like), Premium boost economics, long-form vs. thread tradeoffs, Grok sentiment layer |
| **Reddit** | Subreddit decision tree, specificity test for titles, comment-led marketing, branded-subreddit play, ban-bait moves |
| **Product Hunt** | Curated featuring criteria, full five-piece launch package (tagline, description, gallery, first comment, response templates) |
| **Newsletters (Substack / Beehiiv / Ghost)** | Distribution mechanics across all three; Notes/Boosts/ActivityPub; post-MPP open-rate honesty; Ghost 6.0's social web layer; when each platform wins |
| **Medium** | Boost as the only meaningful distribution lever, AI-only-earning ban policy, what's surviving in 2026 |
| **Hacker News** | Front-page score formula, second-chance pool, Show/Ask/Launch HN conventions, comment craft |
| **YouTube long-form** | Five-system algorithm (Browse, Suggested, Search, Subs, Shorts), satisfaction signals, A/B testing reality, MrBeast stair-step + Veritasium open-loop + tutorial three-act structures, thumbnail/title craft, mandatory AI disclosure (May 21, 2025), inauthentic-content rule (July 15, 2025), RPM by category |
| **Podcasts** | Solo and interview architecture, mandatory cold-open teaser, full-essay show notes for SEO, Apple auto-transcripts, the 2026 video-podcast reality (YouTube #1), monetization beyond CPM, NotebookLM disclosure norms |
| **Short-video (TikTok / Reels / Shorts)** | Length sweet spots, 3-second hook templates, Hook→Problem→Solution→CTA architecture, mandatory C2PA AI disclosure |
| **Threads / Bluesky / Mastodon** | Now-tab discovery, custom feeds, Starter Packs, Mastodon cultural rules (alt-text, CWs, CamelCase hashtags) |
| **Quora** | State of the platform in 2026, where it still pays off, where it doesn't |
| **Indie Hackers** | The canonical "I built X in N months and it makes $Y" milestone format |
| **Dev.to / Hashnode** | Canonical-URL strategy, code-block ratios, why hallucinated APIs are unforgivable |
| **Compliance** | Financial, investment, medical, legal, insurance, cannabis/gambling/alcohol, plus EU AI Act (Aug 2, 2026); escalation callouts for urgent-variant resources across health/financial/legal/investment |

---

## Install

Pubcraft is a standard Claude Agent Skill. It works in every surface that supports custom skills.

### Claude Code (CLI / IDE extensions)

**Plugin marketplace (recommended):**

```bash
/plugin marketplace add thevrus/pubcraft
/plugin install pubcraft@pubcraft
```

**Direct copy:**

```bash
git clone https://github.com/thevrus/pubcraft.git
cp -r pubcraft/skills/pubcraft ~/.claude/skills/   # personal (all projects)
cp -r pubcraft/skills/pubcraft .claude/skills/     # project-only
```

The VSCode and JetBrains Claude Code extensions read from the same `~/.claude/skills/` directory, so a single install covers all of them.

**Skill managers** like [Chops](https://chops.md/) auto-discover skills dropped into `~/.claude/skills/`.

### Claude.ai (web) and Claude desktop apps

Custom skills are available on **Pro, Max, Team, and Enterprise** plans (not the free tier). The Mac and Windows desktop apps share the web client's skill registry, so a single upload covers both.

**Steps:**

1. Download this repo as a ZIP, or clone it and zip the `skills/pubcraft/` folder.
2. Open Claude on web or desktop and go to **Settings → Capabilities → Skills** (Anthropic occasionally renames this section; if you do not see it, check the "/" command menu for `Skills`).
3. Click **Upload skill** and select the `pubcraft` folder (or the ZIP).
4. The skill activates automatically when you ask Claude for any kind of public-facing content. No prefix, no slash command needed.

**Org-managed install (Team/Enterprise admins):** upload via the workspace-level skills panel and the skill becomes available to every member without per-user setup.

### API / Anthropic SDK (Claude Agent SDK)

If you are building your own agent on the [Claude Agent SDK](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills/skills-quickstart), point the SDK's skill loader at `skills/pubcraft/`. Pubcraft is a plain skill folder (`SKILL.md` plus `references/` and `examples/`), so any compliant runtime picks it up.

### Verify it works

Ask Claude: *"Write a 200-word LinkedIn post about a marketing experiment that flopped."*

If pubcraft is loaded, Claude will ask one or two clarifying questions (audience, vertical) and refuse to write "Excited to share…" If you get a generic response, the skill is not loaded; double-check the install path or upload step.

---

## Use

Ask Claude like any writer. Pubcraft activates automatically and routes to the right platform rules.

```
Write a 1,500-word guide on negotiating medical bills, targeting "negotiate medical bill".
```

```
Draft a Reddit post for r/Entrepreneur about a $40K marketing experiment that failed.
```

```
Write a 30-second TikTok script: "I tested 5 SEO tools — here's the one that actually moved rankings."
```

```
Draft an Indie Hackers milestone post: from $0 to $4K MRR in 3 months.
```

```
Show HN submission for an open-source SQLite explainer I built. Title only.
```

```
Optimize this article for AI search — I want to be cited in Perplexity and AI Overviews.
```

---

## Architecture

```
skills/pubcraft/
├── SKILL.md                    # universal context (~245 lines, always loaded)
├── SOURCES.md                  # bibliography for every claim — used to cite mechanisms
├── references/                 # 21 platform/topic files, loaded on demand
│   ├── style-guide.md          # anti-AI-slop rules + "Why these rules exist" — load-always
│   ├── output-formatting.md    # Markdown templates, ASCII charts, Mermaid — load-always
│   ├── seo-article.md          # article structure + production checklist
│   ├── geo.md                  # AI-search citation strategy
│   ├── compliance.md           # regulated-vertical handling
│   ├── youtube-long-form.md    # full upload package (script, thumbnail, title, description)
│   ├── podcast.md              # solo + interview, show notes, monetization
│   ├── newsletters.md          # Substack / Beehiiv / Ghost
│   └── …                       # one file per remaining platform
└── examples/                   # worked ❌/✅ samples per major platform
    ├── linkedin-example.md
    ├── x-example.md
    ├── reddit-example.md
    └── product-hunt-example.md
```

A typical task loads `SKILL.md + style-guide.md + output-formatting.md + one platform reference`, about 400 lines of context. The skill stays focused; Claude stays fast. `SOURCES.md` is loaded only when Claude needs to cite a specific source while teaching the why behind a flag.

---

## What pubcraft does NOT do

- **Generate "publication-ready" content for regulated verticals.** Legal, financial, and medical drafts always end with `[COMPLIANCE TBD]` placeholders and an explicit recommendation to route through a human compliance officer.
- **Write internal docs, README files, or code comments.** Different rules apply.
- **Post for you.** Pubcraft drafts. You ship.
- **Promise rankings or featuring.** No skill can. Algorithms move; human judgment intervenes; the work compounds over months.
- **Run launch operations** (hunter outreach, waitlist mobilization, scheduling). That's a separate problem.

---

## Still on you

- Human compliance review for regulated verticals.
- Quarterly reverification. Platform algorithms shift: LinkedIn changes quarterly, X's open-source algorithm refreshes monthly, Google ships 2–4 core updates a year.
- A real credentialed reviewer byline on YMYL articles.
- The first 60 minutes of engagement on Reddit, X, and LinkedIn after publishing. Pubcraft writes the post; you have to be online.

---

## Contributing

Issues and PRs welcome. Voice is intentionally opinionated; generic-ifying PRs will be declined.

If you spot algorithm or platform changes that contradict what's in the skill, open an issue with a primary source. The whole point is that the rules are current.

## License

MIT. See [LICENSE](./LICENSE).

---

**Version:** 0.4.2 · **Last research date:** May 2026 · **Author:** thevrus
