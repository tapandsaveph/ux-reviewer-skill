---
name: search
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - search
  - query
  - find
  - lookup
  - results
  - autocomplete
  - no results
load_when:
  - Users need to retrieve known or unknown items by query, lookup, global search, autocomplete, or result ranking.
avoid_when:
  - Users are narrowing a visible set with structured facets only; use filtering instead.
---

# Search

## Problem This Solves

Helps users retrieve the right object, record, or answer quickly when navigation or scanning is insufficient.

## Load When

Load for global search, record lookup, command search, autocomplete, result pages, no-results states, and query-based retrieval.

## Avoid When

Avoid when the user is only applying structured filters to an already visible list.

## Principles

- Search should match the user's mental model and vocabulary.
- Results should make selection confidence high.
- No-results states should help users recover.
- Search scope should be clear.

## Heuristics

- What does the user expect to find?
- Is the searchable scope visible?
- Are result titles, type, status, owner, and context enough to choose?
- Are typos, synonyms, IDs, and partial matches handled?
- Does no-results explain how to adjust the query?
- Is recent or frequent retrieval supported when useful?

## Anti-Patterns

- Search box with unclear scope.
- Results that show names without enough context to choose safely.
- No-results dead ends.
- Search used to compensate for broken navigation.
- Technical identifiers required when users know human labels.

## Recommendations It Should Produce

- Clarify search scope and accepted query types.
- Add context to results so users can choose confidently.
- Provide no-results recovery suggestions.
- Support common synonyms, IDs, and partial matches where relevant.
- Preserve recent searches or frequent targets when they speed repeated work.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
