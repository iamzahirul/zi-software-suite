# ZI Academy — Coaching & Online Course LMS

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

কোচিং সেন্টার ও অনলাইন কোর্সের সফটওয়্যার: কোর্স, ভিডিও/লাইভ ক্লাস, কুইজ, বিকাশ পেমেন্ট যাচাই, QR-সহ সার্টিফিকেট। দুটি অংশ — প্রতিষ্ঠানের অ্যাপ আর শিক্ষার্থীদের পোর্টাল।

- **Online demo — institute app:** https://zi-academy-demo.vercel.app → name din → "স্যাম্পল ডেটা দেখুন".
- **Online demo — student portal:** https://zi-academy-demo.vercel.app/portal.html (same browser-e demo data dekhay; login 01711000001 · PIN 1234).
- **Android APK:** `apk/` folder (institute app). **Laptop:** demo link → Chrome/Edge "Install".
- **Web build:** `web/` folder (admin `index.html` + student `portal.html`).

## Institute app
- Courses: fee, teacher, duration, pass mark, quiz time, publish on/off, certificate on/off, duplicate a course.
- Lessons: YouTube video (unlisted ok), PDF / Drive link, live class (Zoom/Meet), notes, free preview lessons, re-order.
- Quiz builder: MCQ (2–4 options), marks, re-order. Graded automatically.
- Students: phone + portal PIN, guardian, enrollments, payments, results, certificates, WhatsApp fee reminder.
- Enrollments & payments: **bKash/Nagad TrxID verify queue** (duplicate TrxID warning), verify → course opens; manual enrollment with discount and partial payment; money receipt (A5).
- Results & certificates: attempts, pass/fail, auto or manual certificate, **A4 landscape certificate with QR**, verify box.
- Student portal page: link, QR for notice board, WhatsApp share, setup steps. Expenses, reports (summary, course-wise, dues, by method).
- Bangla/English, dark mode, PIN lock, backup/restore, offline.

## Student portal (portal.html)
Course catalog → register with phone + PIN → enroll: bKash number shown, student writes TrxID → after the institute verifies: video lessons, live class link, timed quiz → pass = certificate download → anyone can verify the certificate number / QR online.

## Real students online (one-time setup per client)
1. Client-er jonno free Supabase project (supabase.com).
2. SQL Editor: `_source/zi-software/supabase/zi_sync.sql`, tarpor `lms_portal.sql` run.
3. Authentication → Users → institute email + password.
4. App: Settings → Cloud sync → project URL, anon key, email, password.
5. App: Student portal page → link/QR share. (Android app use korle Settings-e portal address: `https://<their-site>/portal.html`.)

Security: students never get the answer key (quiz graded in the database), paid lessons stay locked until payment is verified, one TrxID cannot be used twice. Tested with `node tools/test-lms-sql.mjs` (20 checks).

## Changelog

### v1.0.1 — 28 Oct 2026
- Mobile numbers and PINs typed in Bangla digits (০১৭…, ১২৩৪) now work — in the institute app and in the student portal login/register.
- Fee entry checks: discount cannot be more than the course fee, a payment cannot be more than the due, no negative amounts, and the same TrxID cannot be used twice.
- Money receipt now shows the course fee, total paid and the correct due *after* this payment (before, a receipt printed right after payment showed the old due).
- Dues are counted the same everywhere: online requests still waiting for TrxID check are no longer shown as due (student list, student page, course-wise report, due list, portal).
- New: edit an enrollment (discount, date, status/cancel), delete a wrongly entered payment, delete a course or student that has no enrollments/payments.
- Changing a student's phone now asks for the portal PIN again (the old PIN would have stopped working).
- "Issue all" certificates skips rejected/waiting enrollments and marks the course completed.
- Quiz: asks before submitting when some questions are unanswered. Percent shows as 33.3% (not 33.30%); certificate percent in Bangla digits.
- Pass rate shows "—" until someone takes the quiz (not 0%); course status shows "Published" instead of the long setting text.
- New course / new student from the dashboard opens the new page; small accessibility labels translated.
