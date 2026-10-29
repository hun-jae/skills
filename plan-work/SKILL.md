---
name: plan-work
description: Use after requirements analysis to separate core and supporting capabilities, recommend the minimum fitting framework, and produce an ordered implementation plan with verification time.
---

# Capability-Led Implementation Plan

## Principle

Plan from user value outward. Explain what the smallest useful result does before selecting technology. Use the capabilities and constraints to justify the framework and architecture; do not let a preferred stack create extra scope.

## Procedure
1. Confirm the goal, requirements, assumptions, constraints, existing workspace, and submission instructions. Revisit unanswered scope-changing questions before planning implementation.
2. Classify capabilities by value and dependency:
   - **Core capabilities:** the smallest end-to-end behavior that solves the primary user problem. For each, explain the user outcome, trigger/input, business rule, output, and acceptance check.
   - **Supporting capabilities:** validation, error handling, administration, documentation, observability, polish, and other work that makes the core safe or usable. Mark each as required, conditional, or optional.
   - **Out of scope:** requested or tempting work that is not needed for the agreed result.
3. Translate the core and required supporting capabilities into technical needs: runtime, interface type, data model and persistence, integrations, validation, testability, and operational constraints.
4. Inspect the existing stack first. If a framework choice is still needed, recommend the minimum viable framework, libraries, storage, and test tooling. State the evidence, why each choice supports the capabilities, and the trade-off. Use `pick-stack` for a deeper comparison when the choice is genuinely contested or high impact.
5. Define the smallest architecture and execution/data flow that supports the plan. Keep interfaces and component boundaries proportional to the work.
6. Divide the implementation into dependency-ordered milestones: project skeleton and verified run path, core end-to-end behavior, required supporting behavior, integration/output, tests and documentation, then final audit. For each, name files or components, intended behavior, acceptance criteria, and verification.
7. Prioritize a working core slice before optional features or polish. If multiple agents are available and permitted, delegate only independent bounded work with explicit ownership and interface contracts; keep one integration owner.
8. Reserve explicit time for tests, diff review, documentation, and submission. Update the plan when requirements or test evidence change.

## Output
- Capability map: core, supporting, optional, and out-of-scope work
- Framework and implementation approach, tied to the capability map
- Minimal architecture and data/execution flow
- Ordered checklist with time budget, files/components, acceptance criteria, and verification per milestone
- Dependencies, integration order, risks, fallback plan, and stop conditions
- Explicit verification and submission time reserve

Keep the plan short enough to execute. Do not over-engineer or create files that the task does not need.
