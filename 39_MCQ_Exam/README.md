# ZI MCQ Exam — Online test & admission

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

কোচিং, ভর্তি কোচিং ও স্কুল-কলেজের জন্য: প্রশ্ন ব্যাংক, টাইমারসহ অনলাইন MCQ পরীক্ষা, নেগেটিভ মার্কিং, মেধা তালিকা, প্রশ্ন বিশ্লেষণ, প্রবেশপত্র, সেট A/B প্রশ্নপত্র ও উত্তরমালা, পরীক্ষার্থীদের জন্য আলাদা পরীক্ষার পোর্টাল।

- **Online demo (office app):** https://zi-exam-demo.vercel.app → কোচিংয়ের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Candidate exam portal:** https://zi-exam-demo.vercel.app/exam.html (in the demo it uses the data on the same browser — open the office demo first).
- **Bangla tutorial video:** `video/ZI-MCQ-Exam-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder (office app). **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/` (index.html = office, exam.html = portal).
- **Online exams from home:** `supabase/exam_portal.sql` (run after `zi_sync.sql` in the client's Supabase project; steps are in the app's "Exam portal" page).

## Features
- **Question bank:** subject, chapter, question, 4 options (ক খ গ ঘ / A B C D), right answer, explanation, difficulty. **Paste many at once** from Word / a book / PDF copy ("১. … ক) … খ) … উত্তর: খ") with a live preview; search and filter by subject / chapter.
- **Exams:** title, batch, start & end time (live window), duration, marks per question, negative marking (e.g. 0.25), pass mark, access code, shuffled question order per candidate, when to show answers (right after submit / after the exam ends / never), instructions, draft or published. Questions picked at random from a subject / chapter or chosen by hand.
- **Exam portal (exam.html):** candidates register with mobile + PIN (get a roll no), see live / upcoming exams with countdown, enter the access code, sit the exam with a countdown timer and question palette; answers are kept on the phone and saved to the server every 30 s; auto-submit when time is up; one attempt only. Result with score, pass/fail, merit position, right / wrong / skipped and answer review with explanations; public merit list after the end.
- **Results:** automatic merit list (score, then time), average, highest, pass rate; **question analysis** (% right and how many picked each option); result card print; send results by SMS / WhatsApp.
- **Hall exams:** admit cards (2 per A4, with rules and photo box), question paper in 2 columns with set A / B (different orders) and answer keys, merit list print.
- **Candidates:** roll, school / college, batch, CSV import, each candidate's history.
- **Online (cloud) mode:** the server grades papers and enforces the timer; answer keys never reach the browser (tested with 31 automated checks: `apps/exam/test-sql.mjs`).
- Bangla/English, dark mode, PIN lock, backup, offline office app; optional cloud sync (Supabase).

## Needs from the client
- For candidates to sit exams **from home**, the client needs a free Supabase project (setup steps in the app) and the app published online (e.g. Vercel). Without it, the portal works on the centre's own computers / exam hall. Automatic bulk SMS would need an SMS gateway account; online fee collection (bKash merchant API) is not included.
