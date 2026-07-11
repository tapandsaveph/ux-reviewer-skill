---
name: source-of-truth
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - source of truth
  - status
  - duplicate
  - derived
  - ownership
  - reporting
  - data
load_when:
  - A workflow shows status, readiness, ownership, blockers, reporting, inventory, payments, approvals, or duplicated facts.
avoid_when:
  - The review is about static copy or layout with no business facts, status, or data ownership.
---

# Source of Truth

## Problem This Solves

Prevents UX recommendations from creating duplicate business facts, stale status, or reporting inputs that should derive from operational data.

## Load When

Load when the scenario includes status, readiness, blockers, ownership, approvals, payments, inventory counts, reporting, or repeated data entry.

## Avoid When

Avoid when no business fact, status, ownership, or derived data appears in the workflow.

## Principles

- Every important business fact has one owner.
- Derived values should be calculated, not stored as separate truth.
- Reports read from source records; they do not ask users to enter facts twice.
- UI labels should reveal source status without exposing database language.

## Heuristics

- What existing data already represents this truth?
- Is status derived from requirements, approvals, payments, inventory, or compliance records?
- Could two fields disagree?
- Does the user know which record or person owns the next step?
- Can reports trace back to source records?
- Is freshness or last-updated time important?

## Anti-Patterns

- Duplicate ready, blocked, completed, or approved flags.
- Editable reporting fields that mirror operational data.
- Backend enum names shown as user-facing status.
- Status summaries with no drill-down to source facts.
- Manual re-entry of facts already known to the system.

## Recommendations It Should Produce

- Derive readiness, blockers, and progress from source records.
- Show source status, owner, and last-updated context when relevant.
- Remove duplicate fields or reporting inputs.
- Use user-facing labels for source-backed status.
- Link summaries to the source records behind them.

## Dependencies

- `frameworks/workflow-analysis`
