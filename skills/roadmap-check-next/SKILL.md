---
name: roadmap-check-next
description: Check what's next in the TapTapGo roadmap. Triggers when user asks "check roadmap", "what's next in roadmap", "show roadmap", or "roadmap status".
---

# Roadmap Check Next

Check the TapTapGo roadmap status and show next pending tasks.

## Roadmap Location

- **Path:** ./roadmap/index.md

## Workflow

1. **Read** `roadmap/index.md`
2. **Parse** the checklist items:
   - Count completed items ([x])
   - List pending items ([ ])
   - Group by category
3. **Display** a concise summary with:
   - Total completed/pending counts
   - Next 3-5 pending items in priority order
   - Categories with remaining work

## Output Format

```
## TapTapGo Roadmap Status

**Completed:** X | **Pending:** Y

### Next Tasks
1. [ID]: [Task name] ([Category])
2. [ID]: [Task name] ([Category])
3. [ID]: [Task name] ([Category])

### By Category
- **Auth:** X/Y completed
- **Cart:** X/Y completed
- ...
```

## Trigger Phrases

- "check roadmap"
- "what's next in roadmap"
- "show roadmap"
- "roadmap status"
- "what do we have in the roadmap"
- "what's in the roadmap"
