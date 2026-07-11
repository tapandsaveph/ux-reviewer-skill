---
name: accessibility
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - accessibility
  - keyboard
  - screen reader
  - focus
  - contrast
  - aria
  - touch target
load_when:
  - The review involves controls, forms, errors, modals, status indicators, keyboard use, screen reader use, mobile touch, or accessibility risk.
avoid_when:
  - The review is purely conceptual and has no user interface or interaction surface.
---

# Accessibility

## Problem This Solves

Ensures the primary workflow is completable by users relying on keyboard, assistive technology, sufficient contrast, visible focus, and clear error feedback.

## Load When

Load for UI screens, forms, modals, menus, status indicators, mobile controls, error states, or any core task with accessibility impact.

## Avoid When

Avoid only when no UI or interaction behavior is being reviewed.

## Principles

- Accessibility is part of task completion.
- Native controls are preferred when they satisfy the workflow.
- Errors, focus, labels, and status must be perceivable and operable.
- Color cannot be the only carrier of meaning.

## Heuristics

- Can the workflow be completed with keyboard only?
- Is focus order logical and visible?
- Do controls have accessible names?
- Are errors announced and tied to fields?
- Does color convey meaning with text or icon backup?
- Is contrast sufficient for body text, controls, and status indicators?
- Are touch targets large enough on mobile?
- Are modals, menus, and drawers focus-managed?

## Anti-Patterns

- Icon-only controls without accessible names.
- Error summaries that are not connected to fields.
- Status conveyed by color alone.
- Hover-only access to critical actions.
- Focus traps in modals or drawers.

## Recommendations It Should Produce

- Use native controls where possible.
- Put error text near affected inputs.
- Add text labels to status colors.
- Keep interactive elements reachable and predictable.
- Test the primary workflow without a mouse.

## Dependencies

- `frameworks/workflow-analysis`
