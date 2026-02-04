# 📋 Work Summary Skill

> AI coding assistant skill that generates a structured project history organized by time periods.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📁 **Single history file** | All work in one organized document |
| 📅 **Period-based structure** | Week → Month → Quarter → Archive |
| 🔍 **Progressive detail** | More detail for recent, summarized for older |
| 🔄 **Regeneratable** | Run anytime to refresh |
| 📁 **Local-only** | Auto-added to `.gitignore` |

## 🚀 Installation

```bash
# Clone and install
git clone https://github.com/betarobot/latest-summary-skill.git
cp -r latest-summary-skill ~/.gemini/skills/latest-summary
```

## 📖 Usage

```
/latest
```

Or ask: "Show project history", "What did we do?", "Work summary"

## 📄 Output Structure

Creates `history.md` in your workspace root:

```markdown
# Project History

## 📅 This Week
> Daily breakdown with full details
- Every task, file change, decision

## 📆 Last 30 Days  
> Weekly summaries
- Grouped by week, themes, key outcomes

## 📊 Last 90 Days
> Monthly feature summaries
- Milestones, features delivered

## 📈 Last 180 Days
> Quarterly strategic overview
- Major initiatives, architecture changes

## 🗂️ Archive
> Historical record (condensed)
- One-line per month for older work

## 📌 Pending Items
- Outstanding tasks carried forward
```

## 📊 Detail Levels

| Period | Grouping | What's Included |
|--------|----------|-----------------|
| This week | Daily | Tasks, files, decisions, code |
| 30 days | Weekly | Themes, key outcomes, tables |
| 90 days | Monthly | Features, milestones |
| 180 days | Quarterly | Strategic overview |
| Archive | Yearly | One-line summaries |

## 🤝 Contributing

PRs welcome! Fork → Branch → Submit

## 📜 License

MIT - see [LICENSE](LICENSE)

---

Made with ❤️ for the AI coding community
