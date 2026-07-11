---
name: trust
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/risk
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - trust
  - confidence
  - privacy
  - consent
  - payment
  - identity
  - AI
  - consequence
load_when:
  - Users must trust money movement, identity, privacy, consent, health, AI output, permissions, or irreversible consequences.
avoid_when:
  - The workflow has no sensitive data, consequence, uncertainty, or trust boundary.
---

# Trust

## Problem This Solves

Helps users feel safe acting when consequences, sensitive data, uncertainty, or institutional trust are involved.

## Load When

Load for banking, checkout, healthcare, identity, privacy, consent, AI answers, permissions, account deletion, or billing impact.

## Avoid When

Avoid for routine low-risk workflows where trust cues would become clutter or marketing.

## Principles

- Trust comes from clarity, consequence visibility, control, and recovery.
- Users should know what will happen before they act.
- Sensitive data use should be explained at the point of decision.
- Trust cues must support the workflow, not decorate it.

## Heuristics

- Are fees, renewal terms, privacy impact, or access impact visible before action?
- Does the user understand who receives data or authority?
- Is consent specific and timely?
- Are uncertain outputs labeled with source, confidence, or escalation path?
- Can users recover from mistakes?
- Are trust cues placed near the decision they support?

## Anti-Patterns

- Generic reassurance copy far from the risky action.
- Hidden taxes, fees, renewal, access, or data-sharing consequences.
- Consent bundled with unrelated actions.
- AI answers without sources or boundaries.
- Trust badges used instead of clear terms.

## Recommendations It Should Produce

- Place consequence and privacy microcopy near the action.
- Expose terms, fees, recipients, and access impact before commit.
- Separate consent from unrelated choices.
- Add review steps for sensitive decisions.
- Provide recovery, support, or escalation paths.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/risk`
