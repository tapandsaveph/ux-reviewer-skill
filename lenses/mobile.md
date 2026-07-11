---
name: mobile
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - mobile
  - phone
  - tablet
  - handheld
  - touch
  - offline
  - interruption
load_when:
  - The workflow happens on phones, tablets, handheld scanners, field devices, or small touch screens.
avoid_when:
  - The workflow is desktop-only and has no touch, small-screen, interruption, or mobility constraint.
---

# Mobile

## Problem This Solves

Applies mobile context constraints so reviews account for touch input, small screens, interruption, poor network, and field use.

## Load When

Load for mobile apps, responsive screens, tablet workflows, handheld scanners, field operations, mobile signup, and any flow affected by touch or interruption.

## Avoid When

Avoid for desktop-only workflows unless the same workflow must also work on mobile.

## Principles

- Mobile workflows should preserve context through interruption.
- Critical actions must be reachable and touch-safe.
- Network and device constraints should not cause silent data loss.
- Reduce typing through defaults, scanning, selection, and saved context.

## Heuristics

- Can the user complete the primary task with one hand or touch input?
- Are targets large enough and spaced for touch?
- Is progress preserved after app switch, lock, poor network, or retry?
- Are long forms, tables, and dense controls adapted to small screens?
- Are camera, scanner, location, or notification permissions requested at the moment of need?
- Does the workflow avoid hidden hover-only behavior?

## Anti-Patterns

- Desktop tables squeezed onto mobile without task priority.
- Losing entered data after interruption or network failure.
- Permission prompts before users understand the benefit.
- Tiny adjacent destructive and primary actions.
- Critical controls available only on hover.

## Recommendations It Should Produce

- Prioritize the mobile primary action and defer secondary detail.
- Preserve partial progress through interruption and poor network.
- Replace typing with scan, select, default, or saved context where safe.
- Request device permissions only when needed.
- Separate risky touch targets from routine actions.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
