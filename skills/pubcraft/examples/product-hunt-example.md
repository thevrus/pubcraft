# Product Hunt — worked sample (full launch package)

Hypothetical product: **Slate** — a Slack/Teams app that captures decisions made in chat threads and surfaces them when a teammate later asks "wait, what did we decide?"

## ❌ Generic AI draft (what NOT to ship)

**Tagline:** "Revolutionize team collaboration with AI-powered decision intelligence."

**Description:** "Slate is a cutting-edge AI platform that transforms how distributed teams capture, surface, and leverage critical decisions. Unlock unprecedented productivity with our seamless Slack and Teams integration."

**Why this fails:** Every Product Hunt curator has read 200 versions of this paragraph. Tier-1 banned words across the board. Zero falsifiable claim. "Revolutionize," "AI-powered," "cutting-edge" — auto-buried.

## ✅ Revised launch package

### 1. Tagline (under 60 chars)

> Capture team decisions in Slack — find them later

(50 chars. Plain language. Specific outcome: capture + find. No "AI-powered" or "revolutionary.")

### 2. Description (under 260 chars)

> Your team makes 12 decisions a week in Slack threads and remembers maybe 3. Slate watches your channels, flags decisions as they happen, and gives you one searchable feed. No more "wait, what did we decide?"

(245 chars. Leads with the problem with a specific number. Names the exact phrase the product solves. Two short sentences max.)

### 3. Gallery captions (5 images / GIFs)

1. **GIF — 6 seconds.** "Slate auto-detects a decision in a Slack thread."
2. **Screenshot.** "Decisions feed for the #design channel — 47 decisions over the last 30 days, searchable."
3. **GIF — 8 seconds.** "Asking @slate 'what did we decide about pricing?' in any channel returns the thread + decision summary."
4. **Screenshot.** "The weekly digest: every decision, who made it, what changed."
5. **Screenshot.** "Settings: choose which channels Slate watches. Private channels, never. Direct messages, never."

(Each caption is a factual sentence describing the image. No hype. Last caption preempts a privacy concern — privacy is the #1 question in PH comments for any Slack-watching tool.)

### 4. First comment (the founder story)

> Hey Product Hunt 👋
>
> I'm [founder name]. We built Slate because at our last company we ran weekly retros where someone would ask "didn't we decide to deprecate that two months ago?" and three of us would scroll Slack for 20 minutes trying to find the thread.
>
> We tried Notion docs, decision logs, "captain's log" channels. None of it survived contact with normal team behavior. People decide things in flight; they don't pause to document them.
>
> So Slate works in the opposite direction: it watches the channels you tell it to (never DMs, never private channels you don't add it to), uses a small model to flag decisions, and asks one Slack-button question — "Was this a decision?" — to confirm. The model gets better; you stay in control.
>
> What I'd genuinely value feedback on:
>
> 1. Is the in-channel "Was this a decision?" prompt annoying or useful? We've gone back and forth.
> 2. Pricing: $79/mo flat for under-15 seats, $249 for 15+ seats. Are we under-pricing the larger plan?
> 3. The thing we haven't built yet: a CLI/API to pull decisions into project tracker tools. Worth prioritizing or scope creep?
>
> If you try it and something feels off, tell me here — I'm responding to every comment today. Thanks for taking a look.

(348 words. Specific lived-experience scenario. No press-release voice. Three concrete questions you actually want feedback on, not "tell us what you think." Privacy reassurance is in line 4 — pre-empts the comment that always comes.)

### 5. Comment-response templates

**"How is this different from [Decisions Bot / Asana / Linear / Notion AI]?"**
> Decisions Bot is closest. The difference is detection — we don't require anyone to type `/decision` to log it. We watch and flag, you confirm. In my experience the ones that need a slash command get used week 1 and forgotten by week 4.

**"Is there a free tier?"**
> 14-day free trial, no card. After that it's $79 for under-15 seats, $249 for 15+. We considered freemium and decided against it because the value compounds with team-wide adoption — a 1-person plan is a lot worse than a whole-team plan.

**"What about privacy / does it train on our data?"**
> No training on your data, full stop. We use a hosted small model with zero retention. You pick the channels Slate watches; it never reads DMs or any channel you don't add it to. SOC 2 Type 1 in progress.

**"Feature request: Microsoft Teams support."**
> Teams support is on the roadmap — beta is Q3 2026 if we hit our cohort milestones. If you'd be willing to be a design partner I'd love to talk. DM me.

**"This is just a glorified search tool."**
> Partial truth. It's also a passive capture layer — the search tool only works if you've logged the decision somewhere first. The capture is what nobody else does without imposing a workflow on the team.

**"I tried it and [bug]."**
> Sorry — that's a known issue with [specific cause]. Fix is in [today's / next week's] release. I'll DM you when it ships and refund the trial day.

### Tagging

- **Productivity** is the broad category — too broad. Pick **AI Coding Assistants → No.** Pick **Slack → yes.** Pick **Knowledge Management → yes.** Pick **Productivity → yes** (one broad slot).

Three categories, most-specific-first.

### Timing

- **Launch:** Tuesday, 12:01 AM PT.
- **Avoid:** the week of WWDC, the week of YC Demo Day, the week before Christmas.

### What this package does *not* do

- **No "we're so excited" language.**
- **No fundraising humblebrag** in the first comment.
- **No promise of a featuring outcome** — featuring is curator judgment on usefulness, novelty, craft, creativity. The package optimizes for those four; it can't guarantee them.
