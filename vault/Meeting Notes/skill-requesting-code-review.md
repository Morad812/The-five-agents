---
name: requesting-code-review
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/requesting-code-review/SKILL.md
  - .claude/skills/requesting-code-review/code-reviewer.md
---

# Skill: Requesting Code Review

## Overview

מנחה Claude להפעיל סוכן-סקירה (code reviewer subagent) עם context מדויק לבדיקת עבודה שהושלמה לפני שהיא מתקדמת. קבצי הסקיל: `SKILL.md` — ההוראות הראשיות; `code-reviewer.md` — תבנית ה-prompt שמועברת לסוכן הסקירה. הסוכן מקבל git SHAs (base ו-HEAD), תיאור מה נבנה, ומחזיר דירוג בעיות: Critical / Important / Minor.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `requesting-code-review` כולל `code-reviewer.md`
- **Decisions:** `code-reviewer.md` הוא תבנית prompt בלבד — לא סקיל עצמאי
- **Notes / Caveats:** יש לקרוא סקירה אחרי כל משימה ב-subagent-driven-development, לא רק בסוף
- **Related:** [[skill-receiving-code-review]], [[skill-subagent-driven-development]], [[project-documentation-mapping]]
