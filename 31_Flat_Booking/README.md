# ZI Flat — Booking & Installment

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

রিয়েল এস্টেট ডেভেলপারদের জন্য: প্রজেক্ট ও তলাভিত্তিক ফ্ল্যাট/দোকান/পার্কিং, জমির মালিকের অংশ, বুকিং ও কিস্তির শিডিউল, মানি রসিদ (কথায় টাকাসহ), বরাদ্দপত্র, বকেয়া তাগাদা (প্রবাসী ক্রেতাসহ) আর আদায়ের রিপোর্ট।

- **Online demo:** https://zi-flat-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Flat-Booking-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/`. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Projects & floor plan:** the building floor by floor; each unit coloured available / booked / fully paid / landowner / on hold; make all units at once (floors × A B C), size, rate per sft, parking & utility charge, beds, baths, facing.
- **Booking:** customer (NID, phone, nominee, lives abroad), price, discount, booking money, down payment, N installments every 1 / 3 / 6 months, first due date, handover, sold by (agent) — the whole schedule shows before saving.
- **Booking page:** each installment paid / part / late / due; payments matched oldest first; next due; overdue since; allotment letter with schedule and your terms; statement; cancel with refund (deduction kept).
- **Money receipt:** A5, amount in words, total paid and balance; refund voucher.
- **Overdue & follow-up:** who is late since when and how much; due in 30 days; SMS / WhatsApp reminders; overdue list print.
- **Collections:** receipts by date, refunds, due in the next 30 days.
- **Reports:** month-wise scheduled vs collected (%), project summary (units, sales value, collected, receivable, overdue, unsold value), unit inventory, overdue aging (0–30 / 31–90 / 90+), sales by agent. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).
