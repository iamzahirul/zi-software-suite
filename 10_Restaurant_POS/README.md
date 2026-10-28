# ZI Restaurant — Tables, KOT & Bills

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

রেস্টুরেন্ট, ক্যাফে ও ফাস্ট ফুডের জন্য: টেবিলে অর্ডার, কিচেন টিকিট (KOT), কিচেন স্ক্রিন, বিল ও ভাগ করে পেমেন্ট, পার্সেল ও হোম ডেলিভারি, দিনের রিপোর্ট ও লাভ।

- **Online demo:** https://zi-resto-demo.vercel.app → রেস্টুরেন্টের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Restaurant-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Floor plan:** all tables by area (ground floor, family cabin, rooftop…). Free / running, running bill, minutes seated, waiter; a table turns blue when its food is ready.
- **Order screen:** menu by category, search or short code, tap to add, +/−, kitchen note per item ("less spicy"), waiter, guests. Move to another table, cancel order.
- **KOT (kitchen order ticket):** "Send to kitchen" sends only the new quantities; 80mm KOT print (can switch off). Bottled drinks / counter items never go to the kitchen.
- **Kitchen screen (KDS):** tickets oldest first, turns orange after 15 min and red after 25 min; Ready → Served. Open it on a kitchen tablet/phone (with cloud sync).
- **Bill:** pre-bill, discount (৳ or %), service charge %, VAT %, delivery charge; split payment (cash + bKash/Nagad/card), change to return; 80mm bill print with your note.
- **Takeaway & home delivery:** customer name, mobile, address, delivery charge.
- **Orders & bills:** today / any range, running / paid / cancelled, reprint bill and KOTs.
- **Menu & tables:** price, food cost per plate (margin %), short code, available on/off; tables with area and seats.
- **Expenses:** bazar, gas, rent, salary, bills…
- **Reports:** sales, bills, average bill, estimated food cost, expenses, net profit (sales − VAT − expenses); day by day, item-wise, category, waiter, dine-in vs takeaway, payment methods; day-end report on 80mm; print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for cash counter + kitchen + owner's phone.

## Changelog

### v1.0.1 — 28 Oct 2026
- Takeaway and home-delivery orders paid at the counter before cooking now go to the kitchen automatically when you take payment, and stay on the kitchen screen until served (before, a paid order disappeared from the kitchen screen).
- Pay screen warns when dine-in items were never sent to the kitchen.
- A minus discount, service charge, VAT or delivery charge can no longer raise or break the bill; minus quantity or price on an item is refused (before it showed a wrong "already sent to kitchen" question).
- When a customer pays more by bKash/card than the bill, the extra is counted as change, not as bKash/card income (payment-method report and day report are now correct).
- Kitchen screen beeps when a new ticket arrives.
- Menu price/cost and expense amounts cannot be minus.
- Search works with Bangla digits (table ২, order numbers).
- Bangla wording: "৪টি বিল", "৪টি চলমান অর্ডার" (no stray space).
