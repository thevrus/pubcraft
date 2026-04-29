# Anti-AI-slop style guide

This applies to **every** output produced by the skill — articles, social posts, scripts, captions. Load this reference at the start of any drafting task.

## Why this matters

Two distinct concerns are conflated and need separating:

1. **Algorithmic detection.** Google does not run a public binary "AI penalty." What it penalizes is *low-quality, unoriginal, ranking-motivated content* — which AI happens to produce by default. Generic AI prose loses because it lacks information gain and trust signals, not because a "delve" was detected.
2. **Reader perception.** Readers, journalists, and prospective clients *can* recognize AI slop. A YMYL brand reading as AI-generated is a trust catastrophe. Originality.ai, GPTZero, and Copyleaks use perplexity and burstiness as core signals. None are reliable enough for legal decisions, but a piece flagged by all three reads as AI to humans too.

Optimize for #2 and #1 takes care of itself.

## Banned words

These words are statistical fingerprints of LLM output. Hard-avoid:

**Tier 1 (strongest tells):** delve, tapestry, navigate (as a metaphor — fine when literal), realm, landscape (as a metaphor — fine when literal), pivotal, testament, elucidate, embark, underscore, harness, illuminate, unveil, intricate, multifaceted, robust, ecosystem (as a metaphor), cutting-edge, game-changer, ever-evolving.

**Tier 2 (moderate tells):** leverage (as a verb), seamless, comprehensive, crucial, essential (as filler), key (as filler — "a key consideration"), indeed, furthermore, moreover, additionally (in clusters), in essence, in conclusion, ultimately (as a transition), it's important to note, it's worth noting, it goes without saying, when it comes to, in today's [X] world, in the world of, in the realm of.

**Tier 3 (transition spam — fine in isolation, AI-ish in clusters):** Furthermore + Moreover + Additionally appearing within 200 words of each other.

## Banned structural patterns

**"Not just X, it's Y" construction.** "It's not just a tool — it's a movement." Hard ban. Strongest AI structural fingerprint in 2026.

**Tricolons (rule of three) in series.** "Fast, reliable, and affordable." Limit to one per article.

**Em-dash overuse.** AI loves em-dashes. **Hard limit: one em-dash per ~500 words.** Default to commas, periods, semicolons.

**Mirror Q+A rhetoric.** "But what does this mean? It means…" — sparingly, fine; as a recurring opener, a tell.

**Synonym cycling within close proximity.** AI varies word choice ("borrower… purchaser… aspiring owner…") more than humans do. If "X" is the right word, use "X" three times in a row.

**Comma-linked -ing modifiers.** "Rates rose, making affordability harder." Once or twice fine; as a tic, a fingerprint.

**Symmetrical conclusions** that summarize and end with a forward-looking platitude. Either say something new or stop.

**Bullet lists where every item is the same length and starts with the same part of speech.** Vary it or use prose.

## Pro-human signals to deliberately include

- **Sentence-length variance.** Mix 4-word sentences with 30-word sentences. Burstiness is what humans have and AI doesn't by default.
- **Specific, falsifiable detail.** "Last Tuesday in Pinellas County" beats "recently in Florida." Real names, real places, real dates, real numbers.
- **Opinions and stance.** Take a position. AI hedges; humans commit.
- **First-person and second-person voice.** "I had a client last month who…"; "Your DTI is the deciding factor here."
- **Mild imperfection.** A trailing thought, a parenthetical aside, a "look —" or "honestly."
- **Pop-culture, regional, timely references.** AI cannot generate these convincingly without prompting.
- **Concrete examples over abstractions.** Always.
- **"I don't know"** when relevant. AI never says this; humans do.

## Self-check before delivering

Run every draft through this five-point audit:

1. Did I use any Tier 1 banned word? (Find/replace.)
2. More than two em-dashes total? (Replace most.)
3. Any "Not X, but Y" structure? (Rewrite.)
4. At least two pieces of falsifiable detail per 500 words?
5. Any sentence sound like podcast intro voice? (Cut it.)

---

## Why these rules exist (use this when reviewing or explaining a flag)

When the skill flags a draft, **explain the mechanism**, not just the verdict. Readers and writers learn from "this triggers X classifier" — they tune out from "this is bad." The references below are what to cite when a user asks "why is this flagged?"

### Why Tier 1 banned words matter

LLMs over-produce specific words because their training data is biased toward well-edited prose (Wikipedia, news, academic), where words like *delve*, *robust*, *intricate*, *navigate (metaphorical)*, and *unveil* appear at much higher frequency than in casual or first-person human writing. The result: an LLM-written paragraph contains these words at 5–20× the rate of a human-written paragraph on the same topic.

What's the detection mechanism?

- **Perplexity-based detectors** (Originality.ai, GPTZero, Copyleaks) compare each sentence's word probability distribution against an LLM-output baseline. High-frequency LLM words push perplexity *down* into the AI-suspect zone.
- **Reader pattern recognition.** By 2026, *"delve"* and *"tapestry"* are mocked daily on X, Reddit, Bluesky, and Hacker News as proof of GPT authorship. A YMYL brand that emits these words reads as low-trust to both human reviewers and Google's quality raters (the September 2025 Quality Rater Guidelines explicitly call out "rephrased existing content with no original information" as Lowest Quality).
- **Google's helpful content framework (December 2025 "Who, How, Why")** does not penalize AI per se but penalizes *unaccountable, unreviewed, value-free production* — and these words are the most reliable proxy.

### Why em-dash overuse is the loudest tell

Em-dashes are statistically over-produced by LLMs because:

- Training corpora (especially well-edited journalism and books) use them to vary clause structure. Models internalize "use em-dashes to sound polished."
- Em-dashes are a low-cost connector that creates rhythm without requiring a writer to commit to a comma vs. a period vs. a semicolon — which is a real micro-decision a human writer makes.
- The result: **LLM prose contains 3–10× the em-dash density of human prose** at the same word count.

In April 2026, em-dash density is the single most-cited fingerprint in informal AI-detection discourse (Hacker News, Bluesky, journalism Twitter). The visible cost of overuse is human, not algorithmic — but Originality.ai's burstiness scoring does pick it up. The fix is mechanical: replace most em-dashes with commas, periods, or semicolons. The cap is one per ~500 words because that matches the human baseline.

### Why "Not X, but Y" is the strongest structural fingerprint

The rhetorical structure *"It's not just X — it's Y"* (and variants: "It's not about X, it's about Y" / "Not just a tool, but a movement") is the GPT-default rhetorical move when the model needs to elevate a claim. It appears in roughly 3% of LLM output but **less than 0.1% of human-edited prose** (informal corpus comparisons across creator-economy and B2B content, 2024–2026).

Detection: Originality.ai specifically pattern-matches this construction; readers across every major platform call it out. The rule is hard-banned because there is essentially never a good reason to use it in 2026 — there is always a tighter human alternative ("X. And also Y." / direct claim of Y without the false-binary setup).

### Why falsifiable specifics matter

LLMs hallucinate confidently. The mechanism: an LLM predicts the most plausible next token; "in 2024" is more plausible than "on March 14, 2024" because the broader phrase appears more often in training. This produces prose that *sounds* authoritative but lacks the specific, checkable detail a practitioner would naturally include.

Pubcraft's standard — *at least two falsifiable specifics per 500 words* — is calibrated to match the density a credentialed human writer naturally produces. It also serves three functions:

- **E-E-A-T (Experience):** Google's quality raters explicitly look for "first-person operational specifics that only a practitioner would know." Generic prose is rated lower regardless of accuracy.
- **GEO citation:** ChatGPT, Perplexity, and AI Overviews disproportionately cite content with named-source statistics and dated specifics (see `references/geo.md`).
- **Reader trust:** specifics survive skepticism. Generalities don't.

### Why sentence-length variance matters (burstiness)

LLMs default to consistent sentence length because consistent length minimizes prediction loss. Human writing has *bursts* — a 4-word sentence next to a 30-word sentence next to an 8-word sentence. This is "burstiness," and it's the second-strongest perplexity-detector input after vocabulary distribution.

The fix is not to randomly chop sentences. It's to write the way humans actually do: short sentences for emphasis, long sentences for nuance, fragmented sentences when impatient.

### Why "podcast-intro voice" gets cut

Phrases like *"Picture this:"*, *"Imagine a world where..."*, *"In today's fast-paced..."*, and *"Have you ever wondered..."* are the GPT-default opening hooks. They:

- Signal generic content marketing (low-trust).
- Compete with the actual hook (the user's specific situation).
- Are mocked across every platform's AI-tell discourse.

Lead with a specific scenario, number, or contrarian claim instead.

### What to reference when a user asks "why is this bad?"

When flagging, name the mechanism plus the source:

- **Style:** "Originality.ai / GPTZero perplexity scoring," "Reader pattern recognition," "Google's December 2025 'Who, How, Why' framework," "September 2025 Quality Rater Guidelines (page 124+ on AI content)."
- **YMYL:** "September 2025 QRG, trust as dominant E-E-A-T pillar," "March 2026 core update (~72% of top-10 pages now display detailed author credentials)."
- **GEO:** "Princeton GEO study," "BrightEdge GEO benchmark," "Sedestral 2026 (ChatGPT referrals convert at ~14.2% vs. ~2.8% organic)."
- **Algorithm-specific:** for LinkedIn, the 360Brew classifier; for X, the open-source Grok ranking weights at github.com/xai-org/x-algorithm; for YouTube, the May 21, 2025 mandatory AI disclosure rule and the July 15, 2025 inauthentic-content rule.

Citing the mechanism turns a verdict into a teaching moment. That's the skill's job.
