---
name: receiving-code-review
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/receiving-code-review/SKILL.md
---

# Skill: Receiving Code Review

## Overview

מנחה Claude כיצד להגיב לסקירת קוד שהתקבלה — ממשפך ריגשי (performative) לגישה טכנית ביקורתית. הכלל: לעולם לא "אתה צודק לגמרי!" — במקום זה לאמת, לבדוק מול הקוד, ולדחות בנימוק טכני אם לא נכון. מחייב בדיקת YAGNI לפני מימוש הצעות מ-reviewers חיצוניים. מיועד במיוחד כשפידבק לא ברור או מפוקפק מבחינה טכנית.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `receiving-code-review`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** הסקיל מדגיש שסקירה חיצונית היא הצעה להעריך, לא פקודה לבצע
- **Related:** [[skill-requesting-code-review]], [[skill-verification-before-completion]], [[project-documentation-mapping]]
