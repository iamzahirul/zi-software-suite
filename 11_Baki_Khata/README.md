# ZI Baki Khata — Customer & Supplier Ledger

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

মুদি দোকান, পাইকারি ও যেকোনো ছোট ব্যবসার জন্য: কাস্টমারের বাকি (দিলাম / পেলাম), মহাজনের দেনা, তাগাদা SMS / WhatsApp, প্রতিদিনের ক্যাশ বক্স, রসিদ ও হিসাব বিবরণী।

- **Online demo:** https://zi-khata-demo.vercel.app → দোকানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Baki-Khata-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Customers & suppliers (মহাজন):** name, mobile (duplicates blocked), area, address, old balance from the paper khata, credit limit (warns before going over).
- **Khata page:** big balance (পাবো red / দেবো green), call button, **দিলাম** and **পেলাম** buttons; for suppliers "মাল নিলাম (বাকি)" and "টাকা দিলাম". Each entry: amount, date, what was given, pay-by date, cash / bKash / Nagad / Rocket / bank, memo photo. Running balance on every line.
- **Money receipt** for every payment (MR-… numbers, A4 or 80mm). **Statement** (হিসাব বিবরণী) for any date range on A4.
- **Reminders (তাগাদা):** overdue list (pay-by date passed, or older than N days), filter by area, tick who to message; each message has their name and due amount; one tap SMS / WhatsApp (uses the phone's own SMS — no SMS gateway or monthly fee). Copy all numbers for a bulk-SMS panel. Printed due list for the collector.
- **Cash box (ক্যাশ বক্স):** day by day — opening cash, cash sales and collections, expenses, supplier payments, bank deposits, closing cash.
- **Reports:** month by month (baki given, collected, bought on credit, paid to suppliers), due by age (0–30 / 31–60 / 61–90 / 90+ days), area-wise due, cash in/out by category, supplier summary. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for phone + shop computer.

## Note
SMS go out from the shop owner's own phone (SMS / WhatsApp app). Automatic bulk SMS needs a paid SMS gateway account (e.g. BulkSMSBD / SSL Wireless) — can be added on request with the client's API key.

## Changelog

### v1.0.1 — 28 Oct 2026
- New: send any khata entry to the customer by SMS or WhatsApp ("on 25/10 you took ৳840 on baki — your due ৳9,830"), from the message button on each ledger line.
- Old balance (আগের বাকি / দেনা) can now be corrected later from Edit — before it could only be typed once.
- Due age fixed: a customer added before 6 am no longer shows "1 day" old on the first day.
- Minus amounts are refused in the cash box (and a minus credit limit is saved as no limit).
- Statement: balances read "You will get / You will give ৳…" instead of minus numbers, with totals of gave/got for the period.
- Tapping the print button on a ledger line no longer also opens the edit form.
- Phone numbers typed in Bangla digits are saved as normal digits.
- Cash in/out report names khata cash lines correctly (cash lent to a customer is no longer shown as "paid to suppliers"); delete now confirms with a message.
- বাংলা: প্রতিটি লেনদেন কাস্টমারকে এসএমএস/হোয়াটসঅ্যাপে পাঠানো যায়, আগের বাকি পরে ঠিক করা যায়, বিবরণীতে মাইনাসের বদলে "পাবো/দেবো"।
