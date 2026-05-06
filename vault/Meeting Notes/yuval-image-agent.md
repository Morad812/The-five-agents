# yuval — Creative Image Agent

## Overview

יובל הוא הסוכן הקריאייטיב של מערכת "The Five Agents". תפקידו ליצור תמונות עם עקביות ויזואלית על ידי קריאת תמונות reference מ-`yuval/reference/`, חילוץ סגנון ויזואלי, ובניית prompt שמשלב בין הבקשה הנוכחית לאסתטיקה הקיימת. הסוכן מפעיל את skill `gpt-image-gen` (OpenAI Images API, model: gpt-image-2) ושומר תוצרים ב-`yuval/outputs/` בפורמט `YYYY-MM-DD-<slug>.png` עם sibling `.txt` של ה-prompt.

**מבנה היברידי:** `.claude/agents/yuval.md` — הגדרה קנונית שקלוד קורא; `yuval/` בשורש הפרויקט — תיקיית עבודה עם `reference/`, `outputs/`, ו-pointer docs לבני אדם. ראובן מנתב בקשות תמונה ליובל לפי trigger keywords.

## Open Questions

- האם `yuval/outputs/` צריך להיות git-ignored? (תמונות PNG גדולות עלולות לנפח את ה-repo)
- מה פורמט תמונות reference מתאים? (jpg, png, webp — כולם תואמים Claude multimodal)
- האם להוסיף metadata לשם הקובץ (e.g., קטגוריה: banner/social/illustration)?

## Session Log

### 2026-05-06 — יצירת יובל וסקיל gpt-image-gen [shipped]
- **What was done:** נוצר `.claude/agents/yuval.md` עם workflow מלא (10 שלבים): סריקת reference → חילוץ סגנון → בניית prompt → טעינת API key → קריאה ל-gpt-image-2 → decode (jq/Python fallback) → שמירת prompt log → אימות → דיווח. נוצר `.claude/skills/gpt-image-gen/SKILL.md` כמעטפת עצמאית לקריאת OpenAI Images API (ניתן לשימוש גם על ידי סוכנים אחרים). נוצרה תיקיית עבודה `yuval/` עם `reference/`, `outputs/`, `agent.md`, `skill.md`. עודכן `reuven.md` עם טבלת סוכני משנה ותבנית הפעלה ליובל.
- **Decisions:** Python fallback לdecode (במקום jq בלבד) כי jq לא מותקן בכל סביבה (Git Bash). `gpt-image-2` כפי שנקבע בספציפיקציה. הסוכן משתמש ב-`claude-sonnet-4-6` — עקבי עם `AGENT_MODEL` בפרויקט. `OPENAI_API_KEY` נוסף ל-`.env` ול-`.env.example`.
- **Notes / Caveats:** אין בדיקה חיה של ה-API (מפתח ריק ב-.env). יש למלא `OPENAI_API_KEY` לפני שימוש ראשון. תמונות ב-`yuval/reference/` ריקות בינתיים — יובל יפעל ללא עקביות ויזואלית עד שמוסיפים reference.
- **Related:** [[agent-reuven]], [[project-config-files]]
