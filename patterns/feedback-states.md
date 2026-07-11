---
name: feedback-states
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/production-safety
conflicts_with: []
used_by:
  - skills/ux-implementer
keywords:
  - feedback
  - state
  - loading
  - saving
  - success
  - validation
  - pending
  - progress
load_when:
  - The interface needs loading, saving, validation, success, failure, retry, pending, progress, or status feedback.
avoid_when:
  - The interface is static documentation with no user action or system state.
---

# Feedback States

## Problem This Solves

Ensures users understand whether the system heard them, what is happening, and what they can safely do next.

## Load When

Load for forms, async actions, checkout, approvals, AI responses, uploads, settings saves, errors, permissions, and any state-changing workflow.

## Avoid When

Avoid for static content with no interaction or system state.

## Principles

- Every action needs acknowledgement.
- Feedback should be near the thing affected.
- Use persistent feedback for important outcomes and transient feedback only for low-risk confirmation.
- Users should never wonder whether data was saved, submitted, or lost.
- Progress should reflect meaningful workflow steps, not decorative motion.

## Heuristics

- What happens immediately after the primary action?
- Is there a pending state that prevents duplicate submission?
- Is success visible long enough to guide the next step?
- Are validation errors tied to the affected fields?
- Can users recover from failure without losing entered work?
- Are long-running tasks represented as queued, processing, complete, or failed?

## Anti-Patterns

- Silent saves.
- Spinners with no message or recovery path.
- Toast-only errors for form validation.
- Success messages that do not say what happens next.
- Losing user input after a failed submission.
- Decorative animation used as a substitute for status.

## Recommendations It Should Produce

- Define immediate, pending, success, validation, error, and retry states.
- Keep feedback close to the affected component.
- Preserve user input on failure.
- Prevent duplicate submissions during pending states.
- Use progress indicators only when they clarify waiting or completion.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/production-safety`
