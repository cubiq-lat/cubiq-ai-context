---
name: roadmap-do-next-task
description: Pick the next available task from the roadmap and work on it in priority order.
---

# Roadmap Do Next Task

Pick the next available task from the roadmap and work on it.

## Workflow

1. **Read `roadmap/index.md`** to see all planned features and their status
2. **Find the first unchecked issue** in priority order
3. **Read the issue file** for full implementation details
4. **Verify not already in progress** - check for "In Progress" marker in index.md
5. **Mark as in progress** - update the checkbox to `[ ] 🚧` in index.md
6. **Implement** - work on the feature following the issue details
7. **Wait for user confirmation** that the task is complete
8. **On user confirmation**:
   - Mark checkbox as `[x]` in index.md
   - Delete the issue file
   - Commit with message starting with "AGENT:"
   - Bump version in `package.json`

## Status Markers (in index.md)

- `[ ]` — Not started
- `[ ] 🚧` — In progress
- `[x]` — Completed

## Guidelines

- Always start by reading `roadmap/index.md`
- Work issues in order (001, 002, 003...)
- If issue has dependencies, skip and move to next
- Do NOT mark complete or delete files until user explicitly confirms
- Issue files themselves do NOT contain progress markers
