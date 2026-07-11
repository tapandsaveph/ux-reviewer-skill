---
name: filtering
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - filter
  - facet
  - segment
  - sort
  - view
  - saved filter
  - refine
load_when:
  - Users narrow, segment, sort, or save views over a visible set of records, metrics, or results.
avoid_when:
  - Users need query-based retrieval from an unknown set; use search instead.
---

# Filtering

## Problem This Solves

Lets users narrow known sets without losing context, creating confusing no-results states, or rebuilding the same view repeatedly.

## Load When

Load for tables, dashboards, queues, search results, analytics, saved views, facets, segments, date ranges, sorting, and scoped lists.

## Avoid When

Avoid when the workflow has no set to narrow or when query retrieval is the primary behavior.

## Principles

- Filters should match user decisions and common work modes.
- Active filters must be visible and removable.
- Defaults should reflect the user's role or repeated workflow.
- Saved views should reduce repeated setup without hiding scope.

## Heuristics

- Which filters change the user's next action?
- Are active filters visible near results?
- Can users clear, adjust, or save filter sets?
- Are empty results recoverable?
- Are date ranges, status values, and ownership filters understandable?
- Do defaults accidentally hide urgent work?

## Anti-Patterns

- Too many filters before users know the list.
- Hidden active filters causing missing records.
- Filter labels based on backend fields.
- Saved views with unclear scope.
- No-results states that do not show which filters caused the result.

## Recommendations It Should Produce

- Show active filters and clear actions.
- Prioritize filters tied to role, status, owner, date, risk, or next action.
- Add saved views for repeated workflows.
- Make empty-filter states recoverable.
- Replace technical filter labels with user-facing terms.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
