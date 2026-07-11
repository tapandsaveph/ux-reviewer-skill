---
name: consumer
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - consumer
  - personal
  - signup
  - onboarding
  - habit
  - individual user
  - activation
load_when:
  - The workflow is for individual consumers, personal accounts, first-time use, activation, subscriptions, or habit-forming product use.
avoid_when:
  - The workflow is primarily internal, enterprise, admin, role-based, or operational B2B work.
---

# Consumer

## Problem This Solves

Keeps consumer UX reviews focused on first value, personal motivation, consent timing, and low-effort continuation without turning engagement into decoration.

## Load When

Load for consumer onboarding, signup, subscriptions, personal settings, habit apps, trials, individual account flows, and activation moments.

## Avoid When

Avoid for enterprise, admin, or operational workflows where role/accountability constraints dominate.

## Principles

- First value should arrive before optional personalization or sharing.
- Personal motivation should be supported by useful progress, not gimmicks.
- Consent and permissions should be timely and specific.
- Consumer flows should make exit, skip, and later completion understandable.

## Heuristics

- What is the first useful outcome for this individual?
- Are optional preferences, invites, themes, or marketing choices deferred?
- Does signup ask for only what is needed to begin?
- Can users skip nonessential steps without penalty?
- Are subscription, trial, notification, or data-use consequences clear?
- Does the workflow respect users who are uncertain or exploring?

## Anti-Patterns

- Feature tours before the first useful action.
- Friend invites, notification prompts, or personalization before value.
- Forced account creation before the user understands the product.
- Engagement mechanics that slow completion.
- Hidden subscription or trial consequences.

## Recommendations It Should Produce

- Move first useful action earlier.
- Defer optional preferences, invites, and personalization.
- Make skip/later paths explicit.
- Explain trial, subscription, notification, or data-use consequences at decision points.
- Use progress cues that reflect real completed work.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/cognitive-load`
