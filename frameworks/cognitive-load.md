---
name: cognitive-load
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - cognitive load
  - too many choices
  - confusing
  - unclear
  - memory burden
  - duplicate actions
load_when:
  - A review needs to evaluate choices, memory burden, information timing, labels, or unnecessary steps.
avoid_when:
  - Never avoid for ux-reviewer; it is a required framework.
---

# Cognitive Load

## Problem This Solves

Finds avoidable mental effort that prevents users from confidently completing the workflow.

## Load When

Load for every UX review and whenever users face many choices, fields, labels, paths, or hidden dependencies.

## Avoid When

Do not avoid for `ux-reviewer`.

## Principles

- Reduce decision ambiguity before reducing visual density.
- Dense expert screens can be acceptable when they improve scanning and preserve context.
- Users should not need to remember information from another screen.
- Advanced or rare choices should appear only when needed.
- Do not add tutorials before simplifying the workflow.

## Heuristics

- Can the user identify the primary action in five seconds?
- Are there more than 5-7 competing choices at one level?
- Are similar actions duplicated under different labels?
- Are required fields, blockers, and consequences visible before action?
- Are system terms replaced with user-task language?
- Is information shown at the moment it supports a decision?
- Are expert shortcuts preserved without forcing beginners through complexity?

## Anti-Patterns

- Treating dense as automatically bad.
- Adding filters, tabs, tours, or settings before removing clutter.
- Explaining confusing behavior instead of making defaults clearer.
- Optional fields that exist only for reporting wants.
- Separate modules or pages for decisions that happen together in real life.

## Recommendations It Should Produce

- Make one primary action obvious per workflow step.
- Group related information by user decision.
- Remove duplicate actions and routes.
- Replace explanations with clearer defaults.
- Show blockers next to the action they block.
- Defer optional or advanced inputs until they are needed.

## Dependencies

- `frameworks/workflow-analysis`
