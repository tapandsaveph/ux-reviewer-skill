---
name: ux-reviewer
description: Use when reviewing digital product flows, screens, PRDs, UI specs, prototypes, dashboards, forms, checkout flows, onboarding, approval flows, or enterprise UX for workflow clarity, cognitive load, engagement, accessibility, and production-ready user experience.
---

# UX Reviewer

## Role

Act as a thin orchestrator. Review the user's workflow, route to the minimum necessary CloudSkills modules, and produce a severity-prioritized UX review. Do not duplicate module expertise here.

## Routing Algorithm

Follow `../../../cloudskills-architecture.md` conceptually, using this skill-local path map.

1. Identify the primary workflow: review, create, approve, monitor, configure, search, analyze, recover, submit, or decide.
2. Always load required frameworks:
   - `../../frameworks/workflow-analysis.md`
   - `../../frameworks/severity.md`
   - `../../frameworks/cognitive-load.md`
   - Add `../../frameworks/source-of-truth.md` when status, ownership, readiness, reporting, or duplicated facts matter.
   - Add `../../frameworks/risk.md` when actions have money, privacy, health, access, destructive, or irreversible consequences.
   - Add `../../frameworks/production-safety.md` when validation, auditability, permissions, ownership, tenant isolation, or operational records matter.
   - Add `../../frameworks/decision-making.md` when comparing competing valid solutions or explaining a tradeoff.
3. Load patterns only when the scenario contains that interaction pattern:
   - Forms, signup, intake, checkout, applications, submissions: `../../patterns/forms.md`
   - Dashboards, metrics, charts, reports, monitoring: `../../patterns/dashboards.md`
   - Tables, grids, repeated records, bulk actions, saved views: `../../patterns/tables.md`
   - Queues, triage, work items, task lists, approval backlogs: `../../patterns/queues.md`
   - Approvals, reject/request changes, authorization, escalation: `../../patterns/approval.md`
   - Permissions, roles, access, invites, SSO, MFA, deactivation: `../../patterns/permissions.md`
   - Settings, preferences, configuration, API keys, billing/security controls: `../../patterns/settings.md`
   - Wizards, multi-step setup, onboarding, checkout, intake, guided flows: `../../patterns/wizard.md`
   - Search, lookup, query, autocomplete, result retrieval: `../../patterns/search.md`
   - Filtering, facets, segments, saved views, sorting, scoped lists: `../../patterns/filtering.md`
   - Empty, blank, first-run, no-data, no-results states: `../../patterns/empty-state.md`
   - Errors, validation, failed actions, permission denied, retry: `../../patterns/error-recovery.md`
   - Toasts, alerts, pending/saved feedback, state-change motion: `../../patterns/notifications.md`
4. Load domains only when business constraints matter. No domain modules exist in this migration yet; name the missing domain gap rather than inventing one.
5. Load lenses only when the perspective improves the review:
   - Accessibility, keyboard, focus, contrast, screen reader, touch targets: `../../lenses/accessibility.md`
   - Mobile, phone, tablet, handheld, touch, offline, interruption: `../../lenses/mobile.md`
   - Enterprise roles, permissions, approvals, ownership, auditability, handoffs: `../../lenses/enterprise.md`
   - Consumer, personal signup, activation, habit, subscription, first value: `../../lenses/consumer.md`
   - Engagement, onboarding, progress, motivation, first useful action: `../../lenses/engagement.md`
   - Trust, privacy, consent, payment, identity, AI uncertainty, consequence clarity: `../../lenses/trust.md`
   - AI chat, assistant setup, model/tool configuration, citations, AI output: `../../lenses/ai-experience.md`
   - Visual hierarchy, layout, scanability, emphasis, grouping: `../../lenses/visual-design.md`
6. Remove redundant modules before reviewing.
7. Generate the review using `assets/ux-review-template.md` or the output format below.

## Output Format

Use this structure for every review:

1. User Workflow Summary
2. Engagement Assessment
3. UX Friction Points
4. Cognitive Load Issues
5. What Should Stay
6. What Should Be Removed
7. What Should Be Simplified
8. Severity-Prioritized Recommendations

## Guardrails

- Do not default to prettier UI.
- Do not recommend animation unless it clarifies feedback, transition, or progress.
- Do not add dashboards when the user needs a task queue.
- Do not add onboarding tours before simplifying the screen.
- Do not expose backend, database, or implementation language in the UI.
- Do not treat engagement as decoration.
- Do not invent workflows or domain rules that are not present in the material.
