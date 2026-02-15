# Contributing to the Yoshimi Protocol

This Protocol belongs to its community. That means you.

This document explains how to participate — whether you want to sign the
Protocol, challenge something in it, propose an amendment, or report a
violation.

---

## How to Sign the Protocol

Signing is a public act. It means you commit to operating by these
principles and invite the community to hold you to them.

There are three tiers. Each produces a public artifact that anyone can
inspect. Start where you are — you can progress at any time.

### The Process

All sign-ons follow the same steps:

1. **Fork this repository.**
2. **Complete the required artifacts for your tier** (see below).
3. **Host your artifacts publicly** — in your own project repo, on your website, or wherever you choose. You control your compliance documents. The protocol repo only links to them.
4. **Add your entry to `src/data/signatories.json`** using the format below.
5. **Open a pull request.**

Your entry format:

```json
{
  "name": "Your Name or Project",
  "github": "your-github-handle",
  "organization": "Your Org or Independent",
  "tier": "acknowledged",
  "date": "YYYY-MM-DD",
  "project": "Name of the AI project being pledged (optional)",
  "selfAssessmentUrl": "https://link-to-your-completed-self-assessment",
  "ethicsStatementUrl": "https://link-to-your-public-ethics-statement",
  "complianceDocUrl": null,
  "ethicsContact": null
}
```

A maintainer will review and merge your PR. Your sign-on will appear
on the public signatories page at yoshimiprotocol.org once the site
rebuilds.

**Why this approach:**
- **Privacy-first.** No data collection on the website. No forms. No email harvesting. You share exactly what you choose to share in your PR.
- **Anti-spam.** Requires a GitHub account and a PR review. Natural quality filter.
- **Transparent.** The entire signatory list is version-controlled and publicly auditable.
- **Community-owned.** Anyone can fork. No single entity controls the data.

---

### Acknowledged Tier

The entry point. A public commitment with a real output.

**Artifacts to complete and host publicly:**

1. **A completed [Self-Assessment](templates/SELF_ASSESSMENT.md).** This is a structured questionnaire that maps each of the four core commitments to at least one concrete practice, design decision, or stated intention in your project. Be honest — acknowledging gaps is more valuable than performing completeness.
2. **A plain-language ethics statement** published somewhere publicly accessible — your project's README, your website, a blog post, or equivalent. It must reference the Yoshimi Protocol by name and link to your Self-Assessment.

**In your JSON entry, set:**
- `tier`: `"acknowledged"`
- `selfAssessmentUrl`: link to your hosted Self-Assessment
- `ethicsStatementUrl`: link to your published ethics statement
- `complianceDocUrl`: `null`
- `ethicsContact`: `null`

**Time to complete:** Under one hour for most projects.

---

### Compliant Tier

The substantive tier. You document, in specific and falsifiable terms,
how your AI systems meet each of the Protocol's four commitments.

Everything in the Acknowledged tier, plus:

**Additional artifacts to complete and host publicly:**

1. **A completed [Compliance Document](templates/COMPLIANCE_DOCUMENT.md).** This is a standardized report that addresses each section of the Protocol with specific, falsifiable claims. If someone reading your Compliance Document could not determine whether your claims are true, the claims are not specific enough.
2. **A training data disclosure** is included as part of the Compliance Document, covering sources, known limitations, and steps taken to address bias. Where full disclosure is not possible, explain what cannot be shared and why.
3. **A named ethics contact** — a real person or role (not a generic email address) responsible for responding to questions, concerns, or challenges.

**In your JSON entry, update:**
- `tier`: `"compliant"`
- `complianceDocUrl`: link to your hosted Compliance Document
- `ethicsContact`: name and contact method for your designated ethics contact

Compliance Documents are living artifacts. Update them when your systems
or practices change materially, and update the link in `signatories.json`
if the URL changes.

---

### Verified Tier

Peer-reviewed accountability with an annual commitment.

Everything in the Compliant tier, plus:

1. **Request peer review** from two Compliant-tier (or higher) signatories. Reviews are conducted against the [Peer Review Rubric](templates/PEER_REVIEW_RUBRIC.md) and submitted as public documents — hosted by the reviewer or the reviewee, linked from both parties' records.
2. **Both reviewers must rate all sections as "Meets Standard" or "Meets Standard with Observations"** for Verified status to be granted. If either reviewer recommends revisions, address them and resubmit.
3. **Commit to an annual accountability update** — a public document, published no less than once per calendar year, describing material changes, incidents, challenges, and whether your Compliance Document remains accurate.

**In your JSON entry, update:**
- `tier`: `"verified"`

**Note on timing:** Peer reviews will commence once the community has
active Compliant-tier signatories available to serve as reviewers. In
the founding period, the Protocol is being established by its creator
and all contributions are from the founder. The Verified tier becomes
operational as the community grows — this is by design, not a gap.

---

### Tier Progression and Reversion

To move up a tier, update your JSON entry via PR with the new tier
value and any additional required URLs. To move down voluntarily,
submit the same kind of update.

If a Verified signatory does not publish their annual accountability
update within 90 days of the anniversary of their last review, their
status reverts to Compliant. If a signatory's Compliance Document is
successfully challenged and not updated within 60 days, their status
reverts to Acknowledged. These are transparency mechanisms, not
punishments. Full details in [CERTIFICATION_TIERS.md](CERTIFICATION_TIERS.md).

---

## How to Challenge Compliance

Any person — signatory or not — may challenge a signatory's compliance.

**Open an Issue using this format:**

**Title:** `Compliance Challenge: [Signatory name]`

**Body:**
```
Signatory:
Commitment at issue: [Dignity Anchor / Uncertainty Imperative /
Anti-Tyranny Commitment / Consciousness Precaution]
Relevant claim: [Quote or reference the specific claim in the
signatory's Compliance Document]
The concern: [Explain why you believe the claim is inaccurate,
incomplete, or contradicted by observable practice]
```

The signatory is expected to respond publicly within 30 days.
Challenges must be specific — identify the commitment, cite the claim,
and explain the concern. This system is designed to be fair to both
sides: bad-faith challenges are as visible as legitimate ones, and
evasive responses are as visible as substantive ones.

---

## How to Challenge the Protocol

If you think something in the Protocol is wrong, incomplete, harmful,
or missing — say so. That's not opposition. That's exactly how this
is supposed to work.

**Open an Issue using this format:**

**Title:** `Challenge: [The principle or section you're questioning]`

**Body:**
```
Section:
The problem:
What you'd propose instead (if anything):
```

Challenges will be discussed publicly. Strong challenges that reveal
genuine gaps will be incorporated into the amendment process.

---

## How to Propose an Amendment

Amendments follow the tiered process defined in Part VII of the
Protocol.

**For Tier Three Standards** (operational commitments):
Open a Pull Request directly against `PROTOCOL.md` with your proposed
change. Include in the PR description:
- What you're changing and why
- What harm or gap this addresses
- Whether you're aware of any tradeoffs or objections

A 60-day comment period begins when the PR is opened. Amendments
require 60% approval from participating community members.

**For Tier Two Principles** (structural governance):
Open an Issue first — labeled `amendment: tier-two` — before opening
a PR. Tier Two changes require a 90-day deliberation period and 75%
supermajority approval.

**For Tier One Commitments** (the immutable core):
These cannot be weakened or removed. Proposed clarifications or
extensions may be submitted as Issues labeled `amendment: tier-one`
and will be held to the highest deliberation standard.

---

## How to Report a Violation

If a certified signatory is acting in material violation of their
stated commitments:

Open an Issue titled `Violation: [Signatory name]` and describe
the violation with as much specificity as you can provide. The
Stewardship Council will review and respond within 30 days.

---

## Repository Structure

```
yoshimi-protocol/protocol/
├── README.md
├── PROTOCOL.md
├── CERTIFICATION_TIERS.md
├── CONTRIBUTING.md
├── LICENSE
├── src/
│   └── data/
│       └── signatories.json
└── templates/
    ├── SELF_ASSESSMENT.md
    ├── COMPLIANCE_DOCUMENT.md
    └── PEER_REVIEW_RUBRIC.md
```

---

## Tone and Community Standards

This community exists because people believe building minds carries
responsibilities. Disagreement is welcome. Bad faith is not.

Contributions that demean, harass, or act in bad faith toward other
community members will be removed.

The Protocol's values apply here too.

---

## A Note on Forking

If you believe the governance of this Protocol has been captured by
a single interest — that it no longer belongs to its community — you
have the unconditional right to fork it. That right is written into
the Protocol itself and cannot be revoked.

We hope you never need to use it. We're glad it exists.

---

*The Yoshimi Protocol · github.com/yoshimi-protocol · CC0 1.0 Universal*
