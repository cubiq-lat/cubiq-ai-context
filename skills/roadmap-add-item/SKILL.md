---
name: roadmap-add-item
description: Create a new entry in the project roadmap when user requests a new feature or bug fix.
---

# Roadmap Add Item

Create a new entry in the project roadmap.

## When to Use

- User requests a new feature not in roadmap
- Bug fix that needs tracking
- Any work item worth documenting

## Workflow

1. **Read `roadmap/index.md`** to understand current structure and numbering
2. **Ask the user** for details about the new item (context, requirements, acceptance criteria)
3. **Determine the version/folder** (e.g., `beta/`, `v1.0/`)
4. **Determine the next number** for the issue (check existing files)
5. **Determine the category/folder** (create new folder if needed)
6. **Create the issue file** with proper naming convention
7. **Update `roadmap/index.md`** to include the new item with unchecked checkbox `[ ]`
8. **Commit** with message starting with "AGENT:"

## File Naming

Format: `###-descriptive-name.md`

Examples:
- `001-earn-karma-on-approval.md`
- `002-rate-limit-comments.md`
- `003-auto-flag-spam-comments.md`

## Issue File Template

```markdown
# Issue #[NUMBER]: [Title]

## Context
[What problem does this solve? Why is it needed?]

## Requirements
[What needs to be done?]

## Acceptance Criteria
- [ ] [Criterion 1]
- [ ] [Criterion 2]

## Files to Modify/Create
- `path/to/file.ext` (new/change)
```

## Guidelines

- Ask the user for issue details before creating the file
- Use kebab-case for filenames
- Number sequentially within each folder
- Be concise but complete in issue description
- Include all acceptance criteria
- Progress is tracked in index.md, not in issue files
