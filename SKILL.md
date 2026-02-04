---
name: work-summary
description: Generate detailed markdown summaries of recent work on the current workspace. Supports multiple timeframes - /latest (7 days), /monthly (30 days), /quarterly (90 days), /biannual (180 days).
---

# Work Summary Skill

Generate comprehensive work summaries in the **current workspace root** for various timeframes.

## Commands

| Command | Period | Output File |
|---------|--------|-------------|
| `/latest` | Last 7 days | `latest.md` |
| `/monthly` | Last 30 days | `monthly.md` |
| `/quarterly` | Last 90 days | `quarterly.md` |
| `/biannual` | Last 180 days | `biannual.md` |

## Behavior

1. **Detect workspace root** from active workspace URI
2. **Scan conversation history** for the specified period on this workspace
3. **Generate the appropriate `.md` file** in the workspace root
4. **Update `.gitignore`** to include the generated file (keeps summaries local-only)

## Output Format

### Short-term (7 days): Detailed Daily Log

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

### Medium-term (30 days): Weekly Grouped Summary

```markdown
# Work Summary: Last 30 Days

**Generated**: [YYYY-MM-DD HH:MM]  
**Period**: [Start Date] to [End Date]  
**Project**: [Workspace/Project Name]

---

## Overview
[High-level summary of the month's accomplishments, themes, and progress]

---

## Week-by-Week Summary

### Week of [Date Range]
**Focus Areas**: [Main themes of work]

| Task | Status | Key Changes |
|------|--------|-------------|
| [Task name] | ✅ | [Brief description] |

---

## Major Milestones
- [Milestone 1]: [Description and date]
- [Milestone 2]: [Description and date]

---

## Key Files Changed
| File | Type of Changes |
|------|-----------------|
| `path/to/file` | [Created/Modified/Refactored] |

---

## Technical Decisions Made
| Decision | Rationale | Date |
|----------|-----------|------|
| [Decision] | [Why] | [When] |

---

## Recurring Issues
| Issue | Occurrences | Final Resolution |
|-------|-------------|------------------|
| [Issue] | [Count] | [How resolved] |

---

## Pending Items
- [ ] [Carried over tasks]
```

### Long-term (90/180 days): High-Level Feature Summary

```markdown
# Work Summary: Last [90/180] Days

**Generated**: [YYYY-MM-DD HH:MM]  
**Period**: [Start Date] to [End Date]  
**Project**: [Workspace/Project Name]

---

## Executive Summary
[Paragraph summarizing major achievements, project evolution, and key milestones]

---

## Major Features & Initiatives

### [Feature/Initiative Name]
**Timeline**: [Start] - [End]  
**Status**: [Completed/Ongoing/Paused]

**Description**: [What was built/changed]

**Key Accomplishments**:
- [Accomplishment 1]
- [Accomplishment 2]

---

## Architecture Changes
| Component | Change | Impact |
|-----------|--------|--------|
| [Component] | [What changed] | [Effect] |

---

## Key Metrics (if applicable)
- Files created: [count]
- Files modified: [count]
- Major features: [count]
- Bug fixes: [count]

---

## Technical Debt Addressed
| Area | What was done |
|------|---------------|
| [Area] | [Description] |

---

## Lessons Learned
- [Lesson 1]
- [Lesson 2]

---

## Looking Forward
- [ ] Planned features/improvements
- [ ] Known issues to address
```

## Guidelines

- **7 days**: Maximum detail - include all conversations, file paths, code changes
- **30 days**: Group by week, summarize daily work into themes
- **90/180 days**: Feature-level view, focus on milestones and impact
- **Use tables**: For structured, scannable information
- **Track outcomes**: ✅ 🔄 🔍 ❌ status indicators
- **Link files**: `[filename](file:///absolute/path)`
