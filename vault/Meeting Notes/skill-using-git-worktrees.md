---
name: using-git-worktrees
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/using-git-worktrees/SKILL.md
---

# Skill: Using Git Worktrees

## Overview

מנחה Claude ליצירת סביבת עבודה מבודדת לפני מימוש feature. תהליך: (1) זיהוי אם כבר בתוך worktree — אם כן, דלג; (2) שימוש בכלי native אם קיים; (3) fallback ל-`git worktree add` ידנית. בחירת תיקייה לפי סדר עדיפויות: הוראות משתמש > `.worktrees/` קיים > גלובלי > ברירת מחדל `.worktrees/`. מחייב אימות `.gitignore` לפני יצירה, הגדרת dependencies, ואימות baseline tests.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `using-git-worktrees`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** הפרויקט הנוכחי אינו משתמש ב-worktrees — הסקיל רלוונטי כשיתחיל מימוש פיצ'רים
- **Related:** [[skill-finishing-development-branch]], [[skill-executing-plans]], [[project-documentation-mapping]]
