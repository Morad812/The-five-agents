---
name: obsidian-vault-workflow
type: skill
associated: Superpowers Plugin + פרויקט זה
files:
  - .claude/skills/obsidian-vault-workflow/SKILL.md
---

# Skill: Obsidian Vault Workflow

## Overview

פרוטוקול חובה לניהול זיכרון ארוך-טווח של הפרויקט ב-Obsidian vault. שני שלבים: **Phase 1 (לפני משימה)** — זיהוי topic, חיפוש קובץ קיים, קריאת Meeting Notes אחרונים; **Phase 2 (אחרי משימה)** — כתיבת/עדכון קובץ topic עם session log מתויך ו-wikilinks. מבנה vault: `Meeting Notes/`, `Content Briefs/`, `Publishing Log/`, `Brand Guidelines/`. כל תיקייה כוללת `_index.md`. המשתמש ביקש שיופעל בתחילת כל session ופקודה.

## Open Questions

- הגדרת hook ב-settings.json להפעלה אוטומטית בתחילת כל session — עדיין לא בוצע

## Session Log

### 2026-05-06 — תיעוד מבנה הפרויקט + הגדרת vault [shipped]

- **What was done:** נוצרה תשתית ה-vault המלאה (`vault/Meeting Notes/`, `Content Briefs/`, `Publishing Log/`, `Brand Guidelines/`) עם קבצי תיעוד לכל קובץ בפרויקט
- **Decisions:** הוחלט ליצור topic file נפרד לכל סקיל (ולא לקבץ אותם) כדי לאפשר wikilinks ספציפיים
- **Notes / Caveats:** המשתמש ביקש שסקיל זה יופעל אוטומטית — יש להגדיר hook ב-.claude/settings.json
- **Related:** [[project-documentation-mapping]], [[skill-obsidian-markdown]], [[skill-obsidian-bases]]
