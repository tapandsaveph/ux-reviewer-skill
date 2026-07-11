---
name: settings
version: 1.0.0
category: pattern
depends_on:
  - frameworks/workflow-analysis
  - frameworks/risk
  - frameworks/source-of-truth
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - settings
  - preferences
  - configuration
  - admin settings
  - account settings
  - workspace settings
  - API keys
load_when:
  - Users configure account, workspace, billing, security, integrations, notifications, API keys, data export, or deletion behavior.
avoid_when:
  - The workflow is ordinary data entry, onboarding, or content editing rather than persistent configuration.
---

# Settings

## Problem This Solves

Keeps persistent configuration understandable, owned, and safe without turning settings into a junk drawer.

## Load When

Load for account settings, workspace settings, admin configuration, billing preferences, security controls, API keys, integrations, exports, deletion, and notifications.

## Avoid When

Avoid when users are completing a one-time form, editing a business record, or moving through a wizard that does not persist configuration.

## Principles

- Group settings by ownership, risk, and frequency.
- Separate personal, workspace, billing, security, and organization-level controls.
- Dangerous settings need clear consequence, permission, and recovery.
- Unsaved changes should be visible and recoverable.

## Heuristics

- Who owns this setting: user, workspace, organization, billing admin, or security admin?
- Is the change low-risk preference or high-risk configuration?
- Is the current value, pending change, and save state clear?
- Are dangerous actions isolated from routine edits?
- Does the user know who will be affected?
- Are settings discoverable without exposing backend structure?

## Anti-Patterns

- One long mixed page for profile, billing, security, integrations, API keys, and deletion.
- Technical names used as navigation labels.
- Destructive actions placed beside routine saves.
- Autosave with no visible saved/error state.
- Hidden role requirements for settings changes.

## Recommendations It Should Produce

- Group settings by owner and consequence.
- Separate dangerous actions into a clearly labeled area.
- Show unsaved, saved, failed, and permission-denied states.
- Clarify who is affected by a setting.
- Replace technical labels with user-facing configuration language.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/risk`
- `frameworks/source-of-truth`
