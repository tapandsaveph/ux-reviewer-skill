---
name: forms
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - form
  - signup
  - intake
  - application
  - submit
  - fields
  - validation
load_when:
  - Users enter, edit, validate, review, or submit structured information.
avoid_when:
  - The workflow is read-only monitoring, browsing, or analysis without data entry.
---

# Forms

## Problem This Solves

Ensures forms collect only what is needed for the current workflow step and protect users from rework or unsafe submission.

## Load When

Load for signup, intake, checkout, applications, settings edits, submissions, and any structured data-entry workflow.

## Avoid When

Avoid when the surface is only a dashboard, queue, table, or read-only report.

## Principles

- Collect only what is needed now.
- Put fields in the order users think about the decision.
- Group fields by task, not database table.
- Validate early enough to prevent rework.
- Preserve user-entered data after errors.

## Heuristics

- Is every field necessary now?
- Can any field be defaulted, inferred, imported, or deferred?
- Are required fields obvious without visual noise?
- Are labels written in user language?
- Are examples shown for ambiguous formats?
- Can keyboard and assistive tech users complete the form?
- Is submission protected against duplicate clicks and data loss?

## Anti-Patterns

- Multi-step forms that only hide unnecessary fields.
- Optional fields that are really reporting wants.
- Confirmation modals for every low-risk submission.
- Validation that appears only after submit.
- Errors that clear fields or appear far from the affected input.

## Recommendations It Should Produce

- Remove, defer, default, infer, or import unnecessary fields.
- Add inline validation for fixable errors.
- Add review screens for high-risk submissions.
- Preserve entered data after errors.
- Clarify what happens after submit.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
