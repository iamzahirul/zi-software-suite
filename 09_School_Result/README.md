# ZI School — Result, Admit Card & Fee

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

স্কুল, কিন্ডারগার্টেন ও মাদ্রাসার জন্য: শিক্ষার্থী ভর্তি, পরীক্ষার নম্বর থেকে GPA ফলাফল, নম্বরপত্র, টেবুলেশন শিট, প্রবেশপত্র, সিট স্টিকার, মাসিক বেতন ও অন্যান্য ফি।

- **Online demo:** https://zi-school-demo.vercel.app → স্কুলের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-School-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Classes & subjects:** sections (ক/খ), monthly tuition, subjects with their own full marks and pass marks (e.g. ICT 50, pass 17).
- **Students:** student ID (S-A1001…), class, section, roll (next roll filled in, duplicates blocked), parents, guardian mobile, date of birth, photo, half-free / free studentship. ID cards (8 per A4).
- **Exams:** name, year, classes, routine (or "make routine" one subject a day, skipping Friday).
- **Admit cards** (2 per A4, photo, roll, barcode, subject-wise routine, rules, signatures) — can leave out students with unpaid fees. **Seat stickers** (12 per A4).
- **Marks entry** per class and subject (Enter jumps to the next student, below pass marks turns red). Kept per exam + class + subject, so several teachers can enter different subjects at once.
- **Results:** Bangladesh GPA-5 (A+ … F), fail in any subject = F, total, merit position. **Mark sheets** (one per page with grade chart), **tabulation sheet** (A4 landscape), result messages to guardians (SMS / WhatsApp, one tap each).
- **Promotion** to the next class: new rolls from the merit list of an exam; failed students stay.
- **Fees:** monthly tuition worked out from admission month (fee changes apply from that month on; waive a month), one-time fees for whole classes (session, exam, sports …), collect any amount (oldest dues first), money receipt (A4 / 80mm), due list and reminders.
- **Reports:** month-by-month collection, class-wise students/boys/girls/due, dues list, exam results by class (pass rate, A+, average GPA). Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several computers.

## Note
The separate project `07_Websites_2026/School Management` (plain JS, school-management-bd.vercel.app) is a different, older full school system. This one is the ZI catalog product on the shared ZI stack.

## Changelog

### v1.0.2 — 28 Oct 2026
- Owner's decision: students who left (TC) are not counted in the total due — on the dashboard, in reports and on the dues lists. Their own ledger still shows what they owe, and the "Left" tab now shows how much the students who left still owe in total.
- Owner's decision: GPA is rounded to 2 decimals (4.666 → 4.67) everywhere — result, mark sheet, tabulation and positions.

### v1.0.1 — 28 Oct 2026
- Exam routine "make routine" put every date one day early (time-zone bug) — dates are now correct and Friday is skipped properly.
- Renaming a subject in a class now keeps the marks already entered for it (and updates the exam routine); before, the marks disappeared from results.
- Re-admission fixed: a student who left and comes back is no longer charged tuition for the months they were away.
- Waived months can be undone (tap the month under the fee list).
- Checks added: guardian mobile must be a real number (Bangla digits ০১৭… work, saved as 017…), roll must be 1 or more, no negative fees, one-time fee amount above 0, same subject cannot be added twice, pass marks between 0 and full marks; exam year typed in Bangla digits is saved correctly.
- Result page: pass rate shows "—" before any result (not 0%), and subjects without marks are no longer shown in red; below-pass marks typed in Bangla digits turn red while entering.
- Accessibility labels for subject full/pass mark boxes and the waive button.
