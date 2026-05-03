# שאלון בקשות מרתון למורים

## מטרת הפרויקט
איסוף בקשות מורים לימים מרוכזים (מרתון) לקראת עונת הבגרויות.
המורה בוחר תאריכים על לוח שנה אינטראקטיבי שמציג במקביל את הבגרויות הקיימות,
כך שניתן לתאם ולמנוע התנגשויות.

## טכנולוגיות
- הקובץ `index.html` — טופס עם לוח שנה אינטראקטיבי, HTML סטטי, Vanilla JS
- הקובץ `dashboard.html` — תצוגת לוח שנה עם כל הבקשות + בגרויות, Chart.js
- הקובץ `apps-script.js` — קוד Google Apps Script משותף (נמצא ב-`../גדנע/apps-script.js`)

## Apps Script — פרטים טכניים
- כתובת ה-URL: `https://script.google.com/macros/s/AKfycbyFDlBHn07-bzcBGhok5pVsrFsQcvwspYEf8DF8toXFzog-qhkerIbNc361-Xij3W2VAg/exec`
- שאלון זה שולח `sheetName: 'מרתון'` — הנתונים נשמרים בגיליון "מרתון" בקובץ Sheets
- שיטת שליחה: hidden iframe POST
- שיטת קריאה לדשבורד: JSONP עם פרמטר `callback` ו-`sheetName`

## מקור נתוני הבגרויות
- API של exam11: `https://exam11-next.vercel.app/api/events`
- מחזיר מערך של חודשים עם אירועים, כל אירוע עם `start` בפורמט YYYYMMDD, `cat`, `title`
- קטגוריות רלוונטיות: `bagrut`, `metakonet`

## מבנה הנתונים ב-Google Sheets (גיליון "מרתון")
עמודות: חותמת זמן, שם המורה, מקצוע, תאריכים מבוקשים (JSON array), הצדקה

## עיצוב — Clarity Theme
- רקע: לבן (#FFFFFF), משטחים: #F9FAFB
- אקסנט: טורקיז (#0891B2)
- בגרויות: כחול בהיר (#E0F2FE)
- טקסט: #111111, גבולות: #E5E7EB
- פונט: Heebo

## קהל יעד
מורים בבית הספר נעימת הלב המבקשים ימי מרתון לקראת בגרויות תשפ"ו
