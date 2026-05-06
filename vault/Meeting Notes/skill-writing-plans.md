---
name: writing-plans
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/writing-plans/SKILL.md
  - .claude/skills/writing-plans/plan-document-reviewer-prompt.md
---

# Skill: Writing Plans

## Overview

מנחה Claude לכתיבת תכניות מימוש מפורטות לפני נגיעה בקוד. כל תכנית נשמרת ל-`docs/superpowers/plans/YYYY-MM-DD-<feature>.md`. המבנה: header → file structure → משימות עם steps ברמת דקות (2-5 דקות כל step), קוד מלא בכל step, פקודות מדויקות. `plan-document-reviewer-prompt.md` הוא תבנית לסוכן-בדיקה שסוקר את התכנית. אסור placeholders — כל step צריך קוד אמיתי.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `writing-plans`
- **Decisions:** `plan-document-reviewer-prompt.md` הוא תבנית prompt לסוכן-סקירה של התכנית — לא סקיל עצמאי
- **Notes / Caveats:** הסקיל מסתיים בהצעת שתי גישות ביצוע: subagent-driven (מומלץ) או inline
- **Related:** [[skill-brainstorming]], [[skill-subagent-driven-development]], [[skill-executing-plans]], [[project-documentation-mapping]]
