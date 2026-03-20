---
name: roadmap-complete-item
description: Mark a roadmap task as completed when the implementation is finished.
---

# Roadmap Complete Item
Mark a roadmap task as completed after implementation is done.
## When to Use
- After finishing implementation of a roadmap task
- User confirms a task is done
## Workflow
1. **Read `roadmap/index.md`** to find the task
2. **Change `- [ ]` to `- [x]`** for the completed task
3. **Bump the patch version** in `app/package.json`
4. **Commit** with message starting with "AGENT:"
5. **Ask before pushing**
## Guidelines
- Only mark tasks as complete after implementation is verified (build passes)
- Issue files remain in place as documentation
- Do not delete issue files or their contents
- Progress is tracked in index.md checkboxes, not in issue files