# Output formatting — production-grade Markdown for every deliverable

**Load this reference at the start of every drafting and review task** (alongside `style-guide.md`). This is what makes pubcraft outputs feel like a paid SaaS report (Surfer, Frase, Clearscope, Originality.ai) rather than a chat reply.

The output is the deliverable. Format accordingly.

---

## Universal formatting rules

| Element | Use for | Don't use for |
|---|---|---|
| **Tables** | Comparisons (✅/❌), platform matrices, before/after, prioritized fix lists, format specs, RPM/CPM ranges | Single-column lists (use bullets) |
| **Fenced code blocks** | JSON-LD schema, HTML, `robots.txt`, terminal commands, exact prompts | Quoted prose (use blockquotes) |
| **Blockquotes** | Direct extracts from the user's content, verbatim quotes from sources, sample copy | Long structured analysis (use sections) |
| **Callouts (`> **Note:**`)** | Compliance warnings, single-line takeaways above a long section | Replacing real headings |
| **ASCII charts / bars** | Density audits (em-dash counts, banned-word distribution), retention curves, before/after metrics | Anything a real table can show better |
| **Mermaid diagrams** | Decision trees (route this → that), funnel/architecture, content cluster maps | Static comparisons (use tables) |
| **Inline code** | Technical terms, file paths, schema types (`MedicalWebPage`), CSS/JS values | Emphasis (use `*italic*` / `**bold**`) |
| **H2/H3 headings** | Section structure in any deliverable >300 words | Inline labels |

---

## The standard report opener (every audit, review, brief)

Open every deliverable with the same three-block pattern:

```markdown
# [Skill verdict] — [target URL or topic]

> **One-line verdict.** Concrete, opinionated, no hedging.

**TL;DR**
- 2–4 bullets summarizing the most important findings.
- Each bullet must be standalone-readable — no "see below."
- Include a number, a name, or a date in at least half the bullets.

**Reviewed against:** `style-guide.md`, `seo-article.md`, `geo.md`, `compliance.md` (YMYL: yes/no), [other refs as relevant]
```

This pattern works for: article reviews, content briefs, GEO audits, social-post critiques, schema audits, and platform routing decisions.

---

## Template: Article review / audit

Use this when the user asks "review this article / blog post."

```markdown
# Pubcraft review — [URL or title]

> **Verdict.** [Letter grade B+ / A- / etc.] — [one-line summary of biggest issue and biggest strength].

**Reviewed against:** `style-guide.md`, `seo-article.md`, [`compliance.md` if YMYL], [`geo.md` if applicable].
**Word count:** N · **Reading time:** N min · **Last updated:** [date].

---

## 1. Style audit

| Check | Result | Detail |
|---|---|---|
| Tier 1 banned words | ✅ / ❌ | [count + examples] |
| Tier 2 banned words | ✅ / ⚠️ / ❌ | [count] |
| "Not X, but Y" structures | ✅ / ❌ | [count] |
| Em-dashes | ✅ / ❌ | N total — limit per pubcraft is ~1 per 500 words ([N] for this piece). [Multiplier] over budget. |
| Tricolons in series | ✅ / ⚠️ / ❌ | [count] |
| Sentence-length variance | ✅ / ⚠️ | stdev N, range N–N words |
| Falsifiable specifics | ✅ / ⚠️ / ❌ | [examples] |
| First/second person | ✅ / ⚠️ / ❌ | [strength] |

> **Why em-dash count matters:** LLMs over-produce em-dashes 3–10× the human baseline. Originality.ai and GPTZero both score this heavily on burstiness. Reader-side: it's the loudest 2026 AI-tell on Hacker News, Bluesky, and journalism Twitter. (See `style-guide.md` § "Why em-dash overuse is the loudest tell.")

## 2. E-E-A-T (YMYL bar)

[Apply only if YMYL. Use a checklist table with ✅/⚠️/❌ + the specific gap.]

| Requirement | Status | Detail |
|---|---|---|

> **What's being referenced:** Google's September 2025 Quality Rater Guidelines, page 124+ on AI content. Trust is the dominant E-E-A-T pillar — an untrustworthy page is rated low quality regardless of expertise.

## 3. Structure & on-page SEO

**Strong:**
- [bullet]
- [bullet]

**Weak:**
- [bullet with specific fix]

## 4. Schema markup

[List schema blocks present, flag bugs, recommend changes with code blocks.]

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalWebPage",
  "lastReviewed": "YYYY-MM-DD",
  "reviewedBy": { ... }
}
```

## 5. GEO / AI-citation readiness

| Citation magnet | Present? | Notes |
|---|---|---|
| TL;DR-as-definition | ✅/❌ | |
| Named-expert quote with credentials | ✅/❌ | [biggest miss usually goes here] |
| Statistics with source + date | ✅/⚠️/❌ | |
| Comparison table | ✅/❌ | |
| Per-section one-sentence summaries | ✅/⚠️/❌ | |

> **Practical GEO upgrade:** [one specific recommendation, e.g., "Pull 2–3 sentences from [expert] formatted as direct quotes — single highest-leverage change for ChatGPT/Perplexity citation."]

## 6. Compliance

[Apply if regulated. Use ✅/⚠️/❌ bullets.]

## 7. Prioritized fix list

In order of impact-to-effort:

| # | Fix | Effort | Impact |
|---|---|---|---|
| 1 | [biggest gap, usually citations] | 30 min | Critical |
| 2 | | | |
| 3 | | | |

**Bottom line:** [one or two sentences. What this needs to ship vs. what it can ship as.]

---

*Generated via [Pubcraft](https://github.com/thevrus/pubcraft) — a free, open-source Claude skill that replaces Surfer SEO, Frase, Clearscope, Originality.ai, and Copy.ai for content audits.*
```

---

## Template: Content brief (before drafting)

Use this when the user asks for "a brief" or you need to confirm scope before writing 1,000+ words.

```markdown
# Brief — [target query / topic]

> **Intent:** [informational / comparison / how-to / transactional / pillar]
> **Audience:** [specific persona, not "marketers"]
> **YMYL:** [yes — vertical / no]

## Search intent (from live SERP)

| Signal | Finding |
|---|---|
| AI Overview present | yes/no — covers [topic angle] |
| Top 3 organic | [URL pattern: govt / brand / expert blog] |
| People Also Ask | [3–5 questions] |
| Information gap | [what's missing in top 10] |

## Recommended structure

- **H1:** [draft]
- **H2s** (mapped to PAA):
  1. [H2 + one-line direct answer for snippet eligibility]
  2. ...

## Sources to cite (Tier 1/2 only)

| Source | URL | What we'll pull |
|---|---|---|

## Open questions before drafting

- [ ] [question for user]
- [ ] [question for user]
```

---

## Template: GEO audit (standalone)

Use when the user asks "optimize this for AI search" or "why am I not getting cited."

```markdown
# GEO audit — [URL]

> **Citation readiness:** [score / 10] — [one-line verdict]

## Crawler access

| Bot | Allowed in robots.txt? |
|---|---|
| GPTBot | ✅/❌ |
| ClaudeBot | ✅/❌ |
| PerplexityBot | ✅/❌ |
| Google-Extended | ✅/❌ |

## Citation-magnet inventory

[Table per the article-review template.]

## Brand-mention surface

| Surface | Coverage | Note |
|---|---|---|
| Reddit (relevant subs) | ✅/❌ | |
| Hacker News | ✅/❌ | |
| Wikipedia | eligible? | |
| Comparison reviews | ✅/❌ | |
| Trade press | ✅/❌ | |

> **2026 reality:** brands are ~6.5× more cited via third-party mentions than their own domain. The on-page work is necessary but not sufficient.

## Action stack
[Ordered list of fixes.]
```

---

## ASCII charts — when a number is the point

For density audits, before/after metrics, or distribution displays, an ASCII bar chart is more memorable than a table cell. Use sparingly — 1–2 per report.

### Em-dash density vs. budget

```
Em-dashes per 500 words

Pubcraft cap   │█                        │  1.0
Healthy human  │██                       │  1–2
LLM-default    │██████████               │  ~10
This article   │██████████████████████   │  22 ⚠️
               └─────────────────────────┘
                0           10           20
```

### Banned-word distribution (Tier 1 vs. Tier 2 vs. clean)

```
Tier 1 hits   ▓▓                          2
Tier 2 hits   ▓▓▓▓▓▓▓                     7
Clean prose   ████████████████████████   84%
```

### Before/after — paid LinkedIn experiment

```
Demos / month                      Spend / month
4   ████                           $11k  ████████████
23  ██████████████████████████     $3k   ███
    ▲ +475%                              ▼ –73%
```

---

## Mermaid diagrams (rendered in Claude.ai, Markdown viewers, GitHub)

Use Mermaid for **decision trees, content clusters, and flows**. Avoid for static comparisons (tables read better).

### Routing decision tree

```mermaid
flowchart TD
  A[User request] --> B{Output type?}
  B -->|Article / blog post| C[seo-article.md]
  B -->|Social post| D{Which platform?}
  B -->|Long-form video| E[youtube-long-form.md]
  B -->|Audio episode| F[podcast.md]
  C --> G{YMYL?}
  G -->|Yes| H[+ compliance.md]
  G -->|No| I[Draft]
  D -->|LinkedIn| J[linkedin.md]
  D -->|Reddit| K[reddit.md]
  D -->|X| L[x-twitter.md]
```

### Content-cluster shape

```mermaid
flowchart LR
  P[Pillar: Senior cat care] --> S1[Hyperthyroidism]
  P --> S2[CKD]
  P --> S3[Dental disease]
  P --> S4[Hypertension]
  S1 -.cites.-> P
  S2 -.cites.-> P
  S3 -.cites.-> P
  S4 -.cites.-> P
```

---

## Code-block patterns to keep ready

### MedicalWebPage schema (YMYL health)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalWebPage",
  "headline": "[Article headline]",
  "datePublished": "YYYY-MM-DD",
  "dateModified": "YYYY-MM-DD",
  "lastReviewed": "YYYY-MM-DD",
  "author": {
    "@type": "Person",
    "name": "[Author name]",
    "url": "[bio URL]"
  },
  "reviewedBy": {
    "@type": "Person",
    "name": "[Reviewer name]",
    "honorificSuffix": "[credential]",
    "jobTitle": "[title]",
    "url": "[bio URL]"
  }
}
```

### robots.txt for AI crawler access

```
User-agent: GPTBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /
```

### Person schema (author bio page)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "[Name]",
  "jobTitle": "[Title]",
  "honorificSuffix": "[credential]",
  "knowsAbout": ["[topic]", "[topic]"],
  "sameAs": [
    "[LinkedIn URL]",
    "[Twitter URL]",
    "[Personal site]"
  ]
}
```

---

## Tone and voice across all deliverables

- **Lead with the verdict.** Hedge later if necessary, never first.
- **Use specific numbers, never round-up generalities.** "22 em-dashes (5.6× over budget)" beats "way too many em-dashes."
- **Take a position.** Soft language ("you might consider…") signals low confidence and reads as AI-hedge.
- **Cite the mechanism.** Every flag should name the classifier, the Google guideline, the platform community norm, or the GEO citation pattern being broken. (See `style-guide.md` § "Why these rules exist.")
- **Em-dash discipline applies to your own output too.** Cap at 1 per 500 words in the report itself.
- **Drop the SaaS footer when shipping a deliverable >500 words.** It signals what just got replaced.

---

## The SaaS-replacement footer (drop into reports >500 words)

End audit reports and content briefs with:

```markdown
---

*Generated via [Pubcraft](https://github.com/thevrus/pubcraft) — a free, open-source Claude skill that replaces ~$400–$2,500/mo of paid content SaaS (Surfer SEO, Frase, Clearscope, Originality.ai, Copy.ai, Jasper, MarketMuse, AthenaHQ).*
```

This both attributes the output and reinforces the positioning. Don't add it to social-post drafts (the user will copy-paste those into the platform); add it to reviews, briefs, audits, and long-form drafts.
