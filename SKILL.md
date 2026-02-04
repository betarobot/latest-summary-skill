---
name: work-summary
description: Generate a structured work history document organized by time periods. Invoke with /latest or when asking for work summary, activity log, or project history.
---

# Work Summary Skill

Generate `history.md` in the **current workspace root** - a comprehensive work log organized by time periods.

## Command

```
/latest
```

Or natural language: "What did we do?", "Show project history", "Work summary"

## Behavior

1. **Detect workspace root** from active workspace URI
2. **Scan conversation history** for all available work on this workspace
3. **Generate `history.md`** organized by periods
4. **Update `.gitignore`** to include `history.md`

## Output Structure

```markdown
# Project History

**Project**: [Workspace/Project Name]  
**Workspace**: [Full workspace path]  
**Last Updated**: [YYYY-MM-DD HH:MM]

---

## 📅 This Week
> Detailed daily breakdown of current week's work

### [Day, Date]

#### [Task Title]
**Objective**: [Goal]

**Work Done**:
- [Detailed action]
- [Specific change]

**Files Changed**:
- `path/to/file` - [What changed]

**Status**: ✅ Completed

---

## 📆 Last 30 Days
> Weekly summaries of the past month

### Week of [Date Range]
**Themes**: [Main focus areas]

| Task | Status | Summary |
|------|--------|---------|
| [Task] | ✅ | [Brief outcome] |

**Key Decisions**:
- [Decision]: [Rationale]

---

## 📊 Last 90 Days
> Monthly feature-level summaries

### [Month Year]
**Highlights**:
- [Major accomplishment 1]
- [Major accomplishment 2]

**Features Delivered**:
| Feature | Status | Impact |
|---------|--------|--------|
| [Feature] | ✅ | [Result] |

---

## 📈 Last 180 Days
> Quarterly strategic overview

### Q[N] [Year]
**Executive Summary**: [Paragraph on major achievements]

**Initiatives**:
- **[Initiative]**: [Status and outcome]

**Architecture Changes**:
| System | Change | Reason |
|--------|--------|--------|
| [Component] | [What] | [Why] |

---

## 🗂️ Archive
> Older history beyond 6 months (condensed)

### [Year]
- **[Month]**: [One-line summary of major work]

---

## 📌 Pending Items

- [ ] [Outstanding task 1]
- [ ] [Outstanding task 2]

---

## 📝 Notes & Lessons Learned

- [Insight or pattern observed]
```

## Guidelines

### Detail by Period
| Period | Grouping | Detail Level |
|--------|----------|--------------|
| This week | Daily | Full task breakdown, all files, decisions |
| Last 30 days | Weekly | Theme summaries, key outcomes |
| Last 90 days | Monthly | Feature-level, milestones |
| Last 180 days | Quarterly | Strategic, high-impact items only |
| Archive | Yearly | One-line per month |

### Formatting Rules
- **Most recent first** within each section
- **Progressive summarization** - more detail for recent work
- **Link files**: `[filename](file:///path)`
- **Status indicators**: ✅ 🔄 🔍 ❌
- **Tables** for structured comparisons
- **Collapse older sections** if document gets long

### When to Update
- Run `/latest` to regenerate with current history
- Previous content is replaced with fresh scan
- Pending items carry forward between updates
