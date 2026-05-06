# Agent Guy — QA, סוגר הלולאה

## Overview
גיא הוא הסוכן החמישי והאחרון במערכת "The Five Agents". תפקידו לבדוק כל תוצר שיוצא מהפייפליין לפני שהוא מגיע למשתמש. הוא רץ אוטומטית בסוף כל pipeline תוכן, בודק רלוונטיות לבריף, סגנון, שלמות מבנית, תמונות ושלמות טכנית — ומחזיר פסיקה ברורה לראובן. הוא הסוכן היחיד המורשה לדחות תוצר. ראובן מנהל לולאת retry עד 3 סבבים. הקובץ הקנוני: `.claude/agents/guy.md`. תיקיית עבודה: `guy/`, דוחות: `guy/QA_Reports/`.

## Open Questions
- האם לאפשר לגיא לבדוק תוצרים ידנית (ad-hoc), לא רק דרך הפייפליין?
- האם דוחות QA צריכים להיות git-tracked, או .gitignore?

## Session Log

### 2026-05-06 — יצירה ראשונית [planned]
- **What was done:** הוגדר סוכן גיא — קובץ agent קנוני, pointer doc, תיקיית QA_Reports/. עודכן reuven.md: הוספת גיא לטבלת הסוכנים, section "הפעלת גיא", פרוטוקול QA Loop (3 סבבים עם escalation), עדכון חוק הברזל לפייפליין 1→2→3→4→5.
- **Decisions:** claude-sonnet-4-6 (עקבי עם שאר הצוות). Tools: Read/Glob/Grep/Write בלבד — גיא read-mostly, כותב רק דוחות. לולאת retry מקסימום 3 סבבים: סבב 3 מחזיר שליטה למשתמש. גיא לא מחזיר לסוכנים ישירות — רק לראובן (ארכיטקטורת Claude Code).
- **Related:** [[agent-reuven]], [[agent-yael]], [[yuval-image-agent]], [[agent-chen]]
