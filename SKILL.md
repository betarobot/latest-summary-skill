---
name: latest-summary
description: Generate a detailed markdown summary of recent work on the current workspace. Invoke with /latest or when asking for a work summary, activity log, or "what did we do" review.
---

# Latest Work Summary

Generate `latest.md` in the **current workspace root** with a comprehensive summary of recent work.

## Trigger

- `/latest` command
- "What did we do?" or similar questions
- Requests for work summary or activity log

## Behavior

1. **Detect workspace root** from active workspace URI
2. **Scan conversation history** for work done in the **last 7 days** on this workspace
3. **Generate `latest.md`** in the workspace root
4. **Update `.gitignore`** to include `latest.md` (keeps summary local-only)

## Output Format

```markdown
# Work Summary: Last 7 Days

**Generated**: [YYYY-MM-DD HH:MM]  
**Period**: [Start Date] to [End Date]  
**Project**: [Workspace/Project Name]  
**Workspace**: [Full workspace path]

---

## Overview

[2-3 sentence summary of major accomplishments]

---

## Detailed Activity Log

### [YYYY-MM-DD] - [Day of Week]

#### [Task/Conversation Title]
**Objective**: [What the user wanted to achieve]

**Work Performed**:
- [Detailed description of actions taken]
- [Specific steps and decisions made]

**Files Modified**:
- `path/to/file` - [Description of changes]

**Outcome**: [✅ Completed | 🔄 In Progress | 🔍 Investigation | ❌ Blocked]

---

## Summary of Changes

### Files Created
| File | Purpose |
|------|---------|
| `path/to/file` | [Description] |

### Files Modified
| File | Changes Made |
|------|--------------|
| `path/to/file` | [Description] |

---

## Technical Decisions

- **[Decision]**: [Rationale and alternatives considered]

---

## Issues & Resolutions

| Issue | Resolution |
|-------|------------|
| [Problem] | [Solution] |

---

## Pending Items

- [ ] [Task with context]

---

## Notes

[Additional context or observations]
```

## Guidelines

- **Be verbose**: Include file paths, function names, technical details
- **Document decisions**: Explain why approaches were chosen
- **Use file links**: `[filename](file:///absolute/path)`
- **Group by date**: Most recent first
- **Use tables**: For structured information
- **Track outcomes**: ✅ 🔄 🔍 ❌ status indicators
