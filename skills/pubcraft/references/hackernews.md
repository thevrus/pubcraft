# Hacker News

Load this reference when drafting a Hacker News submission or comment.

## Algorithm and ranking (2026)

Front-page score decays roughly as `(upvotes - 1)^0.8 / (hours_since + 2)^1.8`, plus moderator interventions: flamewar penalties, software-defined "controversy" penalties, off-topic penalties, and the **second-chance pool** (`/pool`) — a moderator-curated list where deserving-but-missed submissions get random front-page placement. You can email `hn@ycombinator.com` to nominate a story. The **/invited** list lets mods invite a writer to repost.

**Karma** unlocks features at thresholds (downvote ~500). Vote rings get nuked.

Editorialized titles are **rewritten by mods** automatically. HN's stance (per pg) is that titles are common property and the article's own title is the default. "[VIDEO]", "I made", or marketing language gets reverted.

**Show HN, Ask HN, Launch HN** are official categories. Launch HN is reserved for active YC startups (announced via YC partner). Show HN requires the project to be something users can *actually try*; the URL must lead to a working demo, repo, or downloadable artifact.

## Format conventions

- **Title:** maximum 80 characters. No clickbait, no company-name brackets, no ALL CAPS, no "[2025]" unless it's in the original title.
- **Show HN body:** 2–6 short paragraphs. What it is, why you built it, what's interesting technically, what feedback you want. **Don't post a press release.**
- **Comments:** average upvoted comment is 2–6 sentences with a specific, often contrarian or experiential, claim. Long comments work *if* dense.

## What works vs. fails

- **Front-page winners (recurring patterns from 2025–2026):** technical writeups (reverse engineering, deep dives, retro-computing), policy critiques on tech regulation, interesting failure modes, "I built this thing and learned X" pieces, original research, academic papers, deep open-source releases. AI critiques and AI tools both feature heavily.
- **Buried/flagged:** "We raised $XM" without substance, generic SaaS launch posts, listicles, AI-generated SEO blog spam, marketing-coded prose, Medium URLs (lower flag bar), reposts within ~6 months. **State of Show HN 2025** consensus: the bar has risen because of AI-coded launch volume; signal/noise of submissions has degraded.

## Community norms / banned moves

- **Don't ask for upvotes** anywhere (post body, Twitter, Slack). Voting rings kill the post and flag the account.
- **Don't editorialize the title.** Use the article's own title; if no good title exists, factual descriptive only.
- **Don't reply combatively.** "Please don't be snarky" is in the official guidelines and is enforced.
- **Don't post the same URL twice within ~6 months.**
- **Show HN must be your own project.** Posting someone else's project as Show HN is a flag-out.
- **Don't downvote disagreement.** (You can; the culture polices it.)
- Tuesday–Thursday morning Pacific is the optimum window. Weekends underperform.

## Comment craft (what gets upvoted vs. downvoted)

- **Upvoted:** specific lived experience ("I worked on this exact problem at $COMPANY in 2018, here's what we found"), correcting an error in the post with citation, technical clarification, counter-example with details, dry humor, niche expertise.
- **Downvoted/flagged:** "this," "+1," "OP is missing the point" without an argument, ad-hominem, political jabs, generic LLM-tone replies, *"Have you considered just using $LIBRARY?"* without context.

## AI content

Heavily controversial through 2024–2026. Mods deboost obvious AI-generated articles. AI-generated *comments* are aggressively flagged. The community broadly tolerates AI-assisted code but is hostile to AI-written prose, especially AI-summary articles about HN itself.

## Compliance

Pump-and-dump crypto submissions get flagged immediately. Affiliate links in submissions get flagged. Financial advice from anonymous accounts gets dismissed.

## Hooks/titles that work in 2026

- "Show HN: I rewrote git in Rust to learn Rust. It's faster than I expected."
- "What fork() actually copies"
- "The 1.5M GitHub PRs that had ads injected by Copilot"
- "Closed-source AI is neofeudalism"
- "Ask HN: How do you stay productive when the model improves weekly?"

## AI-tells / banned phrases

HN comments will brutally call out: *"Great question!"*, *"That's a fascinating point,"* *"In summary,"* *"It's worth noting that,"* the *"Certainly! Here are…"* opener, bullet-point-with-bold-keyword formatting, and any comment that pattern-matches GPT default voice. Em-dashes and triple-clause "It's not X — it's Y — it's Z" structure get sniffed instantly.

## Verdict

Still the highest-quality tech audience on the internet. Viable in 2026, but the bar has risen. Treat HN as a place where you submit *one* deeply considered thing per quarter; don't farm it.
