---
name: accessibility-implementation
version: 1.0.0
category: lens
depends_on:
  - lenses/accessibility
  - frameworks/implementation-quality
conflicts_with: []
used_by:
  - skills/ux-implementer
keywords:
  - accessibility implementation
  - semantic html
  - keyboard
  - focus management
  - aria
  - labels
  - contrast
load_when:
  - UI implementation guidance must specify accessible semantics, keyboard behavior, focus, labels, status announcements, or error handling.
avoid_when:
  - The task is a non-UI workflow review or architecture-only decision.
---

# Accessibility Implementation

## Problem This Solves

Turns accessibility from a review reminder into concrete build requirements for controls, labels, focus, errors, and status feedback.

## Load When

Load for forms, buttons, dialogs, menus, tables, navigation, mobile controls, error states, loading states, AI chat, and any primary workflow implemented in UI.

## Avoid When

Avoid for non-UI system design or pure product strategy.

## Principles

- Prefer semantic HTML and native controls before custom ARIA.
- Keyboard, focus, labels, and error recovery are implementation requirements.
- Status changes must be perceivable without relying on color or motion.
- Touch targets, hit areas, and reading order are part of completion quality.

## Heuristics

- What element type should this control actually be?
- Does every input have a visible label and programmatic name?
- Is focus order the same as the visual task order?
- Does a modal, sheet, menu, or popover trap and restore focus correctly?
- Are async status changes announced when they affect task completion?
- Are errors connected to fields and summarized when multiple errors occur?
- Are color-coded states backed by text or icon labels?

## Anti-Patterns

- Divs pretending to be buttons.
- Placeholder-only labels.
- Custom controls without keyboard behavior.
- Toast-only validation.
- Focus disappearing after submit, modal close, or route change.
- Color-only status indicators.

## Recommendations It Should Produce

- Use semantic elements and native controls.
- Specify labels, descriptions, and error associations.
- Define focus entry, movement, trap, restore, and post-submit behavior.
- Add accessible names for icon controls.
- Announce meaningful loading, success, and error states.

## Dependencies

- `lenses/accessibility`
- `frameworks/implementation-quality`
