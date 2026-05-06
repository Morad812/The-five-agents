---
name: dispatching-parallel-agents
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/dispatching-parallel-agents/SKILL.md
---

# Skill: Dispatching Parallel Agents

## Overview

מנחה Claude להפעיל מספר סוכני-משנה (subagents) במקביל כאשר יש 2+ משימות עצמאיות ללא תלות הדדית. כל סוכן מקבל context מדויק ומבודד — לא יורש את ה-session הנוכחי. התבנית: זיהוי domains עצמאיים → ניסוח prompt ממוקד לכל סוכן → dispatch מקביל → אינטגרציה של תוצאות. משמש בעיקר לתיקון כשלים במספר קבצי בדיקה בו-זמנית.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `dispatching-parallel-agents`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד ללא קבצי עזר נוספים
- **Notes / Caveats:** יש להשתמש בסקיל זה רק כשהמשימות באמת עצמאיות — אם הן משפיעות על אותם קבצים, לא ניתן להפעיל במקביל
- **Related:** [[skill-subagent-driven-development]], [[skill-executing-plans]], [[project-documentation-mapping]]
