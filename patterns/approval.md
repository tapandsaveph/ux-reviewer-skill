---
name: approval
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/severity
  - frameworks/production-safety
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - approval
  - approve
  - reject
  - review
  - request changes
  - escalation
  - approver
load_when:
  - A user accepts, rejects, authorizes, escalates, delegates, or requests changes in a workflow.
avoid_when:
  - The workflow has no decision authority, handoff, approval status, or accountability requirement.
---

# Approval

## Problem This Solves

Makes decision authority, handoff, consequence, and auditability clear in approval workflows.

## Load When

Load for manager review, finance/legal/vendor approvals, content moderation, authorization, request changes, escalation, or delegation.

## Avoid When

Avoid for simple submissions where no separate approver or decision authority exists.

## Principles

- The approver must know what they are approving and the consequence.
- Submitters should know who owns the next step.
- Approval status should be source-backed and auditable.
- Reject/request-changes paths need clear recovery.

## Heuristics

- Who is the current approver?
- What evidence or requirement must be reviewed?
- What happens after approve, reject, hold, or request changes?
- Is the decision immutable, reversible, or editable?
- Is audit history visible without crowding the task?
- Are SLA, due date, or escalation relevant?

## Anti-Patterns

- Generic "Update" buttons for approval decisions.
- Backend approval enum labels.
- No visible next approver or owner.
- Reject states with no correction path.
- Approval actions mixed with routine edits.

## Recommendations It Should Produce

- Use explicit approve, reject, hold, and request-changes actions.
- Show current owner, next approver, due date, and blocker.
- Explain consequences before decision.
- Keep audit trail inspectable.
- Provide recovery path after rejection or changes requested.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/severity`
- `frameworks/production-safety`
