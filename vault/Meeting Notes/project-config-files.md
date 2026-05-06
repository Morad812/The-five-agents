---
name: project-config-files
type: project-config
associated: The Five Agents — תשתית פרויקט
files:
  - CLAUDE.md
  - .env
  - .env.example
  - .gitignore
  - .obsidian/app.json
  - .obsidian/appearance.json
  - .obsidian/core-plugins.json
  - .obsidian/workspace.json
  - .claude/agents/.gitkeep
  - .claude/commands/.gitkeep
  - .claude/skills/.gitkeep
---

# קבצי תצורת הפרויקט

## Overview

קבצי התשתית של הפרויקט "The Five Agents" — מערכת סוכנים ליצירת תוכן.

- **CLAUDE.md** — הנחיות לתוכנת Claude Code: תיאור הפרויקט (מערכת 5 סוכנים, CEO מוביל צוות מתמחים) ומבנה תיקיות `.claude/`.
- **.env** — משתני סביבה אמיתיים (לא מועלה ל-git). כולל: `ANTHROPIC_API_KEY`, `CEO_MODEL`, `AGENT_MODEL`, `MAX_TOKENS`, `TEMPERATURE`, `LOG_LEVEL`.
- **.env.example** — תבנית ציבורית של משתני הסביבה עם ערכי ברירת מחדל.
- **.gitignore** — מוחיל `.env`, `__pycache__`, `*.pyc`, `.DS_Store`.
- **.obsidian/** — תצורת Obsidian: `app.json`, `appearance.json`, `core-plugins.json`, `workspace.json`. כל הפרויקט מוגדר כ-vault.
- **.claude/agents/**, **.claude/commands/**, **.claude/skills/** — תיקיות ריקות (`.gitkeep`) שמיועדות להגדרות סוכנים, פקודות slash, וסקילים מותאמים לפרויקט.

## Open Questions

- הגדרות הסוכנים (agents) עדיין לא נוצרו — CLAUDE.md מציין "יוגדרו בהמשך"
- `ANTHROPIC_API_KEY` ב-.env ריק — יש למלא לפני הרצת הפרויקט

## Session Log

### 2026-05-06 — יצירת תשתית פרויקט בסיסית [shipped]

- **What was done:** נוצרו CLAUDE.md, .env, .env.example, .gitignore; הפרויקט הוגדר כ-Obsidian vault (.obsidian/ קיים)
- **Decisions:** CEO_MODEL=claude-opus-4-7, AGENT_MODEL=claude-sonnet-4-6 כברירות מחדל
- **Notes / Caveats:** .env לא יועלה ל-GitHub (מוחרג ב-.gitignore)
- **Related:** [[project-documentation-mapping]], [[skill-obsidian-vault-workflow]]
