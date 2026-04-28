# Pubcraft

> A Claude skill that writes articles, LinkedIn posts, X (Twitter) posts, Reddit posts, and Product Hunt launch copy that don't read like AI, rank in Google, and survive YMYL scrutiny.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-skill-orange)](https://www.anthropic.com/claude-code)

Most AI content gets de-indexed under Google's scaled-content-abuse policy not because Google detects "AI" but because the prose is generic, unsourced, and patternable. The same content gets buried on LinkedIn, X, and Reddit because each platform's 2026 algorithm has its own classifier, its own format conventions, and its own bullshit detector. Pubcraft is an opinionated Claude Code skill that fixes the underlying causes: it forces real web research before drafting, enforces a strict source-quality hierarchy, surfaces YMYL compliance requirements automatically, applies a banned-words-and-patterns filter that strips the structural fingerprints of LLM prose (the em-dashes, the "not just X, it's Y" constructions, the tricolons, the "delve") — and routes to platform-specific rules for each output channel.

It is the skill I wanted when I started writing for a regulated vertical and realized none of the existing humanizer tools also handled E-E-A-T, citation discipline, schema markup, regulatory disclaimers, *and* the algorithm-specific quirks of every platform I was distributing to.

---

## What it does

When you invoke Pubcraft, Claude:

1. **Clarifies the brief** — audience, target query, length, vertical, regulatory exposure.
2. **Researches the live web** — runs the target query, scrapes the SERP, captures People-Also-Ask, identifies top-10 patterns, pulls primary sources.
3. **Builds a source list before drafting** — minimum 4–6 Tier-1/Tier-2 sources for any YMYL piece.
4. **Plans the structure** based on actual SERP data, not assumptions.
5. **Drafts** following an enforced style guide (banned words, banned structural patterns, sentence-length variance, lived-experience detail).
6. **Self-audits** against a 5-point anti-slop checklist and a 30-item production checklist.
7. **Surfaces compliance requirements** for regulated verticals (financial, medical, legal, insurance, cannabis) with template disclaimer blocks and explicit "[COMPLIANCE TBD] — human review required" flags.
8. **Cites everything** with working URLs in a References section.

What you get back is not "publication-ready" — that's the whole point. You get a researched, structured, sourced, compliance-flagged draft that a human editor or compliance officer can clear in minutes rather than hours.

## What it doesn't do

- It does not pretend to replace a credentialed expert, a compliance officer, or an editor.
- It does not run AI-detection tools for you. (They produce false positives on careful human writing and false negatives on lightly edited AI text. Use them as sanity checks, not gates.)
- It does not generate fiction, internal docs, code comments, or transactional emails. Use the right tool for the right job.

---

## Install

### Option 1 — Plugin marketplace (recommended)

```bash
# Inside Claude Code
/plugin marketplace add thevrus/pubcraft
/plugin install pubcraft@pubcraft
```

### Option 2 — Direct copy (no marketplace)

```bash
# Personal (all your projects)
git clone https://github.com/thevrus/pubcraft.git
cp -r pubcraft/skills/pubcraft ~/.claude/skills/

# Project-only (one repo)
git clone https://github.com/thevrus/pubcraft.git
cp -r pubcraft/skills/pubcraft .claude/skills/
```

### Option 3 — Claude.ai web/desktop (Pro, Max, Team, Enterprise)

Upload the `skills/pubcraft/` folder via the Claude UI's custom skills panel.

---

## Use

Just ask Claude what you'd ask any writer:

```
Write a 1,500-word guide on how to negotiate medical bills, targeting "negotiate medical bill" search queries.
```

```
Write a LinkedIn post about why most B2B founders are getting Reddit wrong in 2026.
```

```
Draft an X long-form post (under 2,000 chars) on the open-sourced X algorithm and what it means for small accounts.
```

```
Write a Reddit post for r/Entrepreneur about a $40K marketing experiment that failed, with the lessons.
```

```
Draft the Product Hunt launch package — tagline, description, gallery captions, first comment — for [your product].
```

Pubcraft activates automatically based on its description and routes to the right platform-specific rules. You can also invoke it explicitly:

```
Use the pubcraft skill to draft an X thread about the 2026 LinkedIn algorithm changes for B2B founders.
```

---

## Why this exists

Three things shifted in early 2026 that made existing AI-writing approaches obsolete:

- **Google's March 2026 spam update** sharpened SpamBrain enforcement of scaled-content-abuse. Sites publishing AI content at scale without human review lost visibility on programmatic pages overnight.
- **The September 2025 Search Quality Rater Guidelines** explicitly rate AI content as "Lowest Quality" when it's mass-produced without human review or offers no original information beyond rephrasing existing sources.
- **Every major social algorithm now runs its own AI classifier.** LinkedIn's March 2026 Authenticity Update, X's Grok-powered ranking (open-sourced January 2026), and Reddit's September 2025 algorithm shift all dropped reach 50%+ for posts matching generic LLM patterns.

The bar moved. Pubcraft is calibrated to the new bar.

## Coverage

**Articles & SEO:**
- Google's March 2024, August 2025, and March 2026 spam policies.
- Quality Rater Guidelines (September 11, 2025 edition, the latest publicly available).
- E-E-A-T pillars with emphasis on Trust as the dominant signal for YMYL.
- Schema markup post-2025 reality (Article in, HowTo out, FAQ caveats).
- Core Web Vitals 2026 targets (LCP < 2.5s, INP < 200ms, CLS < 0.1).

**Social platforms:**
- **LinkedIn** — 360Brew interest-graph algorithm, dwell-time priority, link penalties, document carousel format, 1,300–1,900 char sweet spot.
- **X (Twitter)** — Open-source Grok ranking weights (reply ≈ 27x like, conversation ≈ 150x like), Premium boost economics, long-form vs. thread tradeoffs, sentiment penalties.
- **Reddit** — Engagement velocity, subreddit-fit specificity test, comment-led marketing strategy, the branded-subreddit play, AI-search citation dynamics, and the do-not-do list that keeps your account un-banned.
- **Product Hunt** — Post-2024 curated featuring (10% rate, judged on usefulness/novelty/craft/creativity), full launch copy package (tagline / description / gallery / first comment / response templates), points-not-upvotes ranking.

**Compliance:**
- Regulated verticals: financial/mortgage (TILA, RESPA, ECOA, NMLS, state mortgage statutes), investment (SEC, FINRA), medical (FDA, FTC health claims), legal (state bar advertising), insurance (state DOI), cannabis/gambling/alcohol.

## What you should still do yourself

- **Human compliance review** for regulated verticals. The skill flags `[COMPLIANCE TBD]` placeholders explicitly. Do not ship past those without a qualified human signing off.
- **Reverify quarterly.** Search and platform policy moves fast. The skill's research date is stamped at the top.
- **Add a credentialed reviewer byline** to YMYL articles. The skill cannot manufacture credentials.

---

## Contributing

Issues and PRs welcome. The skill is one file (`skills/pubcraft/SKILL.md`) — easy to read, easy to edit. If you find a banned-word pattern that's slipped through, a regulatory framework that should be added, or a structural anti-pattern that needs flagging, open an issue.

Voice and structure of the skill are intentionally opinionated. Generic-ifying PRs will be declined.

## License

MIT. See [LICENSE](./LICENSE).

## Acknowledgments

Inspiration drawn from the broader anti-AI-slop community — `blader/humanizer`, `lguz/humanize-writing-skill`, `SHADOWPR0/beautiful_prose` — and from Google's published Quality Rater Guidelines, which remain the most underread document in SEO.

---

**Version:** 0.2.0 · **Last research date:** April 2026 · **Author:** thevrus
