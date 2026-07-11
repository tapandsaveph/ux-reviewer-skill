---
name: risk
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
  - frameworks/severity
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - risk
  - consequence
  - destructive
  - irreversible
  - payment
  - privacy
  - health
  - compliance
load_when:
  - User actions can cause money movement, data loss, privacy exposure, clinical harm, compliance issues, permission changes, or irreversible outcomes.
avoid_when:
  - The workflow is low-consequence browsing, reading, or reversible preference editing.
---

# Risk

## Problem This Solves

Separates helpful friction from unnecessary friction so high-consequence workflows are safe without overcomplicating low-risk work.

## Load When

Load for payments, banking, healthcare, identity, privacy, permissions, destructive actions, approvals, compliance, or irreversible changes.

## Avoid When

Avoid for low-risk, reversible actions where added confirmation would slow users without protecting them.

## Principles

- Risk is a product of likelihood, consequence, reversibility, and user control.
- Safety friction is valuable when consequences are high or hard to undo.
- Frequent low-risk actions should stay fast.
- Rare high-risk actions should be guarded, explained, and auditable.

## Heuristics

- What can go wrong if the user acts?
- Is the consequence visible before action?
- Can the action be undone, reversed, or corrected?
- Does the user have enough context to decide safely?
- Would confirmation prevent harm or merely add delay?
- Should the system require review, permission, or escalation?

## Anti-Patterns

- Removing confirmations from irreversible workflows to reduce clicks.
- Adding confirmation modals to every low-risk action.
- Hiding fees, access impact, renewal terms, or data-loss consequences.
- Treating all errors as equal severity.
- Making risky actions visually indistinguishable from routine actions.

## Recommendations It Should Produce

- Make consequences visible before action.
- Add review/confirm steps for high-risk actions.
- Remove unnecessary confirmation for low-risk reversible actions.
- Separate destructive actions from routine actions.
- Provide undo, recovery, escalation, or audit paths where appropriate.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/severity`
