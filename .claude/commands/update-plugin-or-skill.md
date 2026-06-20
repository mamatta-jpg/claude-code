---
name: update-plugin-or-skill
description: Workflow command scaffold for update-plugin-or-skill in claude-code.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-plugin-or-skill

Use this workflow when working on **update-plugin-or-skill** in `claude-code`.

## Goal

Updates a plugin or skill, including its metadata (plugin.json), documentation (README.md or SKILL.md), and implementation files.

## Common Files

- `plugins/*/.claude-plugin/plugin.json`
- `plugins/*/README.md`
- `plugins/*/skills/*/SKILL.md`
- `plugins/*/hooks/*.py`
- `plugins/*/hooks/*.sh`
- `plugins/*/hooks/*.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit plugin.json to update metadata or version.
- Update documentation files (README.md or SKILL.md).
- Modify implementation files as needed.
- Commit all related files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.