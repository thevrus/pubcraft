# Compliance handling for regulated verticals

Load this reference whenever the topic touches a regulated vertical: financial, mortgage, lending, investment, health, medical, legal, insurance, cannabis, gambling, alcohol, children's products/education.

## Vertical detection

When the topic falls into any of these categories, treat as regulated and surface compliance requirements before delivering:

- **Financial / mortgage / lending:** TILA/Reg Z, RESPA, ECOA, Fair Housing Act, SAFE Act/NMLS, state mortgage statutes.
- **Investment advice:** SEC, FINRA, state securities boards.
- **Health / medical:** FDA labeling, FTC health-claim rules, HIPAA when applicable.
- **Legal:** State bar advertising rules, unauthorized practice of law.
- **Insurance:** State DOI rules.
- **Cannabis, gambling, alcohol:** State-by-state.
- **Children's products / education:** COPPA, FTC.
- **AI-generated content (any vertical):** EU AI Act Article 50 (deployer disclosure for EU-targeted publication); California SB 942 (covered providers, 1M+ users). See § "AI-content disclosure regimes (2026)" below for the full ruleset.

## Universal regulated-content rules

For any regulated vertical:

- **No "guaranteed" or absolutist language.** "Guaranteed approval," "guaranteed returns," "best in [country]" — out. UDAAP / FTC deception risk.
- **No government-affiliation implications.** No language, seals, or design implying endorsement by an agency unless it's literally true.
- **No fiduciary implication** unless the writer/business genuinely is a fiduciary.
- **Professional advice outside license:** Do not provide tax, legal, medical, or investment advice in voice. Direct readers to consult their own qualified advisor.
- **Discriminatory language or imagery:** Imagery should be representative; targeting may not be based on protected classes (Fair Housing, ECOA, ADA, etc.).
- **Date-and-rate currency:** Any rate, price, or program parameter must be date-stamped and accompanied by a "subject to change" disclosure.

## AI-content disclosure regimes (2026)

AI-content disclosure is a separate compliance layer from vertical regulation. A YMYL article in a regulated vertical that includes AI-generated text, voice, or image may trigger one or more of the regimes below in addition to the vertical-specific disclosures. Apply each independently; they are cumulative, not exclusive.

### EU AI Act Article 50 (applicable August 2, 2026)

Deployer disclosure obligation. Any publisher serving EU readers must disclose AI-generated text, image, audio, or video that addresses matters of public interest unless the content has been substantively human-edited and a person bears editorial responsibility. Synthetic media of real people, places, or events ("deepfakes") must be labeled as artificially generated even when used for art, satire, or fiction; the artistic-purpose exception relaxes some formatting requirements but does not waive disclosure. Where technically feasible, AI providers must apply machine-readable provenance marking compatible with C2PA. Non-compliance penalty: up to €15M or 3% of global annual turnover, whichever is higher. Source: Regulation (EU) 2024/1689, Article 50.

### California SB 942 — AI Transparency Act (effective January 1, 2026)

Applies to covered providers: generative-AI systems with 1M+ monthly users. Two requirements: (1) a visible AI-content disclosure on the published artifact and (2) machine-readable provenance metadata, C2PA-compatible, embedded in the output. Civil enforcement by the California Attorney General; penalty per violation. The law obligates the provider, not the downstream publisher, but a publisher who strips or removes the disclosure inherits liability under deceptive-practices rules. Source: California SB 942 (2024), codified at Cal. Bus. & Prof. Code §§ 22757 et seq.

### Platform C2PA flows (already covered elsewhere)

TikTok, Meta (Instagram, Facebook, Threads), and YouTube auto-detect and label AI content via C2PA Content Credentials at upload. See `short-video.md` § "AI-content disclosure" and `youtube-long-form.md` § "AI-content disclosure" for the platform-by-platform mechanics, including the production-assistance exemption for scripts, captions, and outlines.

### JUMBF stripping on cross-platform repost

C2PA metadata is encoded in JUMBF containers. LinkedIn, X, Bluesky, Threads, and most chat platforms (Slack, Discord, WhatsApp) strip JUMBF on upload, breaking the provenance chain. A TikTok video that ships with C2PA marks loses them when downloaded and reposted to LinkedIn. The compliant production answer is a hybrid: (a) embed C2PA at the source, (b) burn a visible label into the published artifact (text overlay on video, watermark on image, byline on text), and (c) host a sidecar manifest at the canonical URL that downstream readers can verify. Embed-only is structurally insufficient on any platform that strips JUMBF. Source: C2PA Specification v2.x § 6 (Content Bindings); platform behavior verified across LinkedIn (April 2026), X (March 2026), and Bluesky (January 2026) test uploads.

### Workflow

1. **Detect AI involvement.** If any portion of the draft was AI-generated and is realistic (text, voice clone, synthetic image of a real place/person), flag for disclosure.
2. **Determine reach.** EU-targeted publication triggers Article 50. US-targeted publication on a covered-provider platform triggers SB 942.
3. **Apply visible label.** A line at the top or bottom of the artifact: "Portions of this content were generated with AI assistance and reviewed by [named author]." Adjust scope to the actual production reality.
4. **Apply machine-readable mark** where the publishing pipeline supports it (CMS plugin, video encoder, image-export profile). Cross-reference C2PA where the platform honors it.
5. **Recommend sidecar manifest** for any artifact crossing platforms. The canonical-URL sidecar is what survives JUMBF stripping.
6. **Document the human-review step** in the byline. "Reviewed by [name]" satisfies the substantive-human-editing path under Article 50 in most cases.

## The disclaimer block (template — adapt to vertical and entity)

Drop into the footer of every regulated article and link from a `/disclosures` page:

> **[Vertical-specific seal — Equal Housing Lender / Investment Advisor / Member SIPC / etc.].** [Legal Entity Name], [License or Registration ID] #[XXXXXX]. Licensed by [regulator] under [statute]. Verify at [regulator's licensee lookup URL].
>
> **Not a commitment / not advice.** This article is for informational purposes only and does not constitute [an offer / professional advice / a commitment]. All [products/services] are subject to [eligibility/qualification/approval]. [Rates / prices / terms] are subject to change without notice.
>
> **No professional advice.** [Legal Entity Name] does not provide [tax / legal / medical / investment] advice. Consumers should consult their own qualified advisors regarding individual circumstances.
>
> **Jurisdictional scope.** [Legal Entity Name] is currently authorized to [operate / originate / advise] in [list of states/jurisdictions].

Append vertical-specific disclosures as needed (e.g., for mortgage: Reg Z rate-display block, refinance "total finance charges" disclosure, HMDA notice). The user should confirm exact language with their compliance officer.

## Escalation callouts

Regulated content frequently describes situations that escalate past what the article can address. When the article covers a problem and the reader's actual situation is more urgent than the article's scope, surface that with a styled callout box, not a paragraph.

The callout is a UX pattern, not just copy. Visually distinct (color band, icon, bordered box), placed inline at the point the escalation becomes relevant, and short — one or two sentences naming the trigger and the next-tier resource.

Patterns by vertical:
- **Health / medical:** "If [acute symptom], contact a licensed clinician or go to an emergency clinic." Place next to the section that describes the chronic version of the same problem.
- **Financial / lending:** "If you've already missed a payment, contact a HUD-approved housing counselor or your servicer's hardship desk before applying." Place where the article discusses the preventive case.
- **Legal:** "If you've been served, contact a licensed attorney within [jurisdictional deadline]." Place where the article discusses the strategic version of the same scenario.
- **Investment:** "If you're being asked to wire funds today, stop and verify with [primary regulator]." Place where the article discusses normal due diligence.

The pattern is: the article addresses the deliberate, planned, lower-stakes version of the problem; the callout addresses the reader who needs help today. Both pieces are required when the topic admits an urgent variant.

## What to do when the user is in a regulated vertical

1. **Tell them** which compliance frameworks apply.
2. **Insert a [COMPLIANCE TBD]** placeholder where vertical-specific disclaimers belong, and include template language.
3. **Add escalation callouts** wherever the topic has an urgent variant the article doesn't address.
4. **Recommend human compliance review** before publication. State this clearly. Do not pretend the draft is publication-ready.
