---
name: roadmap-add-item
description: Create a new entry in the project roadmap when user requests a new feature or bug fix. Supports auto-import from formatted issue text.
---

# Roadmap Add Item

Create a new entry in the project roadmap.

## When to Use

- User requests a new feature not in roadmap
- Bug fix that needs tracking
- User pastes issue text from another agent/project
- Any work item worth documenting

## Modes

### Mode 1: Auto-Import (from pasted issue text)

Use when the user pastes formatted issue text (e.g., from `api-issue-request` or another project).

1. **Read `roadmap/index.md`** to understand current structure
2. **Parse the issue text** to extract:
   - Title from `# [Type]: [Title]` or `# Issue #[N]: [Title]`
   - Context from `## Context`
   - Requirements from `## Requirements`
   - Acceptance criteria from `## Acceptance Criteria`
   - Files from `## Files to Modify/Create` or `## Files to Modify`
   - Endpoint from `## Endpoint` (for category detection)
3. **Detect category** using the rules below
4. **Determine the next number** in that category (globally across all categories)
5. **Create the issue file** with extracted content
6. **Update `roadmap/index.md`** to add the new item with `[ ]` checkbox
7. **Commit** with message starting with "AGENT:"

### Mode 2: Interactive (fallback)

Use when no issue text is provided or details are unclear.

1. **Read `roadmap/index.md`** to understand current structure and numbering
2. **Ask the user** for details about the new item (context, requirements, acceptance criteria)
3. **Determine the version/folder** (e.g., `beta/`, `v1.0/`)
4. **Determine the next number** for the issue (check existing files)
5. **Determine the category/folder** (create new folder if needed)
6. **Create the issue file** with proper naming convention
7. **Update `roadmap/index.md`** to include the new item with unchecked checkbox `[ ]`
8. **Commit** with message starting with "AGENT:"

## Smart Category Detection

Analyze issue content and assign to category folder automatically:

| Source | Category Folder |
|--------|-----------------|
| Endpoint: `/users/*`, `/users/list` | `users/` |
| Content: `Cq_Users`, `user module`, `getUsers` | `users/` |
| Endpoint: `/auth/*`, `/login`, `/register` | `auth/` |
| Content: `JWT`, `access_token`, `refresh_token` | `auth/` |
| Endpoint: `/comments/*` | `comments/` |
| Content: `comment`, `karma`, `approval` | `comments/` |
| Endpoint: `/ai/*`, inference-related | `ai/` |
| Content: `openrouter`, `model`, `transformers` | `ai/` |
| Endpoint: `/exchange/*`, `/payments/*` | `payments/` |
| Content: `pix`, `bitcoin`, `sats`, `exchange rate` | `payments/` |
| Endpoint: `/products/*`, `/orders/*` | `commerce/` |
| No match found | Prompt user for category |

### Category Detection Priority

1. Check `## Endpoint` section first (most reliable)
2. Check `## Files to Modify` for module paths (e.g., `src/users/` → `users/`)
3. Check `## Context` and `## Requirements` for keywords
4. Fall back to asking user if ambiguous

## Parsing Issue Text

### Input Format Expected

The skill accepts issue text matching the `api-issue-request` format:

```markdown
# [Request type]: [Short title]

## Context
[Description text]

## Requirements
1. [Requirement text]

## Endpoint
[METHOD] /path

## Parameters
| Param | Type | Required | Default | Description |

## Expected Response
```json
{ ... }
```

## Acceptance Criteria
- [ ] [Criterion]

## Files to Modify
- `path/to/file.ts` — [changes]
```

### Parsing Rules

1. **Title**: Extract from first `#` heading, strip prefix like `New endpoint:` or `Issue #001:`
2. **Context**: Everything between `## Context` and next `##`
3. **Requirements**: Numbered list under `## Requirements`
4. **Acceptance Criteria**: Bullet list under `## Acceptance Criteria`, keep `- [ ]` format
5. **Files**: Extract from `## Files to Modify/Create` or `## Files to Modify`
6. **Endpoint**: Extract method and path from `## Endpoint` line

### Output Issue File

Transform parsed content into roadmap issue format:

```markdown
# Issue #[NUMBER]: [Parsed Title]

## Context
[Parsed context]

## Requirements
[Parsed requirements]

## Acceptance Criteria
[Parsed criteria as-is]

## Files to Modify/Create
[Parsed files]
```

## File Naming

Format: `###-descriptive-name.md`

- Use kebab-case
- Derive from title: `New endpoint: GET /users/list` → `007-get-users-list.md`
- Numbers are global (001, 002, 003...) not per-category

Examples:
- `001-earn-karma-on-approval.md`
- `002-rate-limit-comments.md`
- `007-get-users-list.md`

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

## Index Update Format

When updating `roadmap/index.md`:

1. Find or create the `### [Category]` section under the current version
2. Add entry: `- [ ] [NNN: Title](./version/category/NNN-title.md)`
3. Maintain sort order by number

Example addition to `### Users` section:
```markdown
### Users
- [ ] [005: Add GET /users/list endpoint for leaderboard](./beta/users/005-users-list-leaderboard.md)
- [ ] [006: Add sort support to GET /users/list](./beta/users/006-add-sort-support-to-users-list.md)
- [ ] [007: New item title here](./beta/users/007-new-item-title.md)
```

## Guidelines

- Use kebab-case for filenames
- Number sequentially globally (not per-folder)
- Be concise but complete in issue description
- Include all acceptance criteria
- Progress is tracked in index.md, not in issue files
- When auto-importing, show the user what was parsed before creating files
- If parsing fails or is ambiguous, fall back to interactive mode
