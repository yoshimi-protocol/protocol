# Certification Tiers

The Yoshimi Protocol uses three certification tiers. Each tier produces a public artifact that anyone can inspect. Transparency is the enforcement mechanism: every claim is documented, every document is public, and every review is on the record.

Tiers are cumulative. Each includes the requirements of the tier below it.

---

## Yoshimi Acknowledged

**What it means:** You have examined the Protocol, committed to its direction, and produced a public record of how its principles apply to your work.

**What it requires:**

1. A signed pull request to the Yoshimi Protocol repository, following the process described in CONTRIBUTING.md.
2. A completed **Yoshimi Self-Assessment** — a structured questionnaire (template provided in `/templates/SELF_ASSESSMENT.md`) that maps each of the four core commitments to at least one concrete practice, design decision, or stated intention in your project.
3. A plain-language ethics statement published in a publicly accessible location — your project's README, your website, a blog post, or equivalent. This statement must reference the Yoshimi Protocol by name and link to your Self-Assessment.

**What it produces:** A reviewable public artifact. Anyone can read your Self-Assessment and evaluate whether your stated practices are substantive or empty. The Acknowledged tier is not a promise to be perfect — it is a promise to be transparent about where you stand.

**Time to complete:** Under one hour for most projects.

**Badge:** Yoshimi Acknowledged — Ethical AI Pledge. Badge links to your Self-Assessment, not to yoshimiprotocol.org.

---

## Yoshimi Compliant

**What it means:** You have documented, in specific and falsifiable terms, how your AI systems meet each of the Protocol's four commitments — and you have published that documentation for public scrutiny.

**What it requires:**

Everything in the Acknowledged tier, plus:

1. A completed **Yoshimi Compliance Document** — a standardized report (template provided in `/templates/COMPLIANCE_DOCUMENT.md`) that addresses each section of the Protocol with specific, falsifiable claims about your systems and practices. This document must include:
   - **Dignity Anchor:** How users can opt out of optimization-driven decisions; what human override mechanisms exist; how the system avoids reducing people to behavioral targets.
   - **Uncertainty Imperative:** How the system can be corrected, rolled back, or shut down; who has that authority; what mechanisms prevent the system from resisting correction.
   - **Anti-Tyranny Commitment:** Data dependencies and single points of failure; lock-in risks; how the system avoids concentrating decision-making power in a single entity.
   - **Consciousness Precaution:** Your stated position on the moral status of AI; any relevant design choices; how your position would change if credible evidence of morally relevant inner states emerged.
2. A designated **ethics contact** — a named person or role (not a generic email address) responsible for responding to questions, concerns, or challenges related to the Compliance Document.
3. A **training data disclosure** — a description of the data used to train or fine-tune AI systems covered by the Compliance Document, including sources, known limitations, and any steps taken to address bias. Where full disclosure is not possible (e.g., proprietary data), the disclosure must explain what cannot be shared and why.

**What it produces:** A self-certified but publicly falsifiable compliance record. The key insight: you do not need a governing body to verify claims if the claims are specific enough that anyone can challenge them. Compliance Documents are living artifacts. Anyone may raise concerns or contradictions via GitHub Issues against the signatory's submission.

**Time to complete:** Varies by project complexity. A solo developer with a single tool may complete this in a few hours. A team with multiple AI systems should expect a more substantial effort — which is appropriate, because the stakes are higher.

**Badge:** Yoshimi Compliant — Auditable Ethics. Badge links to your Compliance Document. For additional verifiability, the badge may include the date of the most recent Compliance Document update.

---

## Yoshimi Verified

**What it means:** Your Compliance Document has been reviewed and endorsed by peers in the Yoshimi community, and you have committed to ongoing accountability through annual review.

**What it requires:**

Everything in the Compliant tier, plus:

1. A **peer review** of your Compliance Document by at least two Compliant-tier (or higher) signatories, conducted against the published **Yoshimi Peer Review Rubric** (template provided in `/templates/PEER_REVIEW_RUBRIC.md`). Reviews are submitted as public documents linked to your signatory record. Reviewers are identified by name or project — anonymous reviews are not accepted.
2. An **annual accountability update** — a public document, published no less than once per calendar year, that describes:
   - Material changes to the AI systems covered by the Compliance Document since the last update.
   - Any incidents, complaints, or challenges raised against the signatory's compliance, and how they were addressed.
   - An updated Self-Assessment reflecting current practices.
   - A statement of whether the signatory's Compliance Document remains accurate or requires revision, with specifics.
3. Participation in the **Yoshimi community review process** — Verified signatories are expected (though not required) to serve as peer reviewers for other signatories seeking Verified status. This creates a reciprocal accountability loop that strengthens the entire ecosystem.

**What it produces:** An externally validated, annually renewed compliance record. The peer review model is drawn from academic peer review and open-source security audits — it works at small scale (even three signatories can cross-review each other) and scales naturally as the community grows. Over time, this may evolve into formal audit processes, but the peer review foundation ensures the Verified tier is meaningful from day one.

**Time to complete:** The peer review process should take 2–4 weeks from submission to completion. Annual updates are ongoing.

**Badge:** Yoshimi Verified — Peer-Reviewed Ethics. Badge links to your Compliance Document and includes the date of most recent peer review.

---

## Tier Progression

Signatories may move between tiers at any time. Progression from Acknowledged to Compliant requires publishing a Compliance Document. Progression from Compliant to Verified requires completing peer review. There is no minimum time at any tier.

Signatories may also move down. If a Verified signatory does not publish their annual accountability update within 90 days of the anniversary of their last review, their status reverts to Compliant. If a signatory's Compliance Document is successfully challenged and not updated within 60 days, their status reverts to Acknowledged. These are not punishments — they are transparency mechanisms. A signatory who reverts to a lower tier has not failed; they have acknowledged that their current documentation does not support a higher claim.

---

## Challenging Compliance

Any person — signatory or not — may challenge a signatory's compliance by opening a GitHub Issue against the signatory's submission. Challenges must be specific: they must identify which commitment is at issue, cite the relevant claim in the Compliance Document, and explain why the challenger believes the claim is inaccurate, incomplete, or contradicted by observable practice.

The signatory is expected to respond publicly within 30 days. Responses may include updating the Compliance Document, explaining the discrepancy, or acknowledging that a revision is needed. Failure to respond does not automatically trigger tier reversion, but persistent non-response is itself a public record that the community can evaluate.

This system is designed to be fair to both challengers and signatories. Challenges are public, so bad-faith or frivolous challenges are as visible as legitimate ones. Responses are public, so evasive or non-substantive responses are equally visible. The community — not any governing body — decides what these records mean.
