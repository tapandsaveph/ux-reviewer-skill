---
name: empty-state
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - empty state
  - blank
  - no data
  - first run
  - onboarding
  - create first
load_when:
  - A screen has no records, no configured data, first-run content, or an initial state before work exists.
avoid_when:
  - The user already has meaningful content and the issue is not about missing or initial data.
---

# Empty State

## Problem This Solves

Turns blank or first-run screens into a clear next step without adding onboarding tours or decorative filler.

## Load When

Load for new workspaces, blank tables, no-results pages, first-run product states, or screens without configured data.

## Avoid When

Avoid when the workflow has existing data and the issue is about filtering, dashboards, tables, or navigation.

## Principles

- Empty states should explain what belongs here and what to do next.
- The primary action should create or import the first useful object.
- Empty states should reduce uncertainty, not market features.
- Do not add tours before making the first productive action obvious.

## Heuristics

- Does the empty state say why the screen is empty?
- Is there one obvious primary action?
- Are import, template, or sample options secondary?
- Does the user know what happens after they act?
- Does a no-results state help users adjust search or filters?

## Anti-Patterns

- Blank tables with filters but no explanation.
- Multiple equal-weight first actions.
- Feature descriptions instead of task guidance.
- Empty dashboards that hide the first useful workflow.
- Onboarding slides that delay the first value.

## Recommendations It Should Produce

- Add a clear first productive action.
- Explain what belongs on the screen in user language.
- Make import/template/sample paths secondary.
- Show no-results recovery for search or filter states.
- Remove feature-tour content that delays useful work.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
