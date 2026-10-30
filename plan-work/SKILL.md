---
name: plan-work
description: Use after requirements analysis to separate core and supporting capabilities, choose a minimum fitting framework, and decide whether independent work should be delegated or kept in one implementation flow.
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
6. Decide the implementation shape before delegating. Map every candidate workstream to its dependencies, shared files, stable interface, estimated implementation size, and integration cost.
   - Keep one implementation flow when the work is small, ordered, or likely to contend over the same model, route, configuration, screen, or test files.
   - Delegate only when at least two bounded workstreams can proceed independently after a shared contract is defined, and their expected time saving exceeds setup, handoff, and integration cost.
   - When isolated worktrees are available and permitted, use them only after a clean baseline commit exists. They isolate edits; they do not remove the need to integrate, test, and own the final result.
7. For parallel work, define one integration owner before starting. Give every delegated task: its goal and acceptance criteria, allowed files or directories, interface/input-output contract, dependencies, test command, and handoff format. Do not give multiple agents ownership of the same mutable file without an explicit sequencing plan.
   - For an algorithm-heavy task, separate exploration, complexity/edge-case design, or a stable solver module from application scaffolding; integrate only after the algorithm contract is agreed.
   - For a requirement-heavy application, split by independent feature or layer with separate directories and tests, not by adjacent endpoints or arbitrary CRUD verbs that share a model and route.
   - Use review as a focused post-integration pass unless it can inspect an independent artifact without blocking implementation.
8. Divide the resulting work into dependency-ordered milestones: project skeleton and verified run path, core end-to-end behavior, required supporting behavior, integration/output, tests and documentation, then final audit. For each, name files or components, intended behavior, acceptance criteria, verification, and owner.
9. Prioritize a working core slice before optional features or polish. Reserve explicit time for integration, tests, diff review, documentation, and submission. Update the plan when requirements or test evidence change.

## Output
- Capability map: core, supporting, optional, and out-of-scope work
- Framework and implementation approach, tied to the capability map
- Minimal architecture and data/execution flow
- Collaboration decision: single flow or delegated work, with rationale
- If delegated: ownership map, interfaces, integration owner, handoff checks, and merge/test order
- Ordered checklist with time budget, files/components, acceptance criteria, and verification per milestone
- Dependencies, integration order, risks, fallback plan, and stop conditions
- Explicit verification and submission time reserve

Keep the plan short enough to execute. Do not over-engineer or create files that the task does not need.
