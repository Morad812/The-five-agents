---
name: using-superpowers
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/using-superpowers/SKILL.md
  - .claude/skills/using-superpowers/references/codex-tools.md
  - .claude/skills/using-superpowers/references/copilot-tools.md
  - .claude/skills/using-superpowers/references/gemini-tools.md
---

# Skill: Using Superpowers

## Overview

הסקיל המרכזי של פלאגין Superpowers — מגדיר את כללי השימוש בכלל הסקילים. כלל עיקרי: לפני כל תגובה, בדוק אם סקיל רלוונטי (גם ב-1% סיכוי — בדוק). סדר עדיפויות: הוראות משתמש > Superpowers skills > ברירת מחדל. קבצי reference: `codex-tools.md`, `copilot-tools.md`, `gemini-tools.md` — מיפוי שמות כלים בין פלטפורמות שונות (Codex, GitHub Copilot, Gemini CLI).

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `using-superpowers` כולל קבצי ה-references
- **Decisions:** שלושת קבצי ה-reference הם מיפויי כלים בלבד — לא נחוצים בסביבת Claude Code (שם שמות הכלים זהים)
- **Notes / Caveats:** המשתמש ביקש שסקיל `obsidian-vault-workflow` יופעל בכל תחילת session — ראה [[skill-obsidian-vault-workflow]]
- **Related:** [[skill-obsidian-vault-workflow]], [[project-documentation-mapping]]
