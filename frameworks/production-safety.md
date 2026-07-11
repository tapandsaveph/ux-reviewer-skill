---
name: production-safety
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
  - frameworks/risk
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - production safety
  - audit
  - validation
  - permissions
  - ownership
  - tenant
  - soft delete
  - history
load_when:
  - The workflow touches auditability, permissions, tenant isolation, validation, ownership, approvals, deletion, compliance, or operational records.
avoid_when:
  - The review concerns only non-production concept copy or low-risk static presentation.
---

# Production Safety

## Problem This Solves

Ensures UX simplification does not remove controls that protect data integrity, accountability, permissions, or operational history.

## Load When

Load for admin tools, approvals, records, billing, healthcare, finance, tenant-aware apps, destructive actions, and operational workflows.

## Avoid When

Avoid only for low-risk presentation reviews with no data mutation, permissions, or operational consequence.

## Principles

- Simplicity must not remove audit logging, validation, permissions, ownership, approval controls, tenant isolation, or immutable history where required.
- Prefer soft delete or archive for business records.
- Validation belongs at trust boundaries and before irreversible actions.
- Reports should derive from operational data.

## Heuristics

- Is the actor authorized for the action?
- Is ownership visible and preserved?
- Is the action validated before mutation?
- Does the system retain enough history for accountability?
- Are tenant boundaries protected?
- Is deletion reversible or explicitly irreversible?

## Anti-Patterns

- Simplifying away approval steps that provide accountability.
- Hard-deleting business records without recovery or audit.
- Hidden permission failures.
- Cross-tenant data leakage through summaries, search, or filters.
- Reports that become unofficial write paths.

## Recommendations It Should Produce

- Preserve audit logs, permissions, ownership, and approvals.
- Add validation before data-changing actions.
- Use archive or soft delete where appropriate.
- Show safe permission-denied states.
- Keep reporting read-only and source-backed.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/risk`
