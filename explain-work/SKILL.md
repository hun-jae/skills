---
name: explain-work
description: Use before final submission to generate likely follow-up questions from the actual task artifacts and help the user practice explaining reviewed changes, core logic, decisions, tests, and limitations in their own words.
---

# Artifact-Based Explanation Practice

## Procedure
1. Read the current task brief, implementation, actual diffs, plan/collaboration notes, and verification evidence.
2. Generate focused questions grounded in those artifacts, especially:
   - What did you personally inspect or change, and why?
   - What is the core logic and how did you trace/understand it?
   - Which requirement does a key design decision satisfy?
   - What did a specific test establish, and what did it not establish?
   - What failed or changed during implementation?
   - What is the most important limitation or next improvement?
3. For each question, identify the evidence the user should consult (file/function/test/document). Do not write a polished answer that pretends to be the user's own understanding.
4. Ask the user to answer in their own words first. Then give feedback on accuracy, specificity, reasoning, and whether the answer matches the actual artifacts.
5. Correct misconceptions by pointing to the relevant code or test. If evidence is missing, say so and suggest a real check rather than inventing a justification.
6. Keep practice aligned with the task's actual files; avoid generic questions unrelated to the submission.

## Output
- 5–8 likely questions based on the actual work
- Evidence location for each question
- User's answer and feedback, if provided
- Gaps that should be clarified or verified before submission

This skill is for preparation before the no-AI follow-up phase. Follow the exam's rule prohibiting AI use during the actual written follow-up if that rule applies.
