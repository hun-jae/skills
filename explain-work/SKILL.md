---
name: explain-work
description: "Use before final submission to turn the actual task artifacts into the information the user must be able to verify and explain: changes, decisions, tests, operational behavior, and limitations."
---

# 내가 꼭 확인할 정보들

## Procedure
1. Read the current task brief, implementation, actual diffs, plan/collaboration notes, and verification evidence.
2. Produce a compact list titled **내가 꼭 확인할 정보들**. For each item, name the evidence to inspect (screen state, API request/response, file/function, database record, log, test, or collaboration note) and what can be stated only after checking it. Do not write a polished answer that pretends to be the user's own understanding.
3. Include the applicable items below, grounded in actual artifacts:
   - Where an AI proposal, limitation, or defect was first observed; the screen, log, test, or diff that showed it; what change was requested; and which parts were adopted, corrected, or discarded.
   - Why core logic or an engine was implemented incrementally; cases or alternatives compared; acceptance evidence for each stage; and remaining limits.
   - For shared operator data, the exact conflict behavior when another operator changes the same dataset, the visible error/status, audit trail, and recovery path.
   - What users see while recalculation is pending, and what they see if the routing/search engine fails. Distinguish an observed screen/API response from a proposed design.
   - How domain constraints such as vehicle capacity or arrival buffer were validated, where the validation code runs, and how valid inputs/results flow into the search or routing engine.
   - The responsibilities and data flow across frontend, backend, and database: input, validation, persistence, engine invocation, response, and route display.
   - How changes in constraints or input distribution affect route efficiency, what metric demonstrates the effect, and how to explain the causal chain from data and code without relying on AI-generated claims.
4. Ask the user to explain each selected item in their own words first. Then give feedback on accuracy, specificity, reasoning, and whether the explanation matches the actual artifacts.
5. Correct misconceptions by pointing to the relevant code or test. If evidence is missing, say so and suggest a real check rather than inventing a justification.
6. Keep the list aligned with the task's actual files; omit inapplicable domain examples and avoid generic items unrelated to the submission.

## Output
- 5–8 items under **내가 꼭 확인할 정보들**, based on the actual work
- Evidence location and verified/unverified status for each item
- User's own explanation and feedback, if provided
- Gaps that should be clarified or verified before submission

This skill is for preparation before any no-AI assessment phase. Follow the exam's rules when they prohibit AI use.
