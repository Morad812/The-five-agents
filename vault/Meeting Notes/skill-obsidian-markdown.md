---
name: obsidian-markdown
type: skill
associated: Superpowers Plugin
files:
  - .claude/skills/obsidian-markdown/SKILL.md
---

# Skill: Obsidian Markdown

## Overview

מדריך ליצירת Obsidian Flavored Markdown — תחביר מורחב מעל CommonMark ו-GFM. מכסה: wikilinks (`[[filename]]`), embeds (`![[file]]`), callouts (`> [!note]`), frontmatter/properties (YAML), תגים (`#tag`), הערות (`%%comment%%`). לא מכסה Markdown סטנדרטי (כותרות, bold, רשימות) — מניח ידיעה קודמת. רלוונטי לכל עבודה עם קבצי `.md` בסביבת Obsidian.

## Open Questions

- none

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט [shipped]

- **What was done:** נוצר קובץ תיעוד לסקיל `obsidian-markdown`
- **Decisions:** הסקיל מורכב מקובץ SKILL.md בלבד
- **Notes / Caveats:** הפרויקט מוגדר כ-Obsidian vault (יש `.obsidian/`) — כל קבצי ה-MD ב-vault משתמשים בתחביר זה
- **Related:** [[skill-obsidian-vault-workflow]], [[skill-obsidian-bases]], [[project-documentation-mapping]]
