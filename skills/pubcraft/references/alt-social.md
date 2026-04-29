# Threads / Bluesky / Mastodon (alt-social)

Load this reference when drafting for Threads, Bluesky, or Mastodon.

## Threads

- **Algorithm:** centralized, AI-personalized "For You" via Meta's "Dear Algo" layer. Heavy weight on follower-graph from Instagram, predicted engagement, and (now in 2026) reply quality. Vertical native video gets boosted.
- **Scale:** ~400M MAU by Sep 2025, outpacing X's mobile DAU. Daily reach is real but reach-per-post is volatile.
- **Fediverse integration:** still partial as of 2026. Threads can publish out to ActivityPub but accepts only limited inbound interactions.
- **Format:** 500-char limit. Posts that get reach: 1 strong opening sentence (provocative or contrarian), vertical video, thread-of-replies-to-self for context. Hashtags exist but are weak signals.
- **Works:** quick takes on tech/news, replying to large accounts (Threads heavily surfaces good replies in others' feeds — the "Now" tab and reply-discovery are real growth levers), trending-topic posts within minutes of news.
- **Fails:** corporate brand voice, link-led posts (links are deboosted), recycled X content (engagement is meaningfully lower).
- **AI content:** Meta auto-labels AI-detected content via C2PA. Cultural tolerance is moderate.

## Bluesky

- **Architecture:** AT Protocol; no single algorithm. Distribution is via **Following feed** (chronological, reverse-chrono), **Discover feed** (light algorithmic), **custom feeds** (user-created, e.g. Filmsky, Science — your hashtags and keywords determine which feeds you appear in), and **Starter Packs** (curated bundles of accounts new users mass-follow with one click; inclusion in a strong Starter Pack is the single fastest growth lever).
- **Scale:** ~6M active users (Q1 2026), small but engaged. Engagement rate ~4.2% is **2.8× higher** than X's (per Athenic 2025 study).
- **Format:** 300-char limit per post; threads work well; markdown-style links with previews work; 4-image grid supported. Hashtags work (added Feb 2024).
- **Works:** technical posts, science writing, journalist commentary, leftist-political and arts communities.
- **Fails:** crypto, "build in public" hustle-coded SaaS marketing, growth-hacker tone, unlabeled AI art. **Bluesky has explicitly stated it will not allow user content to train AI**, and the community is *strongly* anti-AI; AI prose and AI art draw immediate replies and blocks.
- **Banned moves:** mass-following Starter Packs and immediately unfollowing (gets you on shared block-lists), engagement bait, posting NSFW without proper labeling.
- **Compliance:** crypto promotion is community-suicide; financial newsletters work with full "not advice" framing; medical claims face the same scrutiny as elsewhere.

## Mastodon

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

## Hooks across all three

- **Threads:** "[Specific contrarian claim]. Reasons in reply." (drives Now-tab visibility)
- **Bluesky:** "[Specific niche observation that an expert would notice]." (rewarded by custom feeds)
- **Mastodon:** First an `#introduction` post; then content like "I've been working on [project] for 18 months. Here's what I learned about [specific technical detail]. (1/n) #DevToot #OpenSource"

## AI-tells / community-specific peeves

- **Threads:** Meta-wide AI tells; users mock GPT-default tone.
- **Bluesky:** anti-AI community blocks accounts emitting *"In today's,"* *"Let's explore,"* or three-clause GPT structure; AI emoji clusters (🚀💡✨) are an instant tell.
- **Mastodon:** any post that reads like marketing draws silent unfollows. Cultural test: "would this same content appear on LinkedIn?" If yes, rewrite.

## Verdict

- **Threads:** worth posting if you already cross-post from Instagram; not worth a dedicated strategy.
- **Bluesky:** worth real investment for tech, science, journalism, B2B SaaS targeting developers; engagement quality significantly higher than X.
- **Mastodon:** worth investment for open-source maintainers, academics, technologists targeting indie/privacy-conscious audiences. *Not* worth investment for brand marketing — culture rejects it and the math doesn't justify.
