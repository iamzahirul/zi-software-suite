# ZI Repair — Mobile Servicing Job Card

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

মোবাইল, ল্যাপটপ ও ইলেকট্রনিক্স সার্ভিসিং দোকানের জন্য: জব কার্ড (IMEI, প্যাটার্ন লক, জমার সময় অবস্থা), কাজের ধাপ, পার্টস স্টক, রেডি হলে SMS / WhatsApp, ডেলিভারির বিল, মেরামত ওয়ারেন্টি ও ওয়ারেন্টিতে ফেরত, টেকনিশিয়ান কমিশন।

- **Online demo:** https://zi-repair-demo.vercel.app → দোকানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Repair-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Job card intake:** mobile (old customers recognised with their past devices), name, device type, brand, model, IMEI / serial, colour; problems (tick list + customer's words); **condition on arrival** (screen / back cracked, scratches, dent, no power, opened before) to avoid disputes; accessories received; **screen lock** — PIN or tap-to-draw **pattern** (printed only on the shop copy); device photos; estimate, advance, promised date, technician, urgent.
- **Print:** job card with customer copy + shop copy (barcode, terms & conditions), 80mm option; device / bag sticker with barcode (58mm); repair bill with payments and warranty date.
- **Status flow:** received → checking → waiting for parts → repairing → ready → delivered (or returned unrepaired / cancelled), with a time-stamped history.
- **Parts:** from stock (stock goes down, comes back if removed) or custom; buy / sell price; the first parts come out of the estimate so the bill stays as quoted.
- **Ready message:** one-tap SMS / WhatsApp with device, job no and due; "message all" for devices not collected; days waiting.
- **Delivery:** take the due, set warranty days, print bill. **Warranty come-back** opens a new job linked to the old one.
- **Find job** by job no, mobile, IMEI or name; late jobs (past promised date).
- **Reports:** received / delivered, bill, parts cost, profit, cash taken; technician-wise jobs, profit and commission (% of service charge); brands; problems; day by day. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for counter + technician bench.
