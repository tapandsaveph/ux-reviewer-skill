---
name: visual-design
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - visual hierarchy
  - hierarchy
  - layout
  - scan
  - emphasis
  - spacing
  - cards
load_when:
  - Visual hierarchy, scanability, layout grouping, emphasis, or content priority affects task completion.
avoid_when:
  - The issue is workflow, domain, safety, or data correctness and visual hierarchy is not a material factor.
---

# Visual Design

## Problem This Solves

Uses visual hierarchy to make the next useful decision obvious without defaulting to decorative polish.

## Load When

Load when layout, grouping, density, emphasis, chart legibility, scanability, or visual priority affects the workflow.

## Avoid When

Avoid when recommendations would only make the UI prettier without improving comprehension or action.

## Principles

- Hierarchy should make the next decision obvious.
- Lead with task, status, and next action.
- Metadata and audit details should be quieter than task-critical facts.
- Color should not be the only hierarchy.

## Heuristics

- Does the screen title match the task?
- Is the primary action prominent without competing with status?
- Are related items grouped?
- Are warnings and blockers placed near the affected action?
- Does spacing communicate groups without creating decorative emptiness?
- Are repeated items presented with the right density for scanning?

## Anti-Patterns

- Hero treatment inside operational tools.
- Equal visual weight for everything.
- Color-only hierarchy.
- Cards used where table density would improve scanning.
- Decorative spacing that pushes task-critical content below the fold.

## Recommendations It Should Produce

- Lead with task, status, and next action.
- Use consistent heading levels.
- Use table density for scanning repeated objects.
- Demote rarely used metadata.
- Keep destructive actions visually separate.

## Dependencies

- `frameworks/workflow-analysis`
