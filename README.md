# 📋 Work Summary Skill

> AI coding assistant skill that generates a structured project history organized by time periods.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📁 **Single history file** | All work in one organized `history.md` |
| 📅 **Period-based structure** | Week → Month → Quarter → 6 Months → Archive |
| 🔍 **Progressive detail** | Full detail for recent, summarized for older |
| 🔄 **Regeneratable** | Run anytime to refresh with latest |
| 🔒 **Local-only** | Auto-added to `.gitignore` |

## 🚀 Installation

```bash
# Clone and install
git clone https://github.com/betarobot/latest-summary-skill.git
cp -r latest-summary-skill ~/.gemini/skills/latest-summary
```

## 📖 Usage

### Default (Current Project Only)
```
/latest
```
Generates history **only** for the project you are currently working in.

### Global (All Projects)
```
/latest -all
```
Generates history including **all** work across all projects/workspaces.

### Natural Language
- "Show project history" (Current project)
- "What did we do in this repo?" (Current project)
- "Show me everything I've worked on recently" (Global)
- "Activity log"

## 📄 Output Structure

Creates `history.md` in your workspace root with these sections:

```
📅 This Week          → Daily breakdown with full details
📆 Last 30 Days       → Weekly summaries with themes
📊 Last 90 Days       → Monthly feature summaries
📈 Last 180 Days      → Quarterly strategic overview
🗂️ Archive            → Condensed historical record
📌 Pending Items      → Outstanding tasks
📝 Notes              → Lessons learned
```

## 📊 Detail by Period

| Period | Grouping | What's Included |
|--------|----------|-----------------|
| This week | Daily | Every task, file path, decision, code changes |
| 30 days | Weekly | Themes, key outcomes, decision rationale |
| 90 days | Monthly | Features delivered, milestones, metrics |
| 180 days | Quarterly | Strategic overview, architecture changes |
| Archive | Yearly | One-line summaries per month |

## 📋 Sample Output

```markdown
# Project History

**Project**: My Project  
**Last Updated**: 2026-02-04 23:00

---

## 📅 This Week

### Tuesday, 2026-02-04

#### Feature Implementation
**Objective**: Add user authentication

**Work Done**:
- Created auth middleware
- Implemented JWT tokens
- Added session management

**Files Changed**:
- `src/auth/middleware.js` - New auth handler

**Status**: ✅ Completed

---

## 📆 Last 30 Days

### Week of Jan 28 - Feb 3
**Themes**: Authentication, Testing

| Task | Status | Summary |
|------|--------|---------|
| User auth | ✅ | JWT implementation |
| Test suite | ✅ | 80% coverage |

---

## 📌 Pending Items

- [ ] Add password reset flow
- [ ] Improve test coverage
```

## ⚙️ Customization

Edit `SKILL.md` to adjust:

| Setting | Default | Description |
|---------|---------|-------------|
| Output file | `history.md` | Generated filename |
| Detail levels | Progressive | How much info per period |
| Status indicators | ✅ 🔄 🔍 ❌ | Task outcome markers |

## 🤝 Contributing

PRs welcome! Fork → Branch → Submit

## 📜 License

MIT - see [LICENSE](LICENSE)

---

Made with ❤️ for the AI coding community
