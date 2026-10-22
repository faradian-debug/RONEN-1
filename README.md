# RONEN-1 — יומן מטופלים

תוכנה לניהול מטופלים, טיפולים ותשלומים, על בסיס גיליון האקסל המקורי:
שם מטופל, קוד, תאריך טיפול, תאריך תשלום, עלות, סכום ששולם, אמצעי תשלום ויתרת חוב.

- כניסה עם חשבון Google; כל משתמש רואה רק את הנתונים שלו (`firestore.rules`).
- הנתונים נשמרים ב-Cloud Firestore בפרויקט Firebase `ronen-1`.
- ייבוא מהגיליון הקיים כקובץ CSV וייצוא חזרה ל-CSV.

## מבנה

| קובץ | תפקיד |
| --- | --- |
| `public/index.html` | התוכנה עצמה |
| `public/firebase-config.js` | הגדרות ה-Web App מהקונסולה של Firebase |
| `firestore.rules` | חוקי אבטחה למסד הנתונים |
| `firebase.json`, `.firebaserc` | הגדרות Firebase Hosting |

## העלאה לאוויר

```bash
npm install -g firebase-tools
firebase login
firebase deploy
```

נתוני מטופלים לעולם לא נשמרים במאגר הזה. קובצי CSV ו-Excel חסומים ב-`.gitignore`.
