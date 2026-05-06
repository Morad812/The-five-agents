---
name: test-driven-development
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/test-driven-development/SKILL.md
  - .claude/skills/test-driven-development/testing-anti-patterns.md
---

# Skill: Test-Driven Development

## Overview

מנחה Claude למחזור Red-Green-Refactor קפדני: כתוב בדיקה כושלת → ראה אותה נכשלת → כתוב קוד מינימלי → ודא שהיא עוברת → refactor. חוק ברזל: אסור לכתוב קוד ייצור לפני בדיקה כושלת. `testing-anti-patterns.md` — מסמך נפרד המתאר מלכודות נפוצות (בדיקת mock במקום קוד אמיתי, מתודות test-only בקלאסי ייצור). הסקיל מחייב מחיקת קוד שנכתב ללא בדיקה קודמת — ללא יוצא מן הכלל.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `test-driven-development`
- **Decisions:** `testing-anti-patterns.md` הוא מסמך עזר שמופנה מ-SKILL.md כ-`@testing-anti-patterns.md`
- **Notes / Caveats:** הסקיל מחמיר ביותר — "delete means delete", ללא חריגים
- **Related:** [[skill-systematic-debugging]], [[skill-writing-skills]], [[project-documentation-mapping]]
