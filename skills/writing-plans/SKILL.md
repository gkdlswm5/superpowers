---
name: writing-plans
description: Use when a user requests an implementation plan or an approved complex change needs a durable sequence of implementation and verification steps.
---

# Writing Plans

Write enough detail for someone to implement and verify the agreed result without rediscovering the important decisions. A simple scoped edit needs a brief plan, not a separate planning ceremony.

## Plan contents

- State the goal, scope boundaries, and decisions already approved.
- Identify files or modules to change and the responsibility of each.
- Sequence dependent work; identify independent tasks only when coordination would help.
- Give the relevant interfaces, business rules, inputs, and acceptance checks.
- Use exact commands and expected outcomes where known. Distinguish unresolved decisions from ordinary implementation choices.
- Include code examples when they resolve ambiguity. Do not prewrite the entire implementation merely to satisfy a plan template.

Keep units cohesive and use existing project patterns. Do not add an architectural split solely because planning touches a large file. Tests should observe public behavior using independent expected results. Use test-driven development for meaningful logic changes and risk-appropriate checks for documentation, configuration, or disposable prototypes.

Save a durable plan only when requested or useful for substantial work. Follow the project's convention; otherwise use docs/superpowers/plans/YYYY-MM-DD-<feature-name>.md. A useful shape is: Goal, Constraints, Tasks, Verification, Open decisions.

## Review and execution

Check coverage, interface consistency, scope, and verification before implementation. Resolve routine omissions directly. Ask only about decisions that materially change behavior, scope, or authorization.

If the user asked for a plan only, deliver it without implementing. If the user already approved implementation, continue without another execution-mode choice. Choose available tools within the user's and runtime's delegation rules; do not mandate unavailable sub-skills.

Commit, push, or publish only when explicitly authorized. Do not insert automatic commit steps into plans. When Git work is requested, follow the user's repository and commit-message conventions.
