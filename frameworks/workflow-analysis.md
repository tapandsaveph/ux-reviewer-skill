---
name: workflow-analysis
version: 1.0.0
category: framework
depends_on: []
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - workflow
  - task
  - trigger
  - goal
  - source of truth
  - status
  - blocker
load_when:
  - Any review needs to identify the real-world process, user goal, trigger, decision, or business outcome.
avoid_when:
  - Never avoid for ux-reviewer; it is a required framework.
---

# Workflow Analysis

## Problem This Solves

Prevents reviews from starting with screens, entities, or aesthetics before understanding the real work being automated.

## Load When

Load for every UX review, PRD review, system review, or workflow critique.

## Avoid When

Do not avoid for `ux-reviewer`.

## Principles

- Start with the manual process.
- Review the workflow, not the database shape.
- Every screen should support a task, decision, handoff, or recovery path.
- Important status, ownership, and completion facts need a clear source of truth.

## Heuristics

- Identify who performs the work, what triggers it, what information they need, what decision they make, and what happens next.
- Ask what business outcome the workflow produces.
- Check whether the user can answer: where am I, why am I here, what should I do next, what blocks me, and what happens after I act?
- Check whether the primary action matches the user's current job.
- Treat status, owner, blocker, due date, and next action as task-critical facts.
- Prefer queues for work to be done and dashboards for monitoring.
- Reports should read from operational data, not ask users to re-enter facts.

## Anti-Patterns

- Screen maps to a database table instead of a task.
- Multiple routes complete the same work.
- Users must navigate elsewhere to answer a simple status or blocker question.
- Backend terms appear in user-facing labels.
- Readiness, blocker, or completion flags duplicate facts that can be derived.

## Recommendations It Should Produce

- Reframe screens around the user's job, trigger, decision, and next step.
- Move blockers and consequences next to the affected action.
- Replace duplicate paths with one guided workflow.
- Derive summary status from source records where possible.
- Preserve existing safety controls, auditability, ownership, and permissions.

## Dependencies

None.
