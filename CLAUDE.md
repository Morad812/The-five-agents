# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

**The Five Agents** — מערכת סוכנים ליצירת תוכן, מנוהלת על ידי סוכן ראשי (CEO) המוביל צוות של סוכנים מתמחים. הסוכנים ותפקידיהם יוגדרו בהמשך.

## Workflow — Obsidian Vault

**חובה:** בתחילת כל session ולפני כל משימה, הפעל את סקיל `obsidian-vault-workflow`.

הסקיל מנחה:
1. **Phase 1 (לפני משימה):** זיהוי topic → חיפוש קובץ קיים ב-`vault/Meeting Notes/` → קריאת session logs קודמים
2. **Phase 2 (אחרי משימה):** כתיבת/עדכון קובץ topic עם session log מתויך ו-wikilinks

ה-vault נמצא ב-`vault/` — ארבע תיקיות: `Meeting Notes/`, `Content Briefs/`, `Publishing Log/`, `Brand Guidelines/`.

## Project Structure

```
.claude/
├── agents/    # הגדרות סוכנים מותאמים לפרויקט
├── skills/    # סקילים מותאמים לפרויקט
└── commands/  # פקודות slash מותאמות לפרויקט

vault/
├── Meeting Notes/     # session logs, החלטות ארכיטקטורה, תיעוד קבצים
├── Content Briefs/    # briefs לתכנים
├── Publishing Log/    # logs של פרסומים
└── Brand Guidelines/  # הנחיות טון ועיצוב
```
