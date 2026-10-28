# ZI Coaching — Tuition & Coaching Centre Manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

কোচিং সেন্টার, প্রাইভেট টিউটর ও ব্যাচভিত্তিক পড়ানোর জন্য: ভর্তি, ব্যাচ, হাজিরা, মাসিক বেতন, পরীক্ষার ফলাফল আর অভিভাবককে SMS / WhatsApp।

- **Online demo:** https://zi-coaching-demo.vercel.app → কোচিংয়ের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Coaching-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Batches:** class, subject, days of the week, time, room, teacher, monthly fee; running / closed.
- **Admission:** student, class, school, guardian name and mobile, photo, one or more batches (fee added up automatically, can be changed), admission fee, auto roll/ID (R-A1001…). **ID cards** (8 per A4, photo + barcode).
- **Monthly fees with no monthly work:** every month's fee is worked out from the admission month — nothing to "generate". A fee change applies from that month on (old months keep the old fee). Free / holiday month can be waived. Left students stop being charged.
- **Collect fee:** shows due months and total; any amount is applied oldest month first (partial and advance payments work); money receipt (A4 or 80mm) with months covered and remaining due.
- **Attendance:** pick the batch (today's batches come first) — everyone is present by default, tap the absent ones; then message the absent students' guardians in one step. Monthly attendance sheet print (A4 landscape).
- **Guardian messages:** fee reminder, absent notice, batch notice, exam result — each guardian gets a ready text with their child's name/due/marks; one tap per guardian opens SMS or WhatsApp. "Copy all numbers" for bulk SMS panels.
- **Exams:** marks entry (Enter jumps to the next student), merit position, GPA-5 grade (A+…F), print result sheet, send results to guardians.
- **Teachers & salary** (paid this month / left), **expenses** (rent, electricity, internet, printing …).
- **Reports:** month by month (billed, collected, expenses, net profit), by batch (students, due, attendance %), dues list, low-attendance list, expenses. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for more than one device.

## Notes
- SMS goes through the phone's own SMS app (no SMS gateway cost). If a client wants automatic bulk SMS from a gateway (e.g. BulkSMSBD), that can be added for them.

## Changelog

### v1.0.1 — 28 Oct 2026
- Re-admission fixed: a student who left and comes back is no longer charged for the months they were away.
- Waived (free) months can now be undone — tap the month under the fee list to charge it again.
- "By batch" report no longer counts a student in two batches twice: monthly fee and due are split between the batches by batch fee (totals now match the real due).
- Exam grade: a mark below the exam's own pass mark now shows F (before it could show D but "fail"). Exam form checks full marks > 0 and pass marks ≤ full marks; result sheet shows 85.5% instead of 85.50%.
- Admission checks: guardian mobile must be a real number (Bangla digits ০১৭… work and are saved as 017…), no negative fee / admission fee / batch fee / expense / salary.
- When you add or remove a batch for an existing student whose fee equals the batch total, the monthly fee follows the new batch total (a special/discounted fee is kept).
- Attendance for a past date no longer lists students who were admitted after that day.
- Small accessibility labels added (waive button).
