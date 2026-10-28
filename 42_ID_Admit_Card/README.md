# ZI ID & Admit Card — Card maker

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

স্কুল, কলেজ, মাদ্রাসা, কোচিং ও অফিসের জন্য: ছবিসহ শিক্ষার্থী ও কর্মচারী আইডি কার্ড (সামনে-পেছনে), প্রবেশপত্র (রুটিন ও নিয়মসহ), পরীক্ষার সিট স্টিকার, ইভেন্ট/ভিজিটর পাস — বারকোড বা QR, স্বাক্ষর, A4 কাগজে কাটার দাগসহ বা পিভিসি কার্ড প্রিন্টারে।

- **Online demo:** https://zi-idcard-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-ID-Admit-Card-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **People:** name (Bangla + English), ID no (automatic), group / class, section, roll, designation, department, date of birth, blood group, mobile, father, address, valid till, photo. **Paste a whole list from Excel / Google Sheets** (Bangla or English headings) and **add many photos at once** (file name = ID no or roll).
- **Designs:** five ready-made — student ID classic (landscape), student ID modern (portrait, round photo, QR), staff ID minimal, admit card, exam seat sticker. Each design: style, two colours, title, which fields show, barcode / QR / none, back side with rules and "if found return to", validity; admit cards with exam name, dates, routine (date | time | subject) and rules, 2 or 4 per A4.
- **Make cards:** pick a design and a group, tick people, live preview (front and back), print **10 cards per A4** (CR80 85.6 × 54 mm, 9 for portrait) with cut lines — back pages mirrored for two-sided printing — or **one card per page for PVC ID-card printers**; admit cards 2 / 4 per A4; seat stickers 21 per A4.
- Institution logo, name, address, EIIN, website and the head's signature (image) on every card.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).

## Needs from the client
- Nothing paid is required. PVC cards need an ID-card printer (e.g. Evolis / Zebra) or a print shop; A4 sheets work on any printer (thicker paper or lamination recommended).
