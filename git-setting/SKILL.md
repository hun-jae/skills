---
name: git-setting
description: Prepare a local project safely for Git worktrees, including first-time repository initialization when Git exists but the project has not been initialized.
---

# Git and Worktree Setup

## Goal

Make a project ready for isolated Git worktrees without overwriting existing history, staging secrets, or pushing anything remotely.

## Procedure

1. Inspect the target directory before changing it: identify the project root, whether it is already inside a repository, the current branch and status, remotes, existing worktrees, and relevant ignore rules. Do not assume that having Git installed means the directory is initialized.
2. If the project is already a repository, preserve its history, branch convention, remotes, and uncommitted work. Resolve the intended base branch before creating a worktree. Do not run `git init` inside an existing repository.
3. If it is not a repository, initialize it with the intended default branch (normally `main`). Inspect the proposed initial contents and `.gitignore` before staging. Never stage `.env`, credentials, build output, or unrelated local files merely to create an initial commit.
4. Check whether a usable local Git identity exists. Do not invent a name or email; ask the user to supply one or have them configure it when a first commit requires it.
5. Create the first local commit only after the staged files are reviewed. A commit is required before creating a normal linked worktree. Do not add a remote or push unless explicitly authorized.
6. Create each worktree as a sibling checkout with a descriptive branch and path. Verify that the new worktree has the intended branch and that the original checkout remains unchanged.
7. Report exact commands run, repository and worktree paths, base and feature branches, ignored/staged files, and any steps requiring user input.

## Command Pattern

Adapt paths and branch names to the actual project; inspect before running each mutation.

```powershell
# First-time initialization only: run from the project root after reviewing files.
git init -b main
git status --short
git add -- <reviewed-project-files>
git commit -m "chore: initial repository setup"

# Create a sibling worktree from the verified base branch.
git worktree add -b feature/<task-name> ..\<project-name>-<task-name> main
git worktree list
```

For an existing repository, omit initialization and use its verified base branch in the `git worktree add` command. If there are uncommitted changes, do not move, reset, or include them in another worktree without explicit direction.

## Completion Criteria

- The original checkout and base branch are identified and unchanged except for explicitly approved initialization.
- The initial commit, if needed, contains only reviewed project files.
- The new worktree has its own branch and expected path.
- No remote was added or pushed, and no secret was exposed or staged.
