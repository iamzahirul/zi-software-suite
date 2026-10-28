# ZI Lawyer Case Diary — Hearing dates & fees

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

আইনজীবীদের ডিজিটাল কেস ডায়েরি: প্রতিদিনের কজলিস্ট, মামলার পরবর্তী তারিখ ও কী হলো, ক্যালেন্ডার, মক্কেলকে তারিখের এসএমএস/হোয়াটসঅ্যাপ, চুক্তির ফি, কিস্তি, কোর্ট ফি ও খরচ, বাকি।

- **Online demo:** https://zi-lawyer-demo.vercel.app → চেম্বারের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Lawyer-Case-Diary-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Case diary (home):** any day's cause list (court, case no, parties, purpose), dates today / tomorrow / this week, past dates still to update, cases with no next date, total fee due. Print the cause list (A4 landscape, with the last result and space to write) and remind every client of the date by SMS / WhatsApp.
- **Update a date:** what happened, the next date and its purpose (hearing, hazira, bail, charge framing, witness, argument, order, judgment), case status — the next date goes straight into the diary.
- **Calendar:** month view with the number of dates per day (red = not updated), Friday/Saturday shaded, tap a day for its list.
- **Cases:** case no, type (civil, criminal, family, land, cheque-dishonour 138, writ, labour, commercial), court (with common BD courts), section / law, both parties, our side (plaintiff, defendant, petitioner, respondent, complainant, accused), opponent's lawyer, police station, filed on, status (running, stayed, disposed, in appeal, withdrawn), result. Full timeline of dates; printable case summary.
- **Clients & fees:** clients with all their cases, agreed fee, instalments with fee receipt (A4 / 80mm), expenses (court fee, stamp, muhuri, certified copy, notice…) optionally billed to the client, due per case and per client, statement, fee reminders.
- **Reports:** dates in a period, courts, case types, status, fee dues, disposed cases — print or CSV.
- Advocate's name, bar membership and chamber on every print. Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for advocate + junior/muhuri.

## Needs from the client
- Nothing paid is required. Automatic bulk SMS would need an SMS gateway account; online cause-list download from the Supreme Court site is not included.
