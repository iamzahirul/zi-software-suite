# ZI Hostel & Mess — Meal count & mess bill

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ব্যাচেলর মেস ও হোস্টেলের জন্য: প্রতিদিনের মিল হিসাব (আধা মিল ও গেস্ট মিলসহ), বাজার, মিল রেট, বাসা ভাড়া-বুয়া-গ্যাস-বিদ্যুতের যৌথ খরচ, সিট ভাড়া, জমা, আর মাস শেষে সবার বিল ও বাকি — সব নিজে নিজে হিসাব হয়।

- **Online demo:** https://zi-mess-demo.vercel.app → মেসের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Hostel-Mess-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Meal count:** every day, every member with + / − (half meals), guest meals charged to the member, "All 2", "All off", "Same as yesterday"; month sheet (members × days) with totals.
- **Bazar:** date, who did the bazar, amount, items; bazar per member; daily bazar chart.
- **Shared costs:** house rent, cook (bua), gas, electricity, water, internet, cleaner, utensils — divided equally among the month's members.
- **Monthly bill:** meal rate = month's bazar ÷ month's meals; each bill = own meals × meal rate + share of shared costs (+ seat rent for hostels); previous due / advance carries over automatically; deposits; due. Print the whole bill sheet (A4 landscape, with signature column) or member slips (4 per A4); send every member the bill by SMS / WhatsApp.
- **Members:** room, seat, seat rent, studies / job, guardian's mobile, join / leave date; month-by-month bills and deposits; deposit receipt (80mm).
- **Dashboard:** running meal rate, meals today, bazar this month, cash in the manager's hand, dues with reminders.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) so the manager and members can share the same data.

## Needs from the client
- Nothing paid is required. Automatic bulk SMS would need an SMS gateway account.
