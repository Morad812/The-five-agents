# Meeting Notes — Index

תיקייה זו מכילה logs של sessions, החלטות ארכיטקטורה, ותיעוד כל קבצי הפרויקט.

## Topics

- [[agent-reuven]] — סוכן המנכ"ל (CEO Orchestrator): מנהל פייפליין טורי של 4 סוכני משנה
- [[yuval-image-agent]] — סוכן קריאייטיב ליצירת תמונות: workflow, reference/, outputs/, gpt-image-gen skill
- [[agent-yael]] — סוכנת כתיבת תוכן LLM-only: שכתוב מאמרים, IMAGE_NEEDED placeholders, Content/ → Output/
- [[agent-chen]] — סוכנת מחקר רשת: מוצאת מקורות, מסננת לפי איכות, מכינה קלט ליעל ב-Content/
- [[project-documentation-mapping]] — מיפוי מלא של כל קבצי הפרויקט לקבצי vault; session יצירת ה-vault
- [[project-config-files]] — CLAUDE.md, .env, .gitignore, .obsidian/, .claude/ (תשתית הפרויקט)
- [[skill-brainstorming]] — סקיל: חקירת כוונת משתמש ועיצוב לפני מימוש; כולל Visual Companion
- [[skill-dispatching-parallel-agents]] — סקיל: הפעלת מספר subagents במקביל למשימות עצמאיות
- [[skill-executing-plans]] — סקיל: ביצוע תכנית מימוש ב-session נפרד עם checkpoints
- [[skill-finishing-development-branch]] — סקיל: סיום branch ובחירת גישת שילוב (merge/PR/מחיקה)
- [[skill-receiving-code-review]] — סקיל: קבלת סקירת קוד עם גישה טכנית ביקורתית
- [[skill-requesting-code-review]] — סקיל: הפעלת סוכן-סקירה עם תבנית code-reviewer.md
- [[skill-subagent-driven-development]] — סקיל: ביצוע תכנית עם subagent לכל משימה + סקירה דו-שלבית
- [[skill-systematic-debugging]] — סקיל: דיבאג מובנה ב-4 שלבים; כולל טכניקות עזר נפרדות
- [[skill-test-driven-development]] — סקיל: Red-Green-Refactor קפדני; כולל testing-anti-patterns
- [[skill-using-git-worktrees]] — סקיל: יצירת סביבת עבודה מבודדת לפני פיתוח
- [[skill-using-superpowers]] — סקיל: כללי שימוש בפלאגין Superpowers; כולל מיפויי כלים לפלטפורמות אחרות
- [[skill-verification-before-completion]] — סקיל: אימות חובה לפני כל הצהרת השלמה
- [[skill-writing-plans]] — סקיל: כתיבת תכניות מימוש מפורטות עם קוד אמיתי בכל step
- [[skill-writing-skills]] — סקיל: יצירה ובדיקה של סקילים (TDD applied to documentation)
- [[skill-obsidian-vault-workflow]] — סקיל: פרוטוקול vault חובה — לפני ואחרי כל משימה
- [[skill-obsidian-markdown]] — סקיל: תחביר Obsidian Flavored Markdown (wikilinks, callouts, embeds)
- [[skill-obsidian-bases]] — סקיל: יצירת קבצי .base לתצוגות בסיסי-נתונים של ה-vault
