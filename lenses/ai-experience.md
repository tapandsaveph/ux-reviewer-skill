---
name: ai-experience
version: 1.0.0
category: lens
depends_on:
  - frameworks/workflow-analysis
  - frameworks/risk
  - lenses/trust
conflicts_with: []
used_by:
  - skills/ux-reviewer
keywords:
  - AI
  - chat
  - assistant
  - model
  - prompt
  - citations
  - hallucination
  - tools
load_when:
  - Users configure, prompt, trust, review, cite, escalate, or act on AI-generated output or AI assistant behavior.
avoid_when:
  - AI is not part of the user-facing workflow or does not influence user decisions.
---

# AI Experience

## Problem This Solves

Helps reviews handle AI uncertainty, source trust, model/tool configuration, and human control without exposing raw AI implementation complexity.

## Load When

Load for AI chat, assistant onboarding, model/tool setup, prompt configuration, citations, generated recommendations, human escalation, or AI outputs users act on.

## Avoid When

Avoid when AI is only internal implementation detail and not visible to users or decision-making.

## Principles

- AI UX should clarify capability, limits, sources, and user control.
- Users need confidence boundaries before acting on AI output.
- Configuration should start from user outcomes, not model parameters.
- High-risk AI actions need review, permission, or escalation.

## Heuristics

- Does the user know what the assistant can and cannot do?
- Are sources, citations, or evidence visible when trust matters?
- Are uncertain outputs labeled with confidence, limits, or escalation?
- Are tool permissions and data access understandable?
- Are advanced model settings hidden behind outcome-based defaults?
- Can users correct, undo, or report bad output?

## Anti-Patterns

- Raw model parameters as primary setup choices for non-experts.
- AI answers users must trust without sources or boundaries.
- Hidden tool access or data permissions.
- Automation that acts without review in high-risk workflows.
- Empty chat screens with no task-oriented starting point.

## Recommendations It Should Produce

- Reframe setup around assistant goals and permitted actions.
- Show sources, limits, and escalation paths where decisions matter.
- Separate advanced model controls from outcome-based defaults.
- Preview tool/data permissions before enabling them.
- Add correction, feedback, undo, or human handoff paths.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/risk`
- `lenses/trust`
