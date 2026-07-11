---
name: implementation-quality
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
  - frameworks/production-safety
conflicts_with: []
used_by:
  - skills/ux-implementer
keywords:
  - implementation
  - buildable
  - component
  - states
  - production
  - acceptance
load_when:
  - A review must turn UX, UI, PRD, prototype, or screen requirements into buildable interface guidance.
avoid_when:
  - The task is only research, product critique, or visual inspiration with no implementation decision.
---

# Implementation Quality

## Problem This Solves

Prevents implementation guidance from staying at the level of opinion. The output should be specific enough for a product engineer to build without inventing missing workflow behavior.

## Load When

Load when producing UI structure, component guidance, state requirements, acceptance criteria, or implementation notes.

## Avoid When

Avoid for pure audits, strategy notes, or visual moodboarding.

## Principles

- Build the workflow before polishing the surface.
- Every component should support a task, decision, feedback state, or recovery path.
- Prefer native controls and existing design-system components before custom UI.
- Implementation guidance must name states, validation, disabled behavior, and success/failure feedback.
- Do not add configurability until the workflow proves it needs variation.

## Heuristics

- Can an engineer identify the container, controls, primary action, secondary actions, and states?
- Are loading, empty, error, validation, pending, saved, and success states defined where relevant?
- Is each field, button, table column, or card tied to a user decision?
- Is copy written in user-facing language rather than backend names?
- Are destructive or high-risk actions separated, confirmed, and recoverable where possible?
- Does the design preserve auditability, permissions, and source-of-truth ownership?

## Anti-Patterns

- "Make it cleaner" without component or state guidance.
- New components when native controls or existing components work.
- A design that only covers the happy path.
- Hidden validation rules.
- Styling recommendations that do not improve comprehension, feedback, or task completion.

## Recommendations It Should Produce

- Name the screen structure and component responsibilities.
- Specify required interaction states and validation behavior.
- Use existing components before introducing new ones.
- Turn vague UI requests into acceptance-checkable implementation steps.
- Keep nonessential polish out of the first implementation pass.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/production-safety`
