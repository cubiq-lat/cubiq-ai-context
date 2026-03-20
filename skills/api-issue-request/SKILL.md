---
name: api-issue-request
description: Generate a formatted API implementation request for the Cubiq NestJS API. Used by any project agent to request new endpoints, modifications, or bug fixes. Outputs issue text to chat for copy-paste.
---

# API Issue Request

Generate a formatted issue text requesting work on the Cubiq NestJS API.

## Cubiq API Reference

- **Docs:** https://api.cubiq.lat/docs (JSON: https://api.cubiq.lat/docs-json)
- **Base URL:** https://api.cubiq.lat
- **Local dev:** http://127.0.0.1:8085

### Standard Response Envelope

```json
{
  "success": true,
  "code": 10000,
  "timestamp": 1774013918246,
  "responseTime": 0.006,
  "data": { ... }
}
```

### Common Response Codes

| Code | Meaning |
|------|---------|
| 10000 | Success |
| 40000 | Validation error |
| 50001 | Server error |

## Workflow

1. **Gather requirements** from the user:
   - What type of request? (new endpoint / modification / bug fix)
   - Endpoint path and method
   - Purpose — what does this do and why is it needed?
   - Database table and relevant columns (if applicable)
   - Parameters (query params, body fields)
   - Expected response shape
   - Auth required? (yes/no, which role)
   - Which API module does this belong to? (users, auth, voting, cms)

2. **Generate the issue text** matching the format below

3. **Print to chat** for the user to copy-paste

## Issue Format

```markdown
# [Request type]: [Short title]

## Context
[1-3 sentences explaining the need]

## Requirements
1. [Numbered, specific, testable requirements]

## Endpoint
[Method] /path

## Parameters
| Param | Type | Required | Default | Description |
|-------|------|----------|---------|-------------|

## Expected Response
```json
{
  "success": true,
  "code": 10000,
  "data": { ... }
}
```

## Acceptance Criteria
- [ ] [Each independently testable]

## Files to Modify
- `module/file.ts` — [what changes]
```

## Guidelines

- Match the Cubiq response envelope format in all examples
- Query params should be optional with defaults where possible
- Never expose sensitive fields (password_hash, app_id) in public endpoints
- Explicitly list allowed values when constraints exist (e.g., sort fields)
- Include error cases in acceptance criteria when relevant
- Be specific — the API agent should not need to guess
