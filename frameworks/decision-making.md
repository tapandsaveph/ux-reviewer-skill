---
name: decision-making
version: 1.0.0
category: framework
depends_on:
  - frameworks/workflow-analysis
  - frameworks/severity
  - frameworks/cognitive-load
conflicts_with: []
used_by:
  - skills/ux-reviewer
  - skills/prd-reviewer
  - skills/system-architect
keywords:
  - decision
  - tradeoff
  - alternative
  - option
  - choose
  - compare
  - matrix
load_when:
  - A review must choose between competing valid solutions or justify why one approach is preferable.
avoid_when:
  - There is only one viable solution or the issue is a clear defect, missing state, broken workflow, or policy violation.
---

# Decision Making

## Problem This Solves

Helps orchestrators recommend one defensible option among multiple valid approaches using explicit criteria instead of preference.

## Load When

Load when comparing alternatives such as wizard vs one page, automation vs user control, dense table vs simplified view, configuration vs convention, dashboard vs queue, or general pattern vs specialized workflow.

## Avoid When

Avoid when the answer is already determined by a blocker, safety requirement, source-of-truth violation, accessibility failure, or missing feedback state.

## Principles

- Choose based on evidence from the workflow, user goal, risk, frequency, expertise, safety, and maintainability.
- Make the decision criteria visible before giving the recommendation.
- Prefer the simplest option that satisfies the workflow and safety constraints.
- Do not optimize for one dimension while hiding the tradeoff in another.

## Heuristics

- Is the workflow linear, branching, or exploratory?
- How often does the user perform this action?
- What is the cost of a mistake?
- Can users safely pause, undo, or recover?
- Does the option preserve context or split it?
- Does flexibility solve a current need or speculative variation?
- Are users expert operators or first-time/low-frequency users?
- Will the choice reduce maintenance burden or create long-term configuration debt?

Decision matrix:

- Frequent + low risk: optimize for speed and low friction.
- Frequent + high risk: optimize for safe defaults and fast review.
- Rare + low risk: keep discoverable; avoid heavy setup.
- Rare + high risk: add explanation, confirmation, audit, and recovery.
- High expertise: preserve density, shortcuts, and comparison context.
- Low expertise: reduce choices, guide sequencing, and explain consequences.

## Anti-Patterns

- Recommending a pattern because it is familiar, not because the workflow fits.
- Adding configuration for hypothetical future variation.
- Choosing automation when users need review, trust, or control.
- Splitting into steps when context comparison is more important than sequencing.
- Flattening into one screen when validation errors or risk make staged review safer.

## Recommendations It Should Produce

- State the decision criteria used.
- Compare the strongest two or three viable options.
- Recommend the option that best fits workflow frequency, risk, expertise, and maintainability.
- Name the tradeoff being accepted.
- Explain when the recommendation should change.

## Dependencies

- `frameworks/workflow-analysis`
- `frameworks/severity`
- `frameworks/cognitive-load`
