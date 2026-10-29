---
name: verify-tests
description: Use after implementation or after a change to design and run focused tests, verify actual behavior, record evidence, and distinguish tested behavior from assumptions.
---

# Test and Verification

## Procedure
1. Convert each acceptance criterion into an observable check.
2. Inspect available test frameworks and commands before adding new dependencies.
3. Cover at least the most important happy path, a boundary/edge case, invalid or missing input, and a likely failure path when relevant.
4. Run the narrowest useful tests first, then broader tests if time and environment permit.
5. For UI/service tasks, verify startup and at least one real end-to-end interaction if the environment permits. For data tasks, independently recalculate or spot-check representative results.
6. Record exact commands, inputs, expected results, actual results, and pass/fail status. Include relevant error excerpts without leaking secrets.
7. If a test cannot run, state why and what remains unverified. Never say “all tests pass” unless they actually ran and passed.
8. Fix high-impact failures before cosmetic issues; rerun tests after fixes.

## Output
- Requirement-to-test matrix
- Commands and test results
- Defects found and fixes applied
- Untested areas and reasons
- Remaining risk and recommended next check
