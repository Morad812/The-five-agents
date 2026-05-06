# Agent Chen — חוקרת הרשת

## Overview
חן היא סוכנת המחקר של מערכת "The Five Agents". תפקידה לאסוף מקורות איכותיים ועדכניים מהאינטרנט לפי בקשת ראובן, ולהכינם כחומר גלם ב-`Content/` לשכתוב על ידי יעל. היא שומרת לוג חיפושים ב-`chen/Memory/searches.md` כדי למנוע חיפושים כפולים בתוך 30 יום. הסוכן מוגדר ב-`.claude/agents/chen.md` עם כלים: WebSearch, WebFetch, Read, Write, Edit, Glob, Grep — ללא Bash וללא API חיצוני.

## Open Questions
- האם להוסיף תמיכה בחיפוש בשפות נוספות מעבר לעברית ואנגלית?
- האם לוג ה-searches.md צריך להיות git-tracked, או שמדובר בנתוני working state שעדיף ל-gitignore?
- מה סדר ה-pipeline המלא? (חן היא Agent 3 או Agent 1? כרגע לא מוגדר סדר)

## Session Log

### 2026-05-06 — יצירה ראשונית [planned]
- **What was done:** הוגדר סוכן חן המלא — קובץ agent קנוני (`.claude/agents/chen.md`), pointer doc (`chen/agent.md`), אתחול `chen/Memory/searches.md`. עודכן `reuven.md` — הוספת חן לטבלת הסוכנים עם trigger keywords, סעיף "הפעלת חן" עם context template, ופרוטוקול חן→יעל (המשך אוטומטי לשכתוב בהתאם לבקשה המקורית).
- **Decisions:** LLM+web בלבד (WebSearch/WebFetch) ללא Bash — עקבי עם מדיניות הפרויקט. זיכרון כ-append-only log (לא DB) — פשוט לתחזוקה, מספיק לתרחיש 30-יום. חן אחראית רק ל-Content/ (לא Output/) — ה-handoff הברור הוא "חן מכינה גלם, יעל שוכתבת, ראובן מחליט מה קורה אחרי".
- **Notes / Caveats:** חן מוכנה טכנית. סדר הפייפליין הכולל (Agent 1–4) עדיין לא מוגדר — חן נוספה לטבלה כסוכן מחקר אך מספרה בפייפליין פתוח.
- **Related:** [[agent-reuven]], [[agent-yael]]
