# X (Twitter)

Load this reference when drafting a single X post, long-form Premium post, or thread.

## Algorithm reality (April 2026)

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

## Format and length

- **Single tweet:** 240–270 characters is the sweet spot for engagement. The 280 char limit invites truncation in feed previews.
- **Long-form post (Premium):** 800–2,500 characters, structured with line breaks. Punchy lead. One idea per paragraph. Specific.
- **Thread:** 4–7 tweets. First tweet must work as a standalone. Number them ("1/" or "1." in the first line, optional). Last tweet should restate the value, not include a CTA to follow.

## Hook patterns that work

- **Specific number lead:** "I closed 23 deals in Q1 using one rule: …"
- **Contrarian:** "Everyone says X. They're wrong, and here's the data."
- **Named scenario:** "A founder DM'd me Friday about [problem]. My answer:"
- **Question-as-thesis:** "Why is [counterintuitive thing] true? Three reasons:"

Avoid: "🧵 thread on…" (signals length without value), "I'll keep it short:" (don't announce structure), "Hot take:" (overused).

## Sentiment notes

Grok's sentiment layer reduces reach for posts that are dunky, negative, or attack-oriented even when they get high engagement. Constructive disagreement is fine; calling people stupid is reach-suicide in 2026.

## Engagement and timing

- **First 30–60 minutes determines distribution.** Post when your most engaged followers are online — for B2B, weekday 9–11 AM PT or 1–3 PM ET tends to work.
- **Reply to every reply** in the first 2 hours, including disagreement. Replies generate the conversation weight that's worth 150x a like.
- **Quote-tweets > retweets.** Add commentary when amplifying.

See `examples/x-example.md` for a worked sample.
