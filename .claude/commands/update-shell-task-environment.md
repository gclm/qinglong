---
name: update-shell-task-environment
description: Workflow command scaffold for update-shell-task-environment in qinglong.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-shell-task-environment

Use this workflow when working on **update-shell-task-environment** in `qinglong`.

## Goal

Modify shell scripts and environment variable handling for task execution.

## Common Files

- `shell/otask.sh`
- `shell/share.sh`
- `shell/preload/sitecustomize.js`
- `shell/preload/sitecustomize.py`
- `back/services/env.ts`
- `back/config/index.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit shell scripts such as shell/otask.sh, shell/share.sh, shell/preload/sitecustomize.js, shell/preload/sitecustomize.py.
- Update back/services/env.ts or back/config/index.ts if environment logic changes.
- Optionally update Dockerfile or related files if environment changes affect containers.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.