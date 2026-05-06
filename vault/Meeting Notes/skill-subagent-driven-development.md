---
name: subagent-driven-development
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/subagent-driven-development/SKILL.md
  - .claude/skills/subagent-driven-development/implementer-prompt.md
  - .claude/skills/subagent-driven-development/spec-reviewer-prompt.md
  - .claude/skills/subagent-driven-development/code-quality-reviewer-prompt.md
---

# Skill: Subagent-Driven Development

## Overview

הגישה המומלצת לביצוע תכניות מימוש ב-session הנוכחי. כל משימה מטופלת ע"י סוכן-משנה חדש עם context נקי. לאחר כל משימה — שני שלבי סקירה: (1) spec compliance reviewer, (2) code quality reviewer. שלושה תבניות prompt בתיקייה: `implementer-prompt.md`, `spec-reviewer-prompt.md`, `code-quality-reviewer-prompt.md`. מסתיים ב-`finishing-a-development-branch`.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `subagent-driven-development` כולל שלוש תבניות ה-prompt
- **Decisions:** שלושת קבצי ה-prompt הם תבניות בלבד — לא סקילים עצמאיים; הם מועברים לסוכנים שמופעלים
- **Notes / Caveats:** לא להפעיל מספר implementer subagents במקביל — יגרמו קונפליקטים בעריכת קבצים
- **Related:** [[skill-executing-plans]], [[skill-requesting-code-review]], [[skill-test-driven-development]], [[project-documentation-mapping]]
