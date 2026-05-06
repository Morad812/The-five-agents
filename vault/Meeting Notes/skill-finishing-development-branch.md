---
name: finishing-a-development-branch
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/finishing-a-development-branch/SKILL.md
---

# Skill: Finishing a Development Branch

## Overview

מנחה Claude לסיים עבודה על branch ולהחליט כיצד לשלב אותה. תהליך: אימות בדיקות → זיהוי סביבה (worktree/repo רגיל) → הצגת 4 אפשרויות (merge מקומי / PR / שמירה / מחיקה) → ביצוע הבחירה → ניקוי worktree במידת הצורך. מחייב אישור מפורש ל-Option 4 (מחיקה). נקרא בסוף כל `subagent-driven-development` ו-`executing-plans`.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `finishing-a-development-branch`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** הסקיל מבדיל בין worktree בניהול Superpowers לבין worktree בניהול חיצוני — רק הראשון מנוקה אוטומטית
- **Related:** [[skill-executing-plans]], [[skill-subagent-driven-development]], [[skill-using-git-worktrees]], [[project-documentation-mapping]]
