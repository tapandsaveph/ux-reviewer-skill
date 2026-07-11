---
name: enterprise
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/severity
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - enterprise
  - approval
  - audit
  - permissions
  - admin
  - owner
  - handoff
  - tenant
load_when:
  - Roles, permissions, approvals, ownership, auditability, handoffs, tenant isolation, or admin controls matter.
avoid_when:
  - The workflow is individual, low-risk, and has no role, approval, permission, or audit concern.
---

# Enterprise

## Problem This Solves

Applies accountability, ownership, permission, approval, and audit expectations without making routine work unnecessarily painful.

## Load When

Load for admin portals, B2B workflows, approvals, permissions, enterprise settings, audit trails, handoffs, and tenant-aware systems.

## Avoid When

Avoid for simple consumer flows with no role, approval, permission, or audit requirement.

## Principles

- Protect accountability without hiding the next action.
- Show owner, status, blocker, due date, and next approver when relevant.
- Preserve auditability, permissions, ownership, and tenant boundaries.
- Use explicit approvals with clear consequences.
- Derive readiness from source requirements instead of duplicating status flags.

## Heuristics

- Who owns the record, decision, approval, and next step?
- Are permissions clear in the UI?
- Are approval states explicit and auditable?
- Are irreversible actions guarded?
- Is history append-only where required?
- Can users understand blockers without seeing data they should not access?
- Does the workflow support handoffs between roles?

## Anti-Patterns

- Hidden permission failures.
- Generic admin actions without accountability.
- Backend enum labels in user-facing UI.
- Duplicated status fields for convenience.
- Audit history mixed into the primary task path when it is not needed.

## Recommendations It Should Produce

- Show owner, status, due date, blocker, and next approver.
- Keep audit history separate from the task flow but easy to inspect.
- Replace generic update actions with explicit approval/reject/request-changes actions.
- Prefer archive or soft delete for business records.
- Preserve tenant isolation and permission boundaries in recommendations.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/severity`
