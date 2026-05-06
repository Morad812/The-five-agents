# Agent Reuven — CEO Orchestrator

## Overview
ראובן הוא סוכן המנכ"ל של מערכת "The Five Agents". תפקידו לנהל פייפליין טורי קבוע של 4 סוכני משנה (Agent 1 → 2 → 3 → 4), לבקש הבהרות ממשתמש כשמשימה אינה ברורה, לדווח לפני/אחרי/בכשל, ולטפל בכשלים לפי פרוטוקול Retry → Diagnose → Halt. ראובן לא מבצע משימות בעצמו — הוא מאציל בלבד. הקובץ נמצא ב-`.claude/agents/reuven.md`. הסוכן משתמש ב-`claude-sonnet-4-6` ויש לו גישה לכלים: Task, Read, Write, Edit, Bash, Glob, Grep.

## Open Questions
- ארבעת סוכני המשנה (Agent 1–4) טרם הוגדרו — יש להגדיר תפקיד וקובץ לכל אחד
- האם להשתמש ב-`claude-opus-4-7` לראובן (כפי ש-.env מגדיר CEO_MODEL) או להישאר על Sonnet?
- מה סדר הפייפליין המדויק? (מחקר → תכנון → כתיבה → עריכה? תלוי ב-use case)
- האם ראובן אמור לשמור state בין sessions או רק בתוך session אחת?

## Session Log

### 2026-05-06 — יצירת agent ראובן [shipped]
- **What was done:** נוצר `.claude/agents/reuven.md` עם system prompt מלא בעברית — זהות, חוקי ברזל, פרוטוקול קבלת משימה (5 שלבים), תבנית הפעלת סוכן עם context block, פרוטוקול דיווח emoji-based, פרוטוקול טיפול בכשלים, גבולות תפקיד ודוגמאות. עודכן `CLAUDE.md` עם הנחיית ניתוב ("כל משימה דרך ראובן").
- **Decisions:** בחרנו `claude-sonnet-4-6` (לא Opus) כי Orchestration לא דורש יכולות reasoning מעמיקות — רק ניהול תהליך. ניתן לשדרג בהמשך. הקובץ הוא קובץ שטוח ב-`.claude/agents/` (לא תיקייה) בהתאם למבנה agent files של Claude Code.
- **Notes / Caveats:** סוכני המשנה (Agent 1–4) עדיין לא הוגדרו — ראובן לא יכול לפעול בייצור עד שיש לו למי להאציל.
- **Related:** [[project-config-files]], [[project-documentation-mapping]]
