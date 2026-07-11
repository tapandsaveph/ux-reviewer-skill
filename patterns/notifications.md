---
name: notifications
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - notification
  - toast
  - alert
  - microinteraction
  - feedback
  - pending
  - saved
load_when:
  - The workflow needs local feedback, state change confirmation, async progress, alerts, or interruption handling.
avoid_when:
  - Motion or messaging is only decorative and does not clarify state, feedback, or continuity.
---

# Notifications

## Problem This Solves

Makes system feedback visible, local, and useful without interrupting the workflow unnecessarily.

## Load When

Load when reviewing toasts, alerts, pending states, saved states, inline confirmations, async feedback, or motion used to communicate state.

## Avoid When

Avoid when the request is about static layout, copy, or data structure with no feedback or notification behavior.

## Principles

- Feedback should clarify state, progress, or consequence.
- Prefer immediate local feedback over detached messages.
- Motion should be short, interruptible, and meaningful.
- Critical errors should not disappear before users can recover.

## Heuristics

- Does the button or control show pending state while submitting?
- Does validation appear near the input it affects?
- Does saved state confirm without interrupting work?
- Does a transition explain where an item moved?
- Is the post-action system state visible after async work?
- Are duplicate submissions prevented while pending?

## Anti-Patterns

- Toasts for errors that require user repair.
- Decorative animation with no state meaning.
- Motion that delays task completion.
- Hover-only feedback for critical actions.
- Success messages that do not show the next useful step.

## Recommendations It Should Produce

- Move repairable errors near the affected field or action.
- Add pending, success, and failure states to async actions.
- Use inline confirmation for saved or submitted states.
- Prevent duplicate submissions during pending states.
- Remove decorative motion unless it clarifies feedback or continuity.

## Dependencies

- `frameworks/workflow-analysis`
