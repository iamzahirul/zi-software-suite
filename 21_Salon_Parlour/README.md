# ZI Salon — Parlour & Salon Manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

বিউটি পার্লার, জেন্টস স্যালন ও স্পা-এর জন্য: বিউটিশিয়ান অনুযায়ী দিনের অ্যাপয়েন্টমেন্ট বোর্ড, এক বিলে কয়েকটি সার্ভিস (প্রতিটি কে করেছেন), বিকাশ/নগদ/ক্যাশ ভাগ করে পেমেন্ট, স্টাফ কমিশন, ক্লায়েন্টের ইতিহাস ও অ্যালার্জি নোট, ব্রাইডাল বুকিংয়ে অগ্রিম, জন্মদিন ও "অনেক দিন আসেননি" মেসেজ।

- **Online demo:** https://zi-salon-demo.vercel.app → পার্লারের নাম দিন → "স্যাম্পল পার্লার লোড".
- **Bangla tutorial video:** `video/ZI-Salon-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Day board:** one column per beautician, bookings as coloured blocks by time; tap an empty slot to book, tap a booking to mark arrived / make bill / no-show / cancel. Phone view shows a simple list. Clash warning when a beautician is already busy.
- **Booking:** client mobile (old clients recognised with last visit), services with total time, beautician, advance, note, bridal / event flag. One-tap SMS/WhatsApp reminders for tomorrow's bookings.
- **Bill (counter):** tap services from the menu (categories, search), pick who did each one, products sold, discount, optional VAT; the booking's advance is deducted automatically. Split payment (cash + bKash…), change to return. 80 mm thermal or A4 bill.
- **Staff commission:** % per staff (or per service), shared after discount; commission statement per beautician for any period with signature lines.
- **Clients:** visits, total spent, average bill, favourite services, skin / hair type, allergy notes, birthday. Lists for "birthday this week" and "not seen in 45 days" with ready SMS/WhatsApp offers.
- **Expenses & reports:** rent, salary, products, electricity…; reports by staff, service, day, payment method, expense; profit = sales − commission − expenses; print / CSV.
- Service menu with price, time and category; staff with role and board colour.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several branches.
