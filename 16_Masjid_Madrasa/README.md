# ZI Masjid & Madrasa — Donation & Fee

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

মসজিদ কমিটি ও মাদ্রাসার জন্য: মাসিক চাঁদা, তহবিল অনুযায়ী দান (সাধারণ, নির্মাণ, রমজান, যাকাত, ফিতরা, কুরবানি, লিল্লাহ), জুমার দানবাক্স, ছাত্রদের মাসিক বেতন, খরচ, আর নোটিশ বোর্ডের জন্য মাসিক আয়-ব্যয়ের হিসাব।

- **Online demo:** https://zi-masjid-demo.vercel.app → মসজিদের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Masjid-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Monthly donors:** promised monthly chanda (amount changes keep history), month boxes green / red, dues and reminders (SMS / WhatsApp), stop / restart, yearly donation statement.
- **Donations:** any donor or anonymous, any fund (add your own funds), cash / bKash / Nagad / bank, receipt (A4 / 80mm) with "JazakAllahu khairan". **Donation box** (Jumma box) entry.
- **Madrasa students:** class (Nurani, Nazera, Hifz, Kitab…), roll, guardian, boarding, monthly fee (0 for lillah students), fee collection with month-wise receipts and dues.
- **Expenses by fund:** imam / muazzin / teacher honorarium, electricity, construction, iftar, students' food…; warns when a fund is short.
- **Monthly account notice:** big A4 sheet — income by type, expense by type, last month's balance, this month, current balance, signature lines for cashier, secretary and president.
- **Reports:** month by month, fund balances, donors list, dues. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for the cashier and committee members.

## Changelog

### v1.0.1 — 28 Oct 2026
- Editing a donor or student (for example only the phone or address) no longer quietly changes their monthly chanda / fee back to the first amount ever set; the form now shows the amount in force.
- Receipt printed right after taking chanda or a fee now shows the correct "still due" (before, it ignored the payment just taken).
- Zero or negative amounts and wrong mobile numbers are refused with a clear message (donations, box count, expenses, donors, students).
- Monthly notice print title shows the month name; phone layout of the donor / student header fixed.
