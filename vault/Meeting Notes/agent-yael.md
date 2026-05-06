# agent-yael

## Overview

יעל היא סוכנת כתיבת תוכן LLM-only במערכת "The Five Agents". תפקידה לשכתב מאמרי גלם מ-`Content/` בסגנון המותג המוגדר ב-`yael/style-guide.md` ו-`yael/reference/`. היא שומרת תוצרים ב-`Output/`, מעבירה מקורות ל-`Content/Ready/`, ומשאירה `{{IMAGE_NEEDED: "..."}}` placeholders עבור יובל. ראובן הוא ה-orchestrator שמפעיל אותה ומטפל בחיבור בינה לבין יובל. הסוכן מוגדר ב-`.claude/agents/yael.md` ותיקיית העבודה שלו היא `yael/`.

## Open Questions

- האם `yael/style-guide.md` מולא עם הסגנון האמיתי של המותג? (נוצר כ-template ריק)
- האם `yael/reference/` מאוכלס בדוגמאות טקסט? (ריק כרגע)
- מה סדר הפייפליין המלא של ראובן? (יעל היא סוכן כתיבה — מתי בדיוק היא רצה ביחס לסוכני מחקר/תכנון/עריכה שטרם הוגדרו?)

## Session Log

### 2026-05-06 — יצירה ראשונית [planned]

- **What was done:** הוגדר סוכן יעל המלא — קובץ agent, workflow 6-שלבים, מנגנון IMAGE_NEEDED, כלי עזר, גבולות תפקיד. נוצרו תיקיות Content/, Content/Ready/, Output/, yael/reference/. נוצרו style-guide.md (template) ו-agent.md (pointer doc). עודכן ראובן עם טבלת סוכנים, section "הפעלת יעל", ופרוטוקול IMAGE_NEEDED.
- **Decisions:** LLM-only by design (Read/Write/Edit/Glob/Grep בלבד) — מונע מיעל לגשת ל-API או להפעיל תהליכים חיצוניים. `{{IMAGE_NEEDED: "..."}}` כ-API מוגדר בין יעל ליובל — ראובן הוא הבלעדי שמתרגם את ה-interface הזה. Content/Ready/ כ-ACK mechanism מונע עיבוד כפול.
- **Notes / Caveats:** יעל מוכנה טכנית אך לא מוכנה תפעולית — חייבים למלא את style-guide.md ולהוסיף reference לפני שימוש ראשון. סדר הפייפליין הכולל של ראובן עדיין לא מוגדר (4 סוכנים — רק יובל ויעל קיימים).
- **Related:** [[agent-reuven]], [[yuval-image-agent]]
