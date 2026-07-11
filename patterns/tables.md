---
name: tables
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - table
  - grid
  - columns
  - rows
  - bulk actions
  - saved views
  - stale data
load_when:
  - Users scan, compare, sort, filter, edit, select, or act on repeated records in rows and columns.
avoid_when:
  - The workflow has only a single object, narrative content, or metric summary without row-level decisions.
---

# Tables

## Problem This Solves

Helps dense record views support scanning, comparison, row-level action, and safe bulk work.

## Load When

Load for operational grids, admin lists, logistics tables, account lists, inventory rows, editable tables, and bulk actions.

## Avoid When

Avoid when a queue, card list, dashboard, or detail page better matches the user's task.

## Principles

- Density is useful when users compare many records.
- Columns should match the user's decision, not all available data.
- Row actions should be close to the row they affect.
- Bulk actions need preview, scope, and recovery.
- Stale or delayed data should be visible.

## Heuristics

- Which columns are needed to choose the next action?
- Are status, owner, age, blocker, and next action visible?
- Are saved views or defaults aligned to common jobs?
- Are filters understandable and recoverable?
- Are bulk selections scoped and confirmed?
- Is last-updated or sync state important?

## Anti-Patterns

- Thirty-plus columns because data exists.
- Hidden row actions that slow repeated work.
- Bulk actions without preview or undo.
- Filters that create no-results confusion.
- Tables used where a guided queue is better.

## Recommendations It Should Produce

- Reduce default columns to decision-critical fields.
- Add saved views for common roles or tasks.
- Put row-level next actions near the row.
- Add bulk action preview and recovery.
- Show stale data, last updated, or partial sync states.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
