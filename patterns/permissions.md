---
name: permissions
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/production-safety
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - permissions
  - roles
  - access
  - admin
  - SSO
  - MFA
  - invite
  - deactivate
load_when:
  - Users grant, remove, inherit, review, or are blocked by access, roles, admin controls, SSO, MFA, or permission boundaries.
avoid_when:
  - The workflow has no authorization, access control, role, or permission state.
---

# Permissions

## Problem This Solves

Makes access control understandable and safe without exposing backend role models or leaking restricted data.

## Load When

Load for admin portals, role assignment, invites, deactivation, SSO, MFA, project access, permission denied states, or inherited access.

## Avoid When

Avoid when users are not managing or encountering access control.

## Principles

- Users should know what access a role grants before applying it.
- Permission changes need clear scope, consequence, and auditability.
- Denied states should explain next steps without leaking sensitive data.
- Use user-facing role names and examples, not internal IDs.

## Heuristics

- Who can view, edit, approve, administer, and audit?
- Is inherited access understandable?
- Does the UI preview what will change?
- Are dangerous access changes confirmed?
- Is deactivation separated from routine edits?
- Does permission denial name an owner or request path?

## Anti-Patterns

- Raw role IDs in user-facing UI.
- Generic "Update" for access changes.
- Bulk permission changes with no preview.
- Hidden disabled controls with no explanation.
- Permission errors that reveal restricted data.

## Recommendations It Should Produce

- Explain roles by capability and scope.
- Preview permission changes before applying.
- Separate destructive access actions.
- Add request-access or contact-owner paths.
- Preserve auditability for access changes.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/production-safety`
