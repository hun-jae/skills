---
name: plan-work
description: Use after requirements analysis to produce a small, ordered implementation plan with acceptance criteria, file ownership, dependencies, and a protected verification/submission window.
---

# Implementation Plan

## Procedure
1. Confirm the task goal, confirmed requirements, assumptions, constraints, and submission instructions.
2. Divide work into small milestones ordered by dependency: skeleton/inputs, core behavior, integration/output, tests, docs, final audit.
3. For each milestone define files to create/change, intended behavior, acceptance criteria, and how to verify it.
4. Prioritize the smallest end-to-end working result before optional features or polish.
5. If multiple agents are available and permitted, delegate only independent, bounded work with explicit file ownership and interface contracts. Keep one integration owner. Do not add agents just for the sake of parallelism.
6. Reserve explicit time for running tests, reviewing diffs, updating documents, and submitting. Never plan to use all available time for implementation.
7. Record decisions and update the plan when new stakeholder information or test results change the approach.

## Output
- Ordered checklist with time budget
- Files/components affected
- Acceptance criteria per milestone
- Dependencies and integration order
- Risks, fallback plan, and stop conditions
- Verification and submission time reserved

Keep the plan short enough to execute. Do not over-engineer or create files that the task does not need.
