---
name: update-version
description: Workflow command scaffold for update-version in qinglong.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-version

Use this workflow when working on **update-version** in `qinglong`.

## Goal

Bump the project version number to a new release.

## Common Files

- `version.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update version.yaml with the new version number.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.