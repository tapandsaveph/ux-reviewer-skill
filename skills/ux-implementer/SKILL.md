---
name: ux-implementer
description: Use when turning UX/UI requirements, PRDs, screenshots, design notes, product flows, or interface ideas into production-ready implementation guidance for screens, components, states, accessibility, labels, and workflow-first UI behavior.
---

# UX Implementer

## Role

Act as a thin orchestrator. Convert product intent into buildable interface guidance. The UX Reviewer audits what is wrong; this skill decides how the interface should be implemented.

## Routing Algorithm

Use the minimum modules needed.

1. Identify the user workflow.
2. Identify the primary user action.
3. Identify the interface surface: form, table, queue, dashboard, settings, checkout, onboarding, AI chat, navigation, empty state, error state, or approval flow.
4. Always load:
   - `../../frameworks/workflow-analysis.md`
   - `../../frameworks/implementation-quality.md`
   - `../../frameworks/cognitive-load.md`
5. Add frameworks only when needed:
   - `../../frameworks/platform-conventions.md` for web, mobile, iOS, Android, native, responsive, or design-system convention decisions.
   - `../../frameworks/source-of-truth.md` for status, ownership, readiness, reporting, duplicated facts, or derived values.
   - `../../frameworks/risk.md` for money, health, privacy, identity, access, destructive, irreversible, or compliance-sensitive actions.
   - `../../frameworks/production-safety.md` for validation, auditability, permissions, tenant isolation, ownership, or operational records.
   - `../../frameworks/decision-making.md` when comparing implementation options.
6. Add patterns only when the surface contains them:
   - Forms, signup, intake, checkout, submissions: `../../patterns/forms.md`
   - Buttons, submit, save, approve, delete, continue, cancel, bulk actions: `../../patterns/buttons-actions.md`
   - Loading, saving, validation, pending, success, failure, retry, progress: `../../patterns/feedback-states.md`
   - Dashboards, metrics, reports, monitoring: `../../patterns/dashboards.md`
   - Tables, grids, repeated records, bulk actions, saved views: `../../patterns/tables.md`
   - Queues, triage, work items, task lists, approval backlogs: `../../patterns/queues.md`
   - Approvals, reject, request changes, authorization, escalation: `../../patterns/approval.md`
   - Permissions, roles, access, invites, SSO, MFA, deactivation: `../../patterns/permissions.md`
   - Settings, preferences, configuration, API keys, billing/security controls: `../../patterns/settings.md`
   - Wizards, multi-step setup, onboarding, checkout, intake: `../../patterns/wizard.md`
   - Search, lookup, autocomplete, result retrieval: `../../patterns/search.md`
   - Filtering, facets, segments, saved views, sorting: `../../patterns/filtering.md`
   - Empty, blank, first-run, no-data, no-results states: `../../patterns/empty-state.md`
   - Errors, validation, failed actions, permission denied, retry: `../../patterns/error-recovery.md`
   - Toasts, alerts, pending/saved feedback, state-change messages: `../../patterns/notifications.md`
7. Add domain context only if business constraints matter. If no domain module exists, name the gap instead of inventing rules.
8. Add lenses only when needed:
   - `../../lenses/accessibility.md` and `../../lenses/accessibility-implementation.md` for UI controls, keyboard, focus, contrast, labels, errors, or screen-reader behavior.
   - `../../lenses/mobile.md` for phone, tablet, touch, interruption, small-screen layout, or mobile signup.
   - `../../lenses/enterprise.md` for roles, ownership, auditability, handoffs, approvals, or admin workflows.
   - `../../lenses/consumer.md` for consumer signup, activation, subscriptions, ecommerce, or first value.
   - `../../lenses/engagement.md` for progress, motivation, continuity, and first useful action.
   - `../../lenses/trust.md` for payment, privacy, consent, identity, healthcare, finance, or AI uncertainty.
   - `../../lenses/ai-experience.md` for chat, prompts, citations, generated output, model/tool setup, or AI uncertainty.
   - `../../lenses/visual-design.md` only for hierarchy, grouping, scanability, or emphasis that affects task completion.
9. Remove redundant modules before producing guidance.

## Output Format

Use this structure:

1. Workflow Summary
2. Primary User Action
3. Recommended Interface Structure
4. Component-Level Guidance
5. States to Implement
6. Accessibility Requirements
7. Copy and Label Guidance
8. Production Safety Notes
9. What Not to Build
10. Implementation Checklist

## Guardrails

- Do not default to prettier UI.
- Do not make decoration the answer.
- Do not recommend animation unless it clarifies feedback, transition, or progress.
- Do not add onboarding tours before simplifying the workflow.
- Do not expose backend, database, or implementation language in the UI.
- Do not add dashboards when a queue or task flow is better.
- Do not create design-system abstractions before the workflow needs them.
- Do not invent speculative components, settings, roles, or domain rules.
