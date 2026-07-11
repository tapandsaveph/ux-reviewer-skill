---
name: dashboards
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with:
  - patterns/queues
used_by:
  - skills/ux-reviewer
keywords:
  - dashboard
  - chart
  - metrics
  - monitor
  - analytics
  - report
  - KPI
load_when:
  - Users monitor metrics, detect exceptions, compare performance, or drill into source records.
avoid_when:
  - Users primarily need a task queue or list of work to complete.
---

# Dashboards

## Problem This Solves

Separates monitoring and decision support from task execution so dashboards do not become cluttered work queues.

## Load When

Load when users monitor, compare, investigate, or drill into metrics and summaries.

## Avoid When

Avoid when the user needs to process actionable work items; use queue/table patterns instead when available.

## Principles

- Dashboards support decisions; they are not decoration.
- Each metric should change what the user does next.
- Derived metrics must be traceable to source records.
- Reports read from operational data and should not write source facts.

## Heuristics

- Is the user monitoring, deciding, investigating, or doing work?
- What metric changes the user's next action?
- Are urgent items visually and structurally prioritized?
- Can users filter to their responsibility, tenant, team, or status?
- Are charts more useful than a sorted list?
- Is there drill-down from summary to source record?

## Anti-Patterns

- Vanity metrics without a decision.
- Dense charts where a sorted queue would help more.
- Editable reporting surfaces.
- More cards added instead of clearer prioritization.
- Animation that makes charts feel lively without improving comprehension.

## Recommendations It Should Produce

- Replace dashboard surfaces with queues when the user needs to act.
- Keep monitoring summaries separate from work execution.
- Put status, owner, age, blocker, and next action before nice-to-have details.
- Add drill-down from metrics to source records.
- Remove metrics that do not support a decision.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
