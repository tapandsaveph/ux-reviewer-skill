---
name: error-recovery
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/severity
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - error
  - failure
  - validation
  - retry
  - recovery
  - failed
  - permission denied
load_when:
  - Users encounter validation errors, failed actions, permission denials, partial failures, or recovery paths.
avoid_when:
  - There is no error, failed state, validation, or recovery path in the scenario.
---

# Error Recovery

## Problem This Solves

Helps users understand what went wrong, what it affects, and the safest next action.

## Load When

Load for validation, submission failures, payment failures, permission denial, async failure, partial save, retry, or support escalation.

## Avoid When

Avoid for happy-path-only reviews unless missing failure states are part of the critique.

## Principles

- Errors should be local, specific, and recoverable.
- Preserve user work after failures.
- Explain account, payment, approval, or access impact when relevant.
- Permission errors should explain why action is unavailable without leaking sensitive data.

## Heuristics

- Is the error placed near the field or action it affects?
- Does it explain what happened and how to recover?
- Can the user retry safely?
- Is partial completion or background processing visible?
- Is there a clear escalation path when self-recovery fails?
- Are destructive or irreversible failures guarded before they occur?

## Anti-Patterns

- Raw error codes in user-facing UI.
- Toasts for repairable or critical errors.
- Errors that clear user input.
- Retry actions that can duplicate submissions.
- Permission denials with no owner, reason, or next step.

## Recommendations It Should Produce

- Replace raw error text with user-facing recovery guidance.
- Move validation near affected fields.
- Preserve entered data and partial progress.
- Add safe retry, edit, support, or escalation paths.
- Show the state impact of failure and what happens next.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/severity`
