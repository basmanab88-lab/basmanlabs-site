# HandyMan — Demo Video Script for Google OAuth Verification

**Target length:** 2 minutes (max 3)
**Language:** Hebrew narration, English subtitles (Google reviewers are English-speaking)
**Format:** Screen recording + voiceover
**Upload:** YouTube as **Unlisted**, paste URL in Google OAuth verification form

---

## What Google reviewers need to see (mandatory)

1. **Homepage / landing page** — so they see it's a real product with branding
2. **OAuth consent screen with app name, scopes shown** — exact moment the user grants permission
3. **What happens after consent** — the app's actual behavior using the scopes
4. **Each scope being used in a meaningful way** (spreadsheets, drive.file, userinfo)

---

## Scene-by-scene breakdown

### Scene 1 — Intro (0:00 – 0:15)

**Show:** `https://handyman.basmanlabs.com` landing page
**Narration (Hebrew):**
> "HandyMan הוא בוט וואטסאפ לבעלי עסקים קטנים בישראל — קבלנים, פרילנסרים — שמאפשר להם לנהל הוצאות ולקוחות ישירות מהוואטסאפ."

**Subtitle (English):**
> HandyMan is a WhatsApp bot for small business owners in Israel — contractors, freelancers — that helps them manage expenses and clients directly from WhatsApp.

### Scene 2 — Onboarding starts (0:15 – 0:30)

**Show:** User opens WhatsApp, sends "start" to the HandyMan bot. Bot replies with a link.
**Narration:**
> "משתמש חדש שולח 'start' לבוט, ומקבל קישור להרשמה."

**Subtitle:**
> A new user sends "start" to the bot and receives a signup link.

### Scene 3 — Click Sign In with Google (0:30 – 0:45)

**Show:** Click the link → see Connect page → click "התחבר עם Google" button
**Narration:**
> "הקישור פותח את הדף הזה, ששואל את המשתמש להתחבר עם חשבון גוגל שלו, כדי שנוכל ליצור לו גיליון פרטי."

**Subtitle:**
> The link opens this page, which asks the user to sign in with their Google account so we can create a private spreadsheet for them.

### Scene 4 — Google OAuth consent (0:45 – 1:15) ⭐ CRITICAL

**Show:** Google OAuth consent screen. **PAUSE on each scope visibly displayed.**
**Narration (read each scope out loud as it appears):**

> "אנחנו מבקשים גישה לשלוש הרשאות:
>
> אחד — Google Sheets — כדי לכתוב את ההוצאות וההכנסות של המשתמש לגיליון שלו.
>
> שתיים — drive.file — כדי ליצור ולנהל *רק את הקובץ שהאפליקציה יצרה*. אין לנו גישה לקבצים אחרים בדרייב של המשתמש.
>
> שלוש — email ו-profile — כדי לזהות את המשתמש."

**Subtitle:**
> We request three permissions:
> 1. **Google Sheets** — to write the user's expenses and income to their spreadsheet.
> 2. **drive.file** — to create and manage **only files the app itself creates**. We do NOT have access to the user's other Drive files.
> 3. **email and profile** — to identify the user.

### Scene 5 — Sheet creation (1:15 – 1:30)

**Show:** After user approves, a toast: "Creating your spreadsheet..." → user lands on Settings page with link to Sheet → open the Sheet, show 3 tabs (הוצאות, לקוחות, תשלומי לקוחות) with headers.

**Narration:**
> "אחרי אישור, האפליקציה יוצרת גיליון חדש ב-Drive של המשתמש, כותבת בו כותרות לשלוש טבלאות — הוצאות, לקוחות, תשלומים — ומחזירה את הקישור למשתמש."

**Subtitle:**
> After approval, the app creates a new spreadsheet in the user's Drive, writes headers for three tables — expenses, clients, payments — and returns the link to the user.

### Scene 6 — Bot in action (1:30 – 1:50)

**Show:** User sends WhatsApp message to bot: "קניתי ברגים ב-150 שקל" → bot replies with confirmation → open sheet, show the row appeared in הוצאות tab.

**Narration:**
> "מעכשיו, המשתמש שולח הודעות לבוט, והבוט כותב את המידע בגיליון שלו. כל הנתונים שייכים למשתמש — הם בגוגל שיטס שלו."

**Subtitle:**
> From now on, the user sends messages to the bot, and the bot writes the information to their spreadsheet. All data belongs to the user — it's in their own Google Sheet.

### Scene 7 — Outro (1:50 – 2:00)

**Show:** Back to landing page, show privacy policy link in footer.
**Narration:**
> "המידע של המשתמש נשאר אצלו. אנחנו לא משתפים אותו, לא מוכרים אותו, ולא משתמשים בו לפרסום. המדיניות המלאה בלינק."

**Subtitle:**
> The user's data stays with them. We don't share it, sell it, or use it for advertising. Full policy in the link below.

---

## Checklist before recording

- [ ] Close all tabs you don't want on camera
- [ ] Use incognito window so no personal Google accounts leak
- [ ] Test the full flow end-to-end once before recording
- [ ] Record in 1080p minimum
- [ ] Keep mouse movements slow and deliberate
- [ ] Verify audio levels — Google reviewers will listen

## Technical recording tips

- **Tool:** OBS Studio (free) or macOS built-in screen recorder
- **Voiceover:** Record separately with phone in quiet room, sync in post
- **Export:** MP4, 1080p, H.264
- **Duration:** Aim for 2:00 exactly. 3:00 is the absolute max.

## Upload

1. YouTube → **Upload video**
2. Title: `HandyMan — Google OAuth Flow Demo`
3. Description: `Demonstration of HandyMan's OAuth flow and use of Google Sheets + drive.file scopes. Submitted for Google OAuth verification.`
4. Visibility: **Unlisted** (not Private — reviewers won't be able to see it if Private)
5. Copy the URL — you'll paste it in the OAuth verification form.

## Common reviewer pushbacks (prep answers)

- **"Why do you need spreadsheets scope?"** → "To read existing rows for context and write new rows when the user adds expenses/payments via WhatsApp. We cannot achieve this feature with any narrower scope."
- **"Why drive.file and not readonly?"** → "We need to *create* the spreadsheet in the user's Drive on first onboarding, and then write to it. drive.file is the narrowest scope that allows both create and write on app-owned files."
- **"How is data stored?"** → "User's financial data is stored exclusively in their own Google Sheet. Our Supabase database stores only the sheet ID and configuration — not the sheet's contents."
