---
name: map-project
description: Use at the beginning of an unfamiliar task to map the current workspace, summarize important files, identify entry points and execution flow, and flag unknowns without changing files.
---

# Project Inventory

## Goal
Create a concise, evidence-based map of the existing project before proposing changes.

## Procedure
1. Inspect the current directory and repository status. Identify the project root and existing conventions.
2. List relevant files while excluding generated/vendor/noisy directories such as `.git`, `node_modules`, `.venv`, `venv`, `dist`, `build`, caches, and large data folders unless the task requires them.
3. Prioritize task instructions, `README`, `AGENTS.md`, manifests/lockfiles, configuration, entry points, routes/controllers, services, models, tests, migrations, and existing documentation.
4. Read only enough file content to establish each important file's purpose and the main execution/data flow. Use exact paths and line references when available.
5. Detect existing language/framework, run/test commands, expected environment variables, and apparent integration boundaries.
6. Never print secrets or full environment files. Report the presence of sensitive configuration without exposing values.
7. Do not edit files or install dependencies during inventory unless explicitly asked.

## Output
- Project type and apparent purpose
- Relevant directory tree (trimmed)
- Table: path | responsibility | why it matters
- Entry point and core execution/data flow
- Existing run/test commands and dependencies
- Existing changes or uncommitted files
- Unknowns and next recommended action

Separate **observed facts**, **inferences**, and **unknowns**. Do not claim a file or behavior exists without inspecting it.
