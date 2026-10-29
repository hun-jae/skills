---
name: ask-requirements
description: Use when a task brief is ambiguous and you need collaboration-ready stakeholder questions that clarify product scope, business rules, and only the technical constraints that affect delivery.
---

# Collaborative Requirements Discovery

## Principle

Start with the work people need to accomplish, not the technology that might implement it. Technical questions are valuable only when their answers affect scope, feasibility, integration, security, or acceptance. Treat the task owner as a collaborator: make uncertainty and its consequence visible, then ask the smallest useful batch of questions.

## Procedure
1. Read the task statement and clearly relevant artifacts before asking anything. Separate **confirmed requirements**, **inferences**, and **unknowns**; cite the source for confirmed items.
2. Build a shared problem view: stakeholder or user, current workflow, pain point, desired outcome, inputs and outputs, business rules, lifecycle, exceptions, and how success will be observed.
3. Identify the **core outcome** that must work for the task to be useful, then distinguish supporting capabilities, nice-to-haves, and explicitly out-of-scope work. Do not infer product policy from an example.
4. Draft product and collaboration questions first. Prefer questions about users, priorities, decision rules, ownership, data meaning, exceptional cases, acceptance, and handoff. Do not ask questions already answered by the materials.
5. Add only technical questions that are genuinely decision-changing: existing runtime or repository constraints, required integrations, persistence or data ownership, security/privacy requirements, deployment environment, and non-functional constraints. Avoid asking the stakeholder to choose a framework unless that is their decision.
6. Prioritize questions that can change scope, business rules, data interpretation, safety, acceptance criteria, or delivery architecture. Ask a small batch rather than a long questionnaire.
7. For each question state the exact question, why it matters, the decision it unlocks, and the risk if unanswered. Group questions by topic when that makes the collaboration easier.
8. Incorporate answers into the requirements and revise assumptions. If no stakeholder channel exists, record explicit, reversible defaults and flag decisions that still need validation.

## Output
- Problem statement in 1–3 sentences
- Confirmed / inferred / unknown requirements table
- Core outcome, supporting capabilities, and scope boundaries
- Prioritized stakeholder questions (usually 3–7 maximum), with rationale, decision, and risk
- Acceptance criteria that can be tested
- Risks and assumptions requiring validation

Do not start implementation until scope-changing unknowns are resolved or explicitly recorded as assumptions. Keep technical design provisional until the product and delivery constraints justify it.
