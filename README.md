# Pubcraft ✍️

> A Claude skill for articles, newsletters (Substack/Beehiiv), Medium, Hacker News, short-video (TikTok/Reels/Shorts), and platform-native social (LinkedIn, X, Reddit, Threads, Bluesky, Mastodon, Quora, Indie Hackers, Dev.to, Hashnode, Product Hunt) that doesn't read like AI, ranks in Google, and survives YMYL scrutiny.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-skill-orange)](https://www.anthropic.com/claude-code)

Most AI content fails not because Google detects "AI" but because the prose is generic, unsourced, and patternable. Pubcraft fixes the underlying causes: real web research before drafting, strict source hierarchy, automatic YMYL compliance flags, and a banned-words filter that strips LLM fingerprints (em-dashes, tricolons, "delve") — then routes to platform-specific rules per channel.

## What it does 🛠️

1. Clarifies the brief (audience, query, length, vertical, regulatory exposure)
2. Researches the live web — SERP, PAA, top-10 patterns, primary sources
3. Builds a source list before drafting (4–6 Tier-1/Tier-2 for YMYL)
4. Drafts under an enforced style guide
5. Self-audits against anti-slop and production checklists
6. Surfaces compliance requirements with `[COMPLIANCE TBD]` flags
7. Cites everything with working URLs

You get a researched, sourced, compliance-flagged draft a human editor can clear in minutes — not "publication-ready" prose. That's the point.

## Install 📦

**Plugin marketplace (recommended):**

```bash
/plugin marketplace add thevrus/pubcraft
/plugin install pubcraft@pubcraft
```

**Direct copy:**

```bash
git clone https://github.com/thevrus/pubcraft.git
cp -r pubcraft/skills/pubcraft ~/.claude/skills/   # personal
cp -r pubcraft/skills/pubcraft .claude/skills/     # project-only
```

**Skill manager (e.g. [Chops](https://chops.md/)):** drop `skills/pubcraft/` into `~/.claude/skills/` and Chops will pick it up automatically — browse, edit, and toggle from the app.

**Claude.ai (Pro/Max/Team/Enterprise):** upload `skills/pubcraft/` via the custom skills panel.

## Use

Ask Claude like any writer:

```
Write a 1,500-word guide on negotiating medical bills, targeting "negotiate medical bill".
```

```
Draft a Reddit post for r/Entrepreneur about a $40K marketing experiment that failed.
```

```
Draft a Substack issue about why most B2B newsletters die at 200 subs.
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

Pubcraft activates automatically and routes to the right platform rules.

## Coverage 🎯

- **SEO:** Google's 2024–2026 spam policies, Sept 2025 Quality Rater Guidelines, E-E-A-T, schema, Core Web Vitals 2026 targets
- **Newsletters (Substack / Beehiiv):** Notes vs. archive distribution, Boosts/Recommendations, post-MPP open-rate norms, length sweet spots
- **Medium:** Boost-only distribution, +5% external-source bonus, AI-only-earning ban policy
- **Hacker News:** front-page score formula, second-chance pool, Show/Ask/Launch HN conventions
- **Short-video (TikTok / Reels / Shorts):** length sweet spots, 3-second hook templates, Hook→Problem→Solution→CTA architecture, mandatory C2PA AI disclosure
- **LinkedIn:** 360Brew algorithm, dwell-time priority, link penalties, format conventions
- **X:** Open-source Grok ranking weights, Premium boost, long-form vs. thread tradeoffs
- **Reddit:** Engagement velocity, subreddit-fit, comment-led marketing, branded-subreddit play
- **Threads / Bluesky / Mastodon:** Now-tab discovery, custom feeds and Starter Packs, Mastodon cultural rules (alt-text, CWs, CamelCase hashtags)
- **Quora:** State of the platform in 2026 and where it still pays off
- **Indie Hackers:** the canonical "I built X in N months and it makes $Y" milestone format
- **Dev.to / Hashnode:** canonical-URL strategy, code-block ratios, why hallucinated APIs are unforgivable
- **Product Hunt:** Curated featuring criteria, full launch copy package
- **Compliance:** Financial, investment, medical, legal, insurance, cannabis/gambling/alcohol — plus EU AI Act (Aug 2, 2026) disclosure obligations

## Still on you

- Human compliance review for regulated verticals
- Reverify quarterly — search and platform policy moves fast
- Add a credentialed reviewer byline to YMYL articles

## Contributing

Issues and PRs welcome. The skill is one file: `skills/pubcraft/SKILL.md`. Voice is intentionally opinionated — generic-ifying PRs will be declined.

## License

MIT. See [LICENSE](./LICENSE).

---

**Version:** 0.3.0 · **Last research date:** April 2026 · **Author:** thevrus
