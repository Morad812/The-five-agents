---
name: writing-skills
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/writing-skills/SKILL.md
  - .claude/skills/writing-skills/anthropic-best-practices.md
  - .claude/skills/writing-skills/persuasion-principles.md
  - .claude/skills/writing-skills/testing-skills-with-subagents.md
  - .claude/skills/writing-skills/graphviz-conventions.dot
  - .claude/skills/writing-skills/render-graphs.js
  - .claude/skills/writing-skills/examples/CLAUDE_MD_TESTING.md
---

# Skill: Writing Skills

## Overview

TDD מיושם על תיעוד תהליכים — מנחה כיצד ליצור, לערוך ולאמת סקילים. מחזור: RED (הרץ תרחיש ללא הסקיל → תעד כשלים), GREEN (כתוב סקיל מינימלי), REFACTOR (סגור פרצות). קבצי עזר: `anthropic-best-practices.md` — הנחיות רשמיות מ-Anthropic; `persuasion-principles.md` — מחקר על עמידות בפני rationalization; `testing-skills-with-subagents.md` — מתודולוגיית בדיקה; `graphviz-conventions.dot` — כללי עיצוב דיאגרמות; `render-graphs.js` — סקריפט לרינדור SVG.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `writing-skills` כולל כל קבצי העזר
- **Decisions:** `CLAUDE_MD_TESTING.md` בתיקיית `examples/` הוא דוגמה לבדיקת סקיל — לא מסמך תצורה
- **Notes / Caveats:** CSO (Claude Search Optimization) קריטי — ה-description קובע אם Claude יטעין את הסקיל
- **Related:** [[skill-test-driven-development]], [[skill-brainstorming]], [[project-documentation-mapping]]
