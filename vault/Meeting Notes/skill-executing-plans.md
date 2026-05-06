---
name: executing-plans
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/executing-plans/SKILL.md
---

# Skill: Executing Plans

## Overview

מנחה Claude לטעון ולבצע תכנית מימוש קיימת (שנוצרה ע"י `writing-plans`) ב-session נפרד עם נקודות בדיקה. התהליך: טעינת התכנית → סקירה ביקורתית → ביצוע משימה אחת בכל פעם → דיווח. אלטרנטיבה ל-`subagent-driven-development` כשעדיף session נפרד ולא subagents בתוך אותו session. מסתיים תמיד ב-`finishing-a-development-branch`.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `executing-plans`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** מומלץ להשתמש ב-`subagent-driven-development` במקום זה כשיש תמיכה בסוכני-משנה — איכות גבוהה יותר
- **Related:** [[skill-subagent-driven-development]], [[skill-writing-plans]], [[skill-finishing-development-branch]], [[project-documentation-mapping]]
