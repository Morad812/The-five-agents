---
name: systematic-debugging
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/systematic-debugging/SKILL.md
  - .claude/skills/systematic-debugging/root-cause-tracing.md
  - .claude/skills/systematic-debugging/defense-in-depth.md
  - .claude/skills/systematic-debugging/condition-based-waiting.md
  - .claude/skills/systematic-debugging/condition-based-waiting-example.ts
  - .claude/skills/systematic-debugging/find-polluter.sh
  - .claude/skills/systematic-debugging/CREATION-LOG.md
  - .claude/skills/systematic-debugging/test-academic.md
  - .claude/skills/systematic-debugging/test-pressure-1.md
  - .claude/skills/systematic-debugging/test-pressure-2.md
  - .claude/skills/systematic-debugging/test-pressure-3.md
---

# Skill: Systematic Debugging

## Overview

מסגרת דיבאג מובנית ב-4 שלבים: (1) Root Cause Investigation, (2) Pattern Analysis, (3) Hypothesis & Testing, (4) Implementation. חוק ברזל: אסור לתקן לפני הבנת הסיבה השורשית. קבצי עזר: `root-cause-tracing.md` — טכניקת מעקב לאחור; `defense-in-depth.md` — הוספת validation בשכבות; `condition-based-waiting.md` + `example.ts` — החלפת timeouts בתנאים; `find-polluter.sh` — סקריפט למציאת test שמזהם אחרים. קבצי `test-*.md` ו-`CREATION-LOG.md` הם חלק מהתפתחות הסקיל (TDD applied to skills).

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `systematic-debugging` כולל כל קבצי העזר
- **Decisions:** קבצי `test-pressure-*.md` ו-`test-academic.md` הם תרחישי בדיקה שנוצרו בפיתוח הסקיל — אינם מיועדים לשימוש ישיר
- **Notes / Caveats:** אחרי 3 ניסיונות כושלים של תיקון, הסקיל מנחה לעצור ולשאול שאלות ארכיטקטוניות
- **Related:** [[skill-test-driven-development]], [[skill-verification-before-completion]], [[project-documentation-mapping]]
