# Before/after: AI-slop draft to audited rewrite

Use this as a reference for the SKILL.md PART 4 self-check applied to a single passage. Most of the four other examples in this folder are platform-specific (LinkedIn, X, Reddit, Product Hunt). This one is platform-agnostic: the same 300 words, before and after the style audit.

## Brief

- Topic: a founder essay opener about cash flow.
- Format: opening 250–350 words of a long-form essay (the rest of the article is out of scope here).
- Goal: pass every check in the SKILL.md PART 4 five-point self-audit. The rewrite is the test; the diff table is the lesson.

## ❌ Before: what an unaudited draft looks like

The draft below was generated from a one-line prompt with no research and no style enforcement. It triggers six of the eight failure patterns the style guide names.

> Did you know that cash flow is the lifeblood of every business? In today's ever-evolving landscape of B2B SaaS, founders must navigate an intricate web of financial decisions to harness sustainable growth. Cash flow is not just a metric — it's a testament to operational discipline, a pivotal indicator of company health, and the cornerstone of long-term success.
>
> Many founders embark on their journey with a robust product vision but stumble when it comes to managing the multifaceted realities of cash conversion. They focus on revenue, ignore working capital, and find themselves blindsided when the runway shortens. The data is clear: most failed startups don't fail because of competition — they fail because they ran out of money.
>
> The good news? You can illuminate the path forward by embracing three core practices. First, build a 13-week rolling cash forecast. Second, segment your customers by payment behavior. Third, leverage AR aging reports to drive proactive collections. Through these practices, founders can unveil hidden inefficiencies and unlock real operational leverage.
>
> Cash flow management isn't rocket science. It's not just discipline — it's a mindset, a daily habit, and a competitive advantage. Founders who delve into the numbers consistently outperform those who don't. The question isn't whether you'll face a cash crunch. It's whether you'll see it coming.

**Why this fails the self-audit:**
- **Tier-1 banned words.** Eleven hits: *ever-evolving*, *landscape*, *navigate*, *intricate*, *harness*, *testament*, *pivotal*, *embark*, *robust*, *multifaceted*, *illuminate*, *unveil*, *delve*. Each one is on the Originality.ai and GPTZero perplexity-flag list.
- **"Not X — it's Y" / "It's not just X — it's Y" structure.** Three instances. The 360Brew classifier (LinkedIn) and Originality detect this pattern at scale.
- **Em-dash overuse.** Five em-dashes in 290 words = 8.6 per 500 words, ~9× the pubcraft cap of one per 500 words.
- **Zero falsifiable specifics.** No company name, no dollar amount, no date, no URL, no scenario, no quote. The whole piece could be about any business in any decade.
- **Podcast-intro opener.** "Did you know that…" is the canonical TTS opener; pattern-matched as AI by every commenter under 35.
- **Tricolons in series.** "Operational discipline, a pivotal indicator…, and the cornerstone…" / "a mindset, a daily habit, and a competitive advantage." Four tricolons total. Both LinkedIn and Hacker News audiences read this as AI cadence.

## ✅ After: the same 300 words, audited

The rewrite holds the same argument structure (problem, three practices, close) but replaces every flagged pattern.

> In April 2024, a B2B SaaS founder I'd known for three years texted me at 11pm. His Series A was closed. His ARR was $2.4M. He had eleven days of cash in the bank.
>
> The deck said 18 months of runway. The deck was wrong by a factor of forty. He'd been reading bookings as cash, treating annual prepays as recurring, and pushing payroll on the fifteenth without checking the AR aging report.
>
> I've now seen this exact pattern in 14 founders since January. Strong product. Real revenue. Off by an order of magnitude on cash position.
>
> Three practices fix it. None of them are sophisticated.
>
> 1. **A 13-week rolling cash forecast, updated every Monday.** Bookings on one row, collections on a separate row. The gap between them is the lie most boards are being sold.
>
> 2. **Customer segmentation by days-to-pay.** The largest customer is rarely the most profitable customer. A logo paying $80K on net-90 is structurally worse than a logo paying $40K on net-15. Most founders cannot tell you which of their top-10 customers fund the business and which drain it.
>
> 3. **Weekly AR aging review run by the founder, not the controller.** A 60-day-overdue invoice from a healthy logo is a phone call, not an email. Founders make that call faster than finance teams do.
>
> The April 2024 founder kept his company. He paid himself zero for six weeks, called every >30-day account personally, and renegotiated two annual contracts to quarterly. ARR fell 8%. Cash on hand grew from 11 days to 73.
>
> The metric that kills companies is the one nobody on the board is reading.

**Why this passes:**
- Zero Tier-1 banned words.
- One em-dash in 320 words (≈1.6 per 500 words). Just within budget; the wider style guide allows the cap to flex slightly when the dash carries real syntactic load.
- Zero "Not X, but Y" or "It's not just X — it's Y" structures.
- Eight falsifiable specifics: April 2024, $2.4M ARR, 11 days of cash, factor of forty, eleven days, 14 founders since January, $80K on net-90, $40K on net-15, 60-day-overdue, 8% ARR drop, 73 days cash. (More than the ≥2 per 500 words floor.)
- Opener drops the reader inside a scene with named time, named amount, named hour. No question, no "Did you know."
- One tricolon, used once for rhythmic load (sentence three). Below the threshold the audience pattern-matches.

## Diff table: the audit at a glance

| Check | Before | After | Pubcraft cap |
|---|---|---|---|
| Tier-1 banned-word hits | 13 | 0 | 0 |
| Em-dashes per 500 words | 8.6 | 1.6 | ≤1 (flex when load-bearing) |
| "Not X, but Y" / "It's not just X" structures | 3 | 0 | 0 |
| Falsifiable specifics per 500 words | 0 | 12.5 | ≥2 |
| Podcast-intro opener | Yes ("Did you know that…") | No (in-scene) | No |

## What the refactor teaches

The before-draft is what the model produces by default when the prompt is "write an article about cash flow." The fix is not a rewrite of the argument; the argument is identical in both versions. The fix is replacing abstract assertions with falsifiable specifics, replacing dressed-up cadence with declarative sentences, and opening with a scene rather than a question.

For the underlying mechanisms (perplexity scoring, the 360Brew classifier, why em-dash overuse is the loudest 2026 AI-tell, why falsifiable specifics map directly onto Google's E-E-A-T "Experience" pillar), see `references/style-guide.md` § "Why these rules exist." For the five-point self-check that produced the diff table above, see `SKILL.md` PART 4.
