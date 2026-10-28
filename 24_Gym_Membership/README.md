# ZI Gym — Gym & Fitness Center Manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

জিম ও ফিটনেস সেন্টারের জন্য: মেম্বার (ছবি, রক্তের গ্রুপ, স্বাস্থ্য তথ্য), প্যাকেজ ও রিনিউ, মেয়াদ শেষের আগে রিমাইন্ডার, আইডি কার্ড স্ক্যান করে হাজিরা, পার্সোনাল ট্রেইনার, ওজন-বিএমআই অগ্রগতি, মানি রসিদ, বাকি ও খরচ।

- **Online demo:** https://zi-gym-demo.vercel.app → জিমের নাম দিন → "স্যাম্পল জিম লোড".
- **Bangla tutorial video:** `video/ZI-Gym-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Front desk check-in:** type the member ID / mobile or scan the ID card barcode and press Enter — photo, status, expiry, due and health note show at once; warning if the membership has expired.
- **Members:** photo, gender, date of birth, blood group, batch (morning / evening / ladies), goal, trainer, emergency contact, health notes (BP, diabetes, injury); lists for active, expiring soon, expired, with due.
- **Packages & renewal:** monthly, 3 / 6 months, yearly, with personal trainer; start date continues from the current expiry; admission fee on the first membership, PT fee, discount, partial payment (due), cash / bKash / Nagad / card; 80 mm money receipt.
- **Reminders:** "expiring soon" and "expired — call back" lists with one-tap SMS / WhatsApp renewal messages.
- **ID cards:** credit-card size cards with photo, member ID, barcode, blood group and validity — 10 on an A4 page.
- **Attendance:** daily check-ins, busy hours, last 14 days; visits per member.
- **Body progress:** weight, height, BMI, waist, chest, arm, body fat — history with weight chart.
- **Trainers:** salary, PT share, PT members.
- **Reports & expenses:** day by day, packages sold, payment methods, dues, expenses (rent, salary, electricity, equipment…), profit; print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several branches.
