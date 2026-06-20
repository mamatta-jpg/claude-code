---
name: update-github-workflow
description: Workflow command scaffold for update-github-workflow in claude-code.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-github-workflow

Use this workflow when working on **update-github-workflow** in `claude-code`.

## Goal

Modifies one or more GitHub Actions workflow YAML files to change CI/CD or automation behavior.

## Common Files

- `.github/workflows/*.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more .github/workflows/*.yml files.
- Commit the changes, often referencing the workflow name in the commit message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.