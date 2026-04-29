# Dev.to / Hashnode (developer publishing)

Load this reference when drafting for Dev.to or Hashnode.

## Dev.to

- **Algorithm:** tag-feed + home-feed + weekly/monthly trending ("top posts of the week"). Editor-curated trending lists. Reactions (♥ 🦄 🔖) and comments both feed visibility; in 2025–2026 the **save (🔖 bookmark) is the strongest "quality" signal**.
- Distribution lives inside the dev.to domain — your post stays on their URL, but they support **canonical URLs** so you don't lose SEO from your own blog.
- **Format:** Markdown editor; cover image (1000×420 ideal); 3–4 tags max (`#javascript`, `#webdev`, `#beginners`, `#tutorial` are highest-traffic); TL;DR at top works.
- **Works:** "I built X with Y" project posts, beginner-friendly tutorials with extensive screenshots and code blocks, "X things I wish I knew when I started [role]" lists, hot-take career posts, post-mortems on bugs/incidents.
- **Fails:** marketing-coded posts, AI-written tutorials with hallucinated APIs (the comment section is brutal — devs run code), short opinion pieces, content with broken/outdated code blocks.
- **Optimal length:** 800–2,000 words for tutorials; 400–800 for opinion/career. Code blocks should be ≥30% of visible content for tutorials.

## Hashnode

- **Architecture:** hybrid — your posts live on **your own custom domain** (free domain mapping is the killer feature) AND distribute through the Hashnode network feed.
- **Distribution:** Hashnode **Featured** section, topic feeds (#oracle, #aws, etc.), and SEO from your own domain (long-term compounding).
- **2026 working patterns:** technical deep dives, AI/ML implementation walkthroughs, "X days of [topic]" series, framework-specific tutorials. Hashnode 2026 data: posts with code snippets and diagrams achieve **2× engagement vs. text-only**.
- **Fails:** opinion-only posts (less audience), career-advice posts (less engagement than dev.to), short pieces.
- **Trade-off vs. Dev.to:** Hashnode's traffic per featured post is generally lower than dev.to's, *but* it builds your owned domain authority instead of dev.to's. Multiple developer-survey 2025–2026 posts concur: **Hashnode for ownership, Dev.to for reach.**

## Cross-posting strategy (2026)

The best practice (cited in TechContentPro 2026 benchmark): publish first on **your own blog** (Hashnode-mapped or self-hosted), then cross-post with `canonical_url` set to your blog on Dev.to and Medium. ContentIQ Analytics shows verbatim cross-posts without canonical see ~65% drop in organic traffic over 6 months.

## Optimal article length and structure for technical tutorials (2026)

- 1,200–2,500 words for tutorials.
- One H1, H2 every ~300–500 words.
- Code-block ratio: ~30% for tutorials, ~15% for conceptual posts.
- Cover image 1200×630 (OG-card friendly).
- TL;DR at top; "what you'll learn" bullet list; numbered steps for tutorials; final "what's next/related reading" section.
- Embed working examples (CodeSandbox, StackBlitz) when possible — boosts retention significantly.

## AI content (developer-specific reception)

This is the platform category where AI-content reception is **most hostile** — because developers can run the code:

- **Hallucinated APIs**, made-up library functions, or syntactically-clean-but-wrong examples get torn apart in comments.
- "ChatGPT wrote this" is the most cutting Dev.to comment.
- Hashnode is slightly more permissive (the platform itself ships AI-writing features), but the audience remains skeptical.
- Best practice: if you used AI, *say so*, and explicitly state that you ran every code block. Disclose AI involvement at the top.

## Community norms / banned moves

- **Dev.to** has an active Code of Conduct; harassment/dismissiveness is moderated.
- Don't paste affiliate links without disclosure.
- Don't post "click here for full article on my site" stub posts (community calls these out; mods may unpublish).
- Don't auto-post from RSS without canonical handling.
- Don't use `#beginners` tag for advanced content (tag editors will downrank).

## Compliance

- For developer audiences, the relevant compliance is **license disclosure** for code samples (MIT, Apache, etc.) and security-disclosure norms for vulnerability writeups (responsibly-disclosed and patched before publication).
- For tools/services you promote: disclose any commercial relationship at the top, not the bottom.

## Hooks/titles that work in 2026

- "I built a Postgres clone in 1,200 lines of Rust"
- "What `fork()` actually copies (with strace traces)"
- "7 Days of Docker in 2026 — Day 4: when containers need to talk and remember"
- "I migrated 4M rows from MongoDB to Postgres with zero downtime. Here's the runbook."
- "Why I'm moving my blog from Dev.to to Hashnode" (a perennial format)

## AI-tells / banned phrases that get developers especially mad

*"Let's dive in!"*, *"In the ever-evolving world of [tech],"* the *"What is [X]? Why is it important?"* H2 ladder, code samples without imports, code that uses fictional methods (e.g. `array.shuffle()` in JS), captions like *"This simple trick will make you 10x faster"*, the closing *"By following these best practices, you'll be well on your way to..."* sentence, and the signature `console.log("Hello, World!");` in a tutorial about an unrelated topic (it's a meme tell now).

## Where developers should publish in 2026 (honest assessment)

- **Your own blog (custom domain) → primary canonical.** Best long-term SEO, ownership, brand.
- **Hashnode with custom domain mapping → equivalent to your own blog**, with bonus discovery from the network. Excellent default for devs without DevOps appetite.
- **Dev.to → cross-post for reach.** Larger audience, more comments, better top-of-funnel.
- **Medium → cross-post only if you have a non-developer adjacent audience.** Medium's developer audience has shrunk; not worth being primary.
- **Substack → only if your dev content is opinion/essay-shaped, not tutorial-shaped.** Tutorials don't render well in email.
- **Hacker News → submit your *best* original-research piece, once per quarter, to your own blog URL.**

## Verdict

**Both alive and worth using.** Best 2026 stack for developer content: **Hashnode-on-your-domain (canonical) → cross-post to Dev.to → submit milestone pieces to HN.**
