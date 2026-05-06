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

## Universal regulated-content rules

For any regulated vertical:

- **No "guaranteed" or absolutist language.** "Guaranteed approval," "guaranteed returns," "best in [country]" — out. UDAAP / FTC deception risk.
- **No government-affiliation implications.** No language, seals, or design implying endorsement by an agency unless it's literally true.
- **No fiduciary implication** unless the writer/business genuinely is a fiduciary.
- **Professional advice outside license:** Do not provide tax, legal, medical, or investment advice in voice. Direct readers to consult their own qualified advisor.
- **Discriminatory language or imagery:** Imagery should be representative; targeting may not be based on protected classes (Fair Housing, ECOA, ADA, etc.).
- **Date-and-rate currency:** Any rate, price, or program parameter must be date-stamped and accompanied by a "subject to change" disclosure.

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
