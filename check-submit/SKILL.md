---
name: check-submit
description: Use near the deadline to audit the current workspace against task instructions, verify required files and filenames, inspect diffs, and report exactly what is ready or still missing.
---

# Submission Audit

## Procedure
1. Re-read the task's submission instructions and extract the exact required files, names, paths, formats, and delivery method.
2. Inspect the workspace and repository status. Confirm that each required artifact exists at the required location and is not empty or stale.
3. Check that implementation, plan, collaboration records, and verification notes agree with one another.
4. Run the highest-value final checks that fit the remaining time. Do not start large refactors or risky feature work at the deadline.
5. Inspect the diff for accidental files, debug output, secrets, local paths, temporary data, and unrelated changes.
6. Confirm run instructions and required dependencies/configuration are documented where needed.
7. Do not delete files or alter submission contents without a clear reason. Do not push to a remote repository unless explicitly authorized; obey any no-push rule.
8. Report gaps honestly. Never imply that clicking submit or uploading succeeded unless the environment confirms it.

## Output
- Required artifact checklist: present / missing / verified
- Final test results and any checks skipped
- Consistency issues between code and documents
- Remaining limitations
- Immediate next actions ordered by importance
