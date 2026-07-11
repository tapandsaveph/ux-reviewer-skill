---
name: severity
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - severity
  - priority
  - risk
  - critical
  - high
  - medium
  - low
load_when:
  - Findings need prioritization by task impact, safety, risk, accessibility, or production consequences.
avoid_when:
  - Never avoid for ux-reviewer; it is a required framework.
---

# Severity

## Problem This Solves

Keeps reviews focused on the highest-impact workflow, safety, accessibility, and production risks instead of cosmetic preference.

## Load When

Load for every UX review that produces recommendations.

## Avoid When

Do not avoid for `ux-reviewer`.

## Principles

- Severity follows user and business impact.
- Safety outranks speed when consequences are irreversible or regulated.
- Prefer one root-cause recommendation over many symptom-level fixes.
- Low-severity polish should not distract from task completion, trust, or recovery.

## Heuristics

- Critical: blocks core task completion, causes likely data loss, unsafe approval, destructive action, inaccessible primary workflow, or hidden payment/compliance/privacy consequences.
- High: makes the primary action unclear, adds unnecessary frequent steps, omits required async/error/validation/approval feedback, or creates repeated mistakes.
- Medium: slows users down but leaves a discoverable path, uses confusing labels/grouping, or shows too much information too early.
- Low: improves confidence, clarity, copy, spacing, or consistency after the core workflow is understandable and safe.

## Anti-Patterns

- Ranking visual polish above blocked task completion.
- Treating every issue as high priority.
- Ignoring auditability, permissions, ownership, or recovery when assigning severity.
- Penalizing safety confirmations that are necessary for high-risk actions.

## Recommendations It Should Produce

- Order findings from highest to lowest severity.
- Explain why each issue matters to task completion, safety, trust, or business outcome.
- Recommend the simplest safe fix for each issue.
- Call out what should not change when existing controls protect users or the business.

## Dependencies

- `frameworks/workflow-analysis`
