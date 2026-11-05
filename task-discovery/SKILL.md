---
name: task-discovery
description: "Use as the user-facing coordinator for a software task: inspect the workspace and requirements, obtain design approval, select a safe session plan, and coordinate integration without duplicating specialist Skills."
---

# Task Discovery and Session Coordination

## Role and boundaries

This is one of the two user-facing Skills in this pack, alongside `git-setting`. It coordinates existing specialist Skills; do not reimplement their analyses or checklists. Route work to them when their trigger applies:

- `map-project` for an unfamiliar workspace and execution flow
- `ask-requirements` for ambiguous briefs
- `pick-stack` for technology choices
- `plan-work` for milestones, ownership, and integration order
- `review-logic`, `verify-tests`, `work-notes`, `check-submit`, and `explain-work` at their respective stages

Start by reading the repository README and the task brief. State confirmed facts, assumptions, unknowns, constraints, and the smallest useful delivery before proposing implementation.

## Approval gate

Before any implementation, present every applicable item below to the user and obtain explicit approval. For each item, offer viable alternatives, their advantages and disadvantages, and a recommendation:

1. Major edge cases and the exception-handling policy.
2. Any complex algorithm and the core implementation design.
3. API contracts, database schema, and shared interfaces.
4. Per-session file ownership and the integration method.

Do not infer approval from silence, a new message, or partial feedback. Record approval, rejection, or deferral with `work-notes`. If a topic does not apply, explain why it is not applicable. Requirements questions remain open until the user answers or explicitly authorizes an assumption.

## Choose the session shape after approval

Use parallel sessions only for independent, bounded units where their time benefit exceeds setup, handoff, and integration cost. Keep a small task in one flow when work shares a core abstraction or the work is mostly sequential.

| Situation | Default ownership |
| --- | --- |
| Small CRUD | One Fullstack session |
| Typical web service | Backend + Frontend |
| Complex algorithm | Backend + Frontend + Core Logic |
| AI service | Backend + AI/RAG + Frontend |

These are starting points, not quotas. Merge roles when their files or interfaces are tightly coupled; split only after the interface and file ownership are approved.

## User-led parallel execution

The main session owns discovery, approvals, worktree setup, integration, and final verification. It must not silently create or run hidden implementation agents.

After confirming a clean base commit and approved ownership, create one branch and worktree for each independent role. Give the user an exact command and a role-specific prompt for each terminal, using this form with actual values substituted:

```powershell
cd <absolute-worktree-path>
codex "You are the <role> implementer. Work only on: <owned files>. Follow approved decisions: <decisions>. Do not edit shared files or other owners' files. Run: <role tests>. If you find a material design issue, stop and report it to the main session without expanding scope."
```

Workers may implement autonomously only inside their approved scope. A newly discovered material design issue, interface change, or ownership conflict is a stop-and-report event for the main session; it requires a new user approval before work continues.

## Git and integration safety

Preserve existing branches and uncommitted work. Create parallel worktrees only from a verified clean base commit, use separate branches, and assign every editable file to exactly one session. The integration owner reviews each branch, resolves only approved interface changes, runs the agreed checks, and records actual results.

Never push, merge into `main`, or delete a branch/worktree without explicit user approval. Treat a request to implement as separate from authorization to publish or merge.
