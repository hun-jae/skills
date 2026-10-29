---
name: ask-requirements
description: Use when a task brief or requirements files are ambiguous and you need to separate confirmed requirements from assumptions and prepare high-value questions for a business/task-owner role.
---

# Requirements Analysis and Stakeholder Questions

## Procedure
1. Read the task statement and all clearly relevant provided instructions before asking questions.
2. Build three lists: **confirmed requirements**, **inferences/assumptions**, and **unknowns**. Cite the exact task text or file path supporting confirmed items.
3. Identify the user/persona, current workflow, pain point, desired outcome, inputs, outputs, constraints, edge cases, and success criteria. Mark missing information rather than inventing it.
4. If a task-owner AI/persona is available and the rules allow questions, draft a short prioritized set of questions. Ask only questions not already answered by the materials.
5. Prioritize questions whose answers may change scope, business rules, data interpretation, safety, acceptance criteria, or architecture. Avoid vague questions such as “What should I build?”
6. For each question include: exact question, why it matters, what decision it changes, and risk if unanswered.
7. Ask questions in small batches; incorporate answers into the requirements and revise the plan. Do not fabricate answers from the stakeholder.
8. If no stakeholder channel exists, proceed with explicit assumptions and choose reversible, low-risk defaults.

## Output
- Problem statement in 1–3 sentences
- Confirmed / inferred / unknown requirements table
- Prioritized stakeholder questions (usually 3–7 maximum)
- Acceptance criteria that can be tested
- Risks and assumptions requiring validation

Do not start implementation until the main scope-changing unknowns are resolved or explicitly recorded as assumptions.
