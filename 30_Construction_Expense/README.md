# ZI Site — Construction Expense Tracker

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ঠিকাদার ও ডেভেলপারদের জন্য: প্রতিটি সাইট/প্রজেক্টের খাতভিত্তিক বাজেট, মালামাল ক্রয় ও সাইটের স্টক, প্রতিদিনের শ্রমিক হাজিরা, সাপ্লায়ার ও সর্দারের দেনা, সাইট ম্যানেজারের পেটি ক্যাশ, ক্লায়েন্টকে রানিং বিল আর এ পর্যন্ত লাভ।

- **Online demo:** https://zi-site-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Construction-Site-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/` (for site managers). **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Projects:** client, location, contract value, site manager, start / handover, budget by head (material, labour, machine rent, transport, utility, permit, food, site office, other); spent vs budget bars (red when over), client due, petty cash in hand, profit so far.
- **Material purchase:** several items on one supplier memo (cement bags, rod tons, bricks, sand / stone cft, tiles…), carrying cost, paid now — the rest goes to the supplier's ledger. Standard BD materials and units come ready.
- **Site stock:** bought − used per material per site (write material used) — waste and theft show up.
- **Labour hajira:** daily masons, helpers, rod mistri, carpenter… with daily rate, under a sardar (owed) or own workers (paid the same day); overtime; hajira sheet print.
- **Expenses & petty cash:** cash given to the site manager and what he spent (voucher no); office expenses; by-head chart.
- **Suppliers & sardars:** what we owe each, full ledger, statement print, payments by cash / bank / cheque / bKash.
- **Client running bills:** bill no, work done, previous bills, this bill, received so far, payable now — print; receipts.
- **Reports:** project cost by head, period cost, material bought with average rate, labour man-days by trade, what we owe, client bills. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, works offline at the site; optional cloud sync (Supabase) with the office.
