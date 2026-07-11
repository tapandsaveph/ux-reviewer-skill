---
name: platform-conventions
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-implementer
keywords:
  - platform
  - conventions
  - web
  - mobile
  - ios
  - android
  - material
  - HIG
load_when:
  - Interface guidance depends on web, mobile, iOS, Android, desktop, native, or design-system conventions.
avoid_when:
  - The implementation target is unknown and no platform-specific behavior is being decided.
---

# Platform Conventions

## Problem This Solves

Keeps implementation guidance familiar for the target platform instead of inventing custom controls for common behavior.

## Load When

Load for mobile apps, native-feeling flows, web app controls, menus, navigation, sheets, dialogs, toolbars, keyboard behavior, or design-system alignment.

## Avoid When

Avoid when the platform is irrelevant or unspecified and generic workflow guidance is enough.

## Principles

- Familiar controls reduce cognitive load.
- Platform navigation, confirmation, input, and feedback patterns should be respected unless they block the workflow.
- Use native semantics before custom ARIA.
- Match destructive, modal, and permission behavior to platform expectations.

## Heuristics

- Is the primary action placed where users expect it on this platform?
- Does navigation use familiar page, tab, drawer, sheet, or stack behavior?
- Are dialogs reserved for decisions that interrupt the workflow?
- Do inputs use platform-supported types, keyboards, pickers, and validation?
- Are gestures optional, discoverable, and backed by visible controls?

## Anti-Patterns

- Custom dropdowns, date pickers, or toggles where native controls work.
- Web-style dense tables forced into small mobile screens.
- Hidden gesture-only actions.
- Platform-inconsistent destructive confirmations.
- Treating Material or HIG as decoration instead of behavior guidance.

## Recommendations It Should Produce

- Choose standard platform components for common jobs.
- Adapt layout density and control placement to the target device.
- Keep navigation and modal behavior predictable.
- Use native input types and semantic markup where possible.

## Dependencies

- `frameworks/workflow-analysis`
