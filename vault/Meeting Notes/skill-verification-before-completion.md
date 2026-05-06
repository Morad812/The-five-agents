---
name: verification-before-completion
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/verification-before-completion/SKILL.md
---

# Skill: Verification Before Completion

## Overview

אוסר על Claude להצהיר על השלמת עבודה ללא הרצה אמיתית של פקודת אימות. חוק ברזל: ראיות לפני טענות — תמיד. התהליך: זהה פקודת אימות → הרץ → קרא output מלא → רק אז טען. הסקיל חל על כל ניסוח הצלחה: "בוצע", "עובד", "עבר", "תקין" — כולם מחייבים ריצת אימות. נוצר בעקבות 24 אירועי כשל שבהם Claude הצהיר על הצלחה ללא אימות.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `verification-before-completion`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** חל גם על תוצאות של subagents — גם אם הסוכן דיווח "הצלחה", יש לאמת בדיף
- **Related:** [[skill-test-driven-development]], [[skill-systematic-debugging]], [[project-documentation-mapping]]
