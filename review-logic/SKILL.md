---
name: review-logic
description: Use after AI-generated or modified code exists to trace the real core logic, inspect changes, find defects, and prepare an evidence-based explanation of what changed and why.
---

# Core Logic Review and Explanation

## Procedure
1. Inspect the actual diff and relevant current files. Do not rely only on the coding agent's summary.
2. Identify the main entry point and trace one representative request/input through validation, core processing, data access, and output.
3. Explain important functions, state/data structures, algorithms, business rules, and error handling with file paths and line references when available.
4. For every material change, record: prior behavior (if verified), new behavior, reason, requirement satisfied, and evidence.
5. Look for correctness risks: missing validation, incorrect boundaries, hidden assumptions, exception paths, data loss, security/privacy issues, duplicated logic, race conditions, and mismatch between docs and code.
6. Check whether the implementation actually matches the requirement and whether any claimed behavior is unsupported by code or tests.
7. Separate issues found from possible risks; do not invent defects. Suggest the smallest safe fix first.
8. Do not modify code during a review-only request. If asked to fix issues, explain the fix and then rerun relevant tests.

## Output
- Core flow: input → key functions → transformation/decision → output
- Key files/functions and their responsibilities
- Important changes and rationale
- Findings ranked by severity, with evidence
- Tests that support or fail to support each claim
- A plain-language explanation the developer can personally defend

Never claim to understand or verify code that you did not inspect or execute.
