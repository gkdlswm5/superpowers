---
name: test-driven-development
description: Use when implementing behavior changes or bug fixes whose correctness benefits from an executable regression test, or when the user explicitly requests test-first development.
---

# Test-Driven Development

Use a failing behavior test to establish the defect or missing capability, make the smallest justified implementation change, then improve structure while keeping the behavior green.

## Scope and authorization

Choose relevant tests at established public interfaces within the approved task. No separate permission is needed to select a test boundary, run local checks, fix failures caused by the change, or rerun affected tests. Ask when the expected business behavior or a consequential interface decision is genuinely unresolved.

For documentation, formatting, configuration, generated output, and disposable prototypes, use checks proportionate to the risk rather than requiring a new unit test or permission to skip one. Configuration that controls side effects may warrant a regression test. Honor an explicit user or project requirement for test-first work.

This skill does not authorize commits, pushes, publishing, destructive operations, or unrelated fixes. Follow the user's approval policy and runtime/tool requirements.

## Red, green, refactor

1. **Red:** Write one test for externally observable behavior. Derive the expected result from the requirement, a worked example, or another independent source. Run it and verify it fails for the intended reason; fix fixture/setup errors before treating a failure as evidence.
2. **Green:** Implement only enough behavior to satisfy the requirement. Run the new test and relevant existing checks. Diagnose failures rather than weakening assertions to match incorrect output.
3. **Refactor:** Improve local structure if useful while preserving behavior. Keep refactoring in scope and rerun affected tests. Larger architectural changes require their own scope decision.

Work in small vertical slices. Do not prewrite a large suite against imagined internals. Prefer public interfaces and real collaborators when practical; mock external boundaries where needed to keep tests deterministic and safe.

## Test quality

- A regression test must fail on the defective behavior, not merely confirm that code ran.
- Avoid assertions that recalculate the expected result using the same implementation.
- Avoid excessive mocking of internal methods or assertions tied to incidental call order.
- Use isolated fixtures; tests must not modify live user data or contact production services unless that work is explicitly authorized.
- Existing uncommitted work belongs to the user. Do not delete it to manufacture a test-first history. Add a regression test and report honestly if red-before-green was not observed.

See testing-anti-patterns.md for detailed examples when test design is difficult. The optional tdd skill provides complementary public-interface and mocking examples; it does not add a separate approval or refactoring policy.

## Completion

Report the relevant checks and results, including what was not tested. After they pass, broaden or repeat testing only for new changes, failures, or unresolved concerns. Passing tests are evidence for the checked behavior, not proof of every possible case.
