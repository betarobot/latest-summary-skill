# 📋 Work Summary Skill

> AI coding assistant skill that generates comprehensive work summaries for any project across multiple timeframes.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📅 **Multiple timeframes** | 7 days, 30 days, 90 days, 180 days |
| 🔍 **Workspace-aware** | Auto-detects current project context |
| 📁 **Local-only output** | Automatically added to `.gitignore` |
| 📊 **Adaptive detail** | More detail for recent, high-level for long-term |
| 🔄 **Regeneratable** | Run anytime to get updated summary |

## 🚀 Installation

### For Gemini / Antigravity

```bash
# Clone the repo
git clone https://github.com/betarobot/latest-summary-skill.git

# Copy to skills directory
cp -r latest-summary-skill ~/.gemini/skills/latest-summary
```

### Manual Installation

1. Download or clone this repository
2. Copy the contents to your AI assistant's skills directory
3. Restart your assistant or reload skills

## 📖 Usage

### Commands

| Command | Period | Output | Detail Level |
|---------|--------|--------|--------------|
| `/latest` | 7 days | `latest.md` | Daily breakdown |
| `/monthly` | 30 days | `monthly.md` | Weekly grouped |
| `/quarterly` | 90 days | `quarterly.md` | Feature-level |
| `/biannual` | 180 days | `biannual.md` | Executive summary |

### Natural Language

- "What did we do recently?" → 7-day summary
- "Monthly summary" → 30-day summary
- "Quarterly review" → 90-day summary
- "Six month overview" → 180-day summary

## 📄 Output

Creates summary files in your workspace root:

```
your-project/
├── latest.md          ← 7-day detailed log
├── monthly.md         ← 30-day weekly summary
├── quarterly.md       ← 90-day feature summary
├── biannual.md        ← 180-day executive overview
├── .gitignore         ← Auto-updated
└── ...
```

### Detail Levels by Timeframe

| Timeframe | Grouping | Focus |
|-----------|----------|-------|
| **7 days** | Daily | Every task, file change, decision |
| **30 days** | Weekly | Themes, milestones, key changes |
| **90 days** | Monthly | Features, architecture, metrics |
| **180 days** | Quarterly | Strategic overview, lessons learned |

## 📋 Sample Outputs

<details>
<summary><strong>7-Day Summary (detailed)</strong></summary>

```markdown
# Work Summary: Last 7 Days

## Detailed Activity Log
### 2026-02-04 - Tuesday
#### Feature Implementation
**Objective**: Add user authentication
**Work Performed**:
- Created auth middleware
- Implemented JWT tokens
**Files Modified**:
- `src/auth/middleware.js` - New file
**Outcome**: ✅ Completed
```
</details>

<details>
<summary><strong>30-Day Summary (weekly)</strong></summary>

```markdown
# Work Summary: Last 30 Days

## Week-by-Week Summary
### Week of Jan 28 - Feb 3
**Focus Areas**: Authentication, Testing

| Task | Status | Key Changes |
|------|--------|-------------|
| User auth | ✅ | JWT implementation |
| Test suite | ✅ | 80% coverage |
```
</details>

<details>
<summary><strong>90/180-Day Summary (strategic)</strong></summary>

```markdown
# Work Summary: Last 90 Days

## Executive Summary
Major platform overhaul including authentication system,
performance optimizations, and Drupal 11 migration.

## Major Features & Initiatives
### Authentication System
**Timeline**: Dec 2025 - Jan 2026
**Status**: Completed
```
</details>

## ⚙️ Customization

Edit `SKILL.md` to adjust:

| Setting | Options | Description |
|---------|---------|-------------|
| Timeframes | 7/30/90/180 days | Coverage period |
| Output files | `*.md` | Generated filenames |
| Detail level | Verbose/Summary | Information depth |
| Grouping | Daily/Weekly/Monthly | How to organize |

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## 📜 License

MIT License - see [LICENSE](LICENSE) for details.

---

Made with ❤️ for the AI coding community
