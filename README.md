# 📋 Latest Summary Skill

> AI coding assistant skill that generates comprehensive work summaries for any project.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📅 **7-day activity log** | Detailed breakdown of recent work |
| 🔍 **Workspace-aware** | Auto-detects current project context |
| 📁 **Local-only output** | Automatically added to `.gitignore` |
| 📊 **Structured format** | Tables, status indicators, file links |
| 🔄 **Regeneratable** | Run anytime to get updated summary |

## 🚀 Installation

### For Gemini / Antigravity

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/latest-summary-skill.git

# Copy to skills directory
cp -r latest-summary-skill ~/.gemini/skills/latest-summary
```

### Manual Installation

1. Download or clone this repository
2. Copy the contents to your AI assistant's skills directory
3. Restart your assistant or reload skills

## 📖 Usage

### Command

```
/latest
```

### Natural Language

- "What did we do recently?"
- "Generate a work summary"
- "Show me the last week's activity"
- "Create an activity log"

## 📄 Output

The skill creates `latest.md` in your workspace root:

```
your-project/
├── latest.md          ← Generated summary
├── .gitignore         ← Auto-updated to include latest.md
└── ...
```

### Sample Output Structure

```markdown
# Work Summary: Last 7 Days

**Generated**: 2026-02-04 22:00
**Period**: 2026-01-28 to 2026-02-04
**Project**: My Awesome Project

## Overview
Brief summary of major accomplishments...

## Detailed Activity Log
### 2026-02-04 - Tuesday
#### Feature Implementation
**Objective**: What the user wanted to achieve
**Work Performed**: Detailed steps taken
**Files Modified**: List of changed files
**Outcome**: ✅ Completed

## Summary of Changes
| File | Changes |
|------|---------|
| `src/app.js` | Added new feature |

## Technical Decisions
- **Decision**: Rationale explained

## Pending Items
- [ ] Outstanding tasks
```

## ⚙️ Customization

Edit `SKILL.md` to customize:

| Setting | Default | Description |
|---------|---------|-------------|
| Time period | 7 days | How far back to look |
| Output file | `latest.md` | Generated filename |
| Detail level | Verbose | Amount of information |

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## 📜 License

MIT License - see [LICENSE](LICENSE) for details.

---

Made with ❤️ for the AI coding community
