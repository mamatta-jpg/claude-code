---
name: update-changelog-and-feed
description: Workflow command scaffold for update-changelog-and-feed in claude-code.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-changelog-and-feed

Use this workflow when working on **update-changelog-and-feed** in `claude-code`.

## Goal

Updates the CHANGELOG.md and feed.xml files, likely to publish release notes and update an RSS/Atom feed with recent changes.

## Common Files

- `CHANGELOG.md`
- `feed.xml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit CHANGELOG.md to add new entries.
- Update feed.xml to reflect the latest changes.
- Commit both files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.