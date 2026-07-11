---
name: engagement
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - engagement
  - momentum
  - progress
  - feedback
  - onboarding
  - motivation
  - continue
load_when:
  - The review needs to assess whether users feel useful momentum, progress, clarity, and confidence to continue.
avoid_when:
  - The recommendation would become decoration, gamification, or animation unrelated to task completion.
---

# Engagement

## Problem This Solves

Defines engagement as useful workflow momentum rather than visual excitement or decoration.

## Load When

Load for onboarding, activation, empty states, progress flows, repeated workflows, and reviews that mention engagement or user motivation.

## Avoid When

Avoid when engagement would distract from safety, completion, recovery, or workflow clarity.

## Principles

- Engagement means users understand where they are and what to do next.
- Users should feel progress through useful feedback and completed work.
- Safe momentum matters more than excitement.
- Low effort increases willingness to continue.

## Heuristics

- Is the user's location in the workflow clear?
- Does the user know what is done, current, and next?
- Do actions produce visible outcomes?
- Can users act without fear of hidden consequences?
- Does the system reduce typing, searching, and decision load?

## Anti-Patterns

- Gamification unrelated to the job.
- Animation used as excitement instead of feedback.
- Engagement metrics that conflict with task completion.
- Onboarding tours before first useful action.
- Feature marketing where task guidance is needed.

## Recommendations It Should Produce

- Add progress indicators for multi-step tasks.
- Use inline success and recovery messages.
- Surface the next best item in task queues.
- Use defaults and saved context to reduce repeated effort.
- Explain consequences before action with concise microcopy.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
