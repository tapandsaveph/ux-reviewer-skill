---
name: wizard
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - wizard
  - multi-step
  - stepper
  - onboarding
  - setup
  - guided flow
  - progress
load_when:
  - A workflow is intentionally split into ordered steps for setup, signup, onboarding, intake, checkout, or review.
avoid_when:
  - Steps merely hide unnecessary fields or the task can be completed safely on one clear screen.
---

# Wizard

## Problem This Solves

Ensures multi-step flows reduce complexity instead of hiding clutter or delaying the first useful action.

## Load When

Load for setup flows, onboarding, checkout, intake, applications, progressive configuration, and guided review/confirmation sequences.

## Avoid When

Avoid when a wizard is proposed only to make an overlong form feel shorter without changing what users must decide.

## Principles

- Each step should map to a real user decision.
- Progress should show current, completed, and remaining work.
- Users should be able to recover, go back, and preserve entered data.
- Optional setup should be deferred until after first value when safe.

## Heuristics

- Does each step have a distinct purpose?
- Is the next step predictable before the user advances?
- Are dependencies between steps visible?
- Can users save, resume, or go back without data loss?
- Is review/confirm used only when consequence warrants it?
- Does the flow reach first value quickly?

## Anti-Patterns

- Splitting one noisy form into arbitrary pages.
- Progress indicators with unclear completion.
- Forced tours before productive action.
- Hidden validation saved until the final step.
- Steps users cannot revisit or correct.

## Recommendations It Should Produce

- Make each step represent a clear decision.
- Move eligibility or blocking checks earlier.
- Defer optional setup until after first useful outcome.
- Add save/resume and back behavior where needed.
- Use review/confirm for high-consequence submissions.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
