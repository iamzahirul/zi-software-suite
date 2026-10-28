# ZI Laundry — Laundry & Dry-clean Order Tracker

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

লন্ড্রি ও ড্রাই ক্লিনারের জন্য: কাউন্টারে চাপ দিয়ে কাপড় জমা (ধোয়া-আয়রন / ড্রাই ক্লিন / শুধু আয়রন, পিস বা কেজি), দাগ-ছেঁড়া নোট, প্রতিটি পিসের ট্যাগ, জরুরি ও হোম ডেলিভারি চার্জ, কোন র‍্যাকে রাখা, রেডি মেসেজ, বাকি আর হোটেল-মেসের মাসিক হিসাব।

- **Online demo:** https://zi-laundry-demo.vercel.app → লন্ড্রির নাম দিন → "স্যাম্পল লন্ড্রি লোড".
- **Bangla tutorial video:** `video/ZI-Laundry-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Counter:** price list grid (men, ladies, household, by weight), switch service (wash & iron / dry clean / iron only), tap to add; pieces, pairs, kg or sq ft; condition chips per line (stain, torn, button missing, colour may run, may shrink, item in pocket) and a note.
- **Charges:** express (% on top, faster delivery date), home delivery charge, discount, advance by cash / bKash / Nagad / card; old due shown when the customer's mobile is typed.
- **Prints:** memo (80 mm or A5) with barcode, terms and conditions; **piece tags** on 58 mm — order no., piece k/N, item, service, delivery date, express mark.
- **Stages:** received → washing → ready (choose the rack / shelf) → out for delivery → delivered; one-tap "ready" SMS / WhatsApp; delivery with payment and a "count the pieces" reminder.
- **Dashboard:** search by order no., mobile or rack; received today, in progress, ready on the rack, cash today, due; due today, ready list, home deliveries today.
- **Customers:** history and due; **monthly account customers** (hotel, mess, office) with a printable account statement.
- **Reports & expenses:** day by day, by item, by service, payment methods, expenses (detergent, gas, electricity, salary, rent…), profit.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several branches.
