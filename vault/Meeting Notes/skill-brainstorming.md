---
name: brainstorming
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/brainstorming/SKILL.md
  - .claude/skills/brainstorming/visual-companion.md
  - .claude/skills/brainstorming/spec-document-reviewer-prompt.md
  - .claude/skills/brainstorming/scripts/server.cjs
  - .claude/skills/brainstorming/scripts/frame-template.html
  - .claude/skills/brainstorming/scripts/helper.js
  - .claude/skills/brainstorming/scripts/start-server.sh
  - .claude/skills/brainstorming/scripts/stop-server.sh
---

# Skill: Brainstorming

## Overview

הסקיל הזה מחייב שימוש לפני כל עבודה יצירתית — יצירת פיצ'רים, קומפוננטות, או כל שינוי התנהגות. הוא מנחה Claude לחקור כוונת המשתמש, דרישות ועיצוב לפני מימוש. התהליך: הצגת 2-3 גישות → אישור עיצוב → כתיבת מסמך spec → העברה ל-`writing-plans`. כולל מצב "Visual Companion" שמפעיל שרת HTTP מקומי להצגת מוקאפים ודיאגרמות בדפדפן.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `brainstorming` כחלק ממיפוי כלל הקבצים ב-vault
- **Decisions:** קובץ ה-SKILL.md הוא המסמך הראשי; הסקריפטים תומכים ב-Visual Companion בלבד
- **Notes / Caveats:** הסקריפטים בתיקיית `scripts/` משמשים אך ורק להפעלת שרת ה-Visual Companion המקומי — אינם חלק מהיגיון הסקיל עצמו
- **Related:** [[skill-writing-plans]], [[skill-using-superpowers]], [[project-documentation-mapping]]
