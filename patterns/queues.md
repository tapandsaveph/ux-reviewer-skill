---
name: queues
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with:
  - patterns/dashboards
used_by:
  - skills/ux-reviewer
keywords:
  - queue
  - task list
  - triage
  - work items
  - next action
  - backlog
  - priority
load_when:
  - Users need to process, triage, prioritize, assign, or complete a list of work items.
avoid_when:
  - Users are monitoring aggregate metrics or investigating trends rather than doing item-level work.
---

# Queues

## Problem This Solves

Turns operational work into an ordered, actionable list instead of forcing users to hunt through dashboards or navigation.

## Load When

Load for task queues, approval queues, support queues, customer success triage, inventory exceptions, review backlogs, and work assignment.

## Avoid When

Avoid when the user only needs aggregate monitoring or historical reporting.

## Principles

- Queues are for work to be done.
- Items should be ordered by urgency, risk, SLA, blocker, or user responsibility.
- Each item should expose status, owner, age, blocker, and next action.
- Users should be able to filter to their responsibility without losing context.

## Heuristics

- What item should the user handle first?
- Why is each item in the queue?
- What action resolves or advances the item?
- Can users see blocked, overdue, assigned, and unassigned work?
- Can users complete repeated work without opening every detail page?
- Is the queue source-backed rather than manually maintained?

## Anti-Patterns

- Dashboard cards used as a substitute for actionable work.
- Equal priority for every item.
- Missing owner, blocker, or next action.
- Queues that require manual status updates duplicating source facts.
- Filters users must rebuild every day.

## Recommendations It Should Produce

- Replace dashboard clutter with an actionable queue when work needs doing.
- Sort by urgency, SLA, risk, or blocker.
- Show owner, status, age, blocker, and next action.
- Add role-based default views.
- Derive queue membership from source records.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
