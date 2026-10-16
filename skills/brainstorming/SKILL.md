---
name: brainstorming
description: Use when the user asks to explore a design or when consequential product, architecture, or behavior choices remain unresolved before implementation.
---

# Brainstorming Ideas Into Designs

Turn an unresolved idea into an actionable design. A clear, scoped edit or an already approved design does not need a new brainstorming cycle.

## Establish what needs deciding

Read the relevant project context and existing decisions. Identify what is still unknown and whether different answers would materially change the result. Make routine, reversible implementation choices yourself.

Ask focused questions only about consequential unknowns. Batch related questions when that reduces back-and-forth. Compare alternatives only when there are meaningful tradeoffs; do not invent multiple approaches for an obvious fix.

## Present a concrete design

Explain the proposed behavior, boundaries, important interfaces, data flow, and relevant checks. Scale detail to the work. Follow existing project patterns and keep unrelated refactoring out of scope. Decompose large independent systems only when that makes the design reviewable.

Use a visual when the user requested one or it clarifies a real visual choice. Follow the user's presentation preferences; do not add a separate visual-companion approval gate to an authorized preview. Read visual-companion.md only if using that optional browser companion.

## Approval and follow-through

Follow the user's global approval policy. Ask for a decision when a material design choice remains unresolved or the proposal expands scope. A prior approval covers the agreed design; do not seek section-by-section approval and then a second approval of the same written spec.

When the request is only to compare designs, present the comparison and wait for the user's selection before applying a design. When implementation is already authorized and decisions are settled, continue.

For substantial designs, save a concise spec in the project's established location (default: docs/superpowers/specs/YYYY-MM-DD-<topic>-design.md). Check it for contradictions, missing decisions, and scope drift. Saving a spec does not authorize a commit or push.

Use writing-plans if a durable implementation plan will help. Otherwise proceed with the scoped work. Do not require a particular execution skill or subagent mode when it is unavailable or unnecessary.
