---
name: buttons-actions
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/risk
conflicts_with: []
used_by:
  - skills/ux-implementer
keywords:
  - button
  - action
  - primary action
  - secondary action
  - destructive action
  - call to action
load_when:
  - The interface includes submit, save, approve, delete, continue, cancel, confirm, retry, bulk, or destructive actions.
avoid_when:
  - The work is informational only and has no user action to design.
---

# Buttons And Actions

## Problem This Solves

Makes the next action obvious while keeping destructive, secondary, and unavailable actions safe.

## Load When

Load for forms, checkout, approvals, settings, modals, toolbars, bulk actions, and any flow where action priority matters.

## Avoid When

Avoid for read-only screens with no meaningful action.

## Principles

- One primary action per decision point.
- Button labels should describe the outcome, not the UI mechanic.
- Secondary actions must not compete with the primary action.
- Destructive actions need distance, consequence copy, and confirmation proportional to risk.
- Disabled actions should explain what is missing when users are likely to be blocked.

## Heuristics

- Is there exactly one obvious next action?
- Does the label answer what happens after clicking?
- Are cancel, back, skip, save, submit, and delete visually and semantically distinct?
- Are dangerous actions separated from routine actions?
- Are loading, disabled, permission-denied, success, and failure states defined?
- Do bulk actions show scope and consequence before execution?

## Anti-Patterns

- Generic labels like Submit, OK, Continue, or Update when the outcome is specific.
- Multiple equally prominent actions.
- Destructive and routine actions placed together.
- Disabled buttons with no blocker explanation.
- Icon-only critical actions without labels or accessible names.

## Recommendations It Should Produce

- Rename actions around user outcomes.
- Pick a single primary action and demote the rest.
- Define pending, disabled, success, and error behavior.
- Add consequence copy or confirmation for risky actions.
- Keep action placement consistent across the workflow.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/risk`
