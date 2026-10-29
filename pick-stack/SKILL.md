---
name: pick-stack
description: Use after understanding the task to choose the minimum suitable language, framework, libraries, storage, and runtime based on the actual workspace and constraints.
---

# Framework and Technology Selection

## Principles
- Prefer the existing stack when it is viable; avoid rewrites and unnecessary dependencies.
- Optimize for task completion, reliability, testability, and time-to-verify—not novelty.
- Do not assume the task needs a web app, database, API, or UI. Select only what the requirements need.
- Respect the provided runtime, installed packages, network restrictions, permitted tools, and submission format.

## Procedure
1. Summarize the task's functional needs, runtime constraints, input/output shape, persistence needs, and verification needs.
2. Inspect existing manifests, lockfiles, configuration, examples, and installed tooling before recommending a stack.
3. Compare at most 2–3 realistic options using: fit, implementation time, reliability, testability, dependency/setup risk, and maintainability.
4. Recommend one default and state why it fits. Name the trade-off and what would make the alternative preferable.
5. Define the minimum architecture and interfaces needed. Keep component boundaries proportional to the task.
6. List setup/run/test commands only when verified from the repository or clearly label them as proposed.
7. Do not install packages or change configuration until the user/agent accepts the plan or the task clearly authorizes implementation.

## Output
- Recommended stack and evidence
- Alternatives and trade-offs
- Minimal architecture/data flow
- Required dependencies and environment assumptions
- Run/test approach
- Decisions that remain uncertain
