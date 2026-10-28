# ZI Dealer — Ledger & Warranty Claim

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

মোবাইল অ্যাক্সেসরিজ, ইলেকট্রনিক্স, ইলেকট্রিক্যাল বা যেকোনো ব্র্যান্ডের ডিলার/হোলসেলারের জন্য: ডিলারকে ইনভয়েস (সিরিয়াল / IMEI সহ), ডিলারভিত্তিক বাকি ও খতিয়ান, আদায়, আর ওয়ারেন্টি ক্লেইম (RMA) — কোনটা অফিসে, কোনটা কোম্পানিতে, কোনটা ফেরত দেওয়ার জন্য রেডি।

- **Online demo:** https://zi-dealer-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Dealer-Warranty-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/`. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Dealers:** code, owner, area, district, price level (dealer / sub-dealer / retail), credit limit, opening due; ledger, statement, due list, SMS / WhatsApp due reminder, days since last payment.
- **Invoices:** search & add products, rate by the dealer's price level, serial numbers (one per line or scanned) with count check and duplicate-serial warning, discount, paid now (cash / bKash / Nagad / bank / cheque), credit-limit warning; A4 / A5 / 80mm print with serials, warranty months and terms.
- **Serial check:** type a serial → which dealer, which invoice, sale date, warranty end, earlier claims.
- **Warranty claims (RMA):** serial lookup fills dealer, product, sale date and checks warranty; problem, accessories; claim receipt for the dealer; steps received → sent to company → ready → given back; result repaired / replaced (new serial, from own stock or company) / credit note (taken off the dealer's due) / rejected (with service charge added to the due); late claims (>15 days); claim list (challan) to send to the company.
- **Products & stock:** model, category, three price levels, buy price, warranty months, serial tracking, stock (opening + received − sold − replaced from stock), claim rate % per product, price list print.
- **Reports:** dealer-wise sales & collection, product sales & profit, due aging (0–30 / 31–60 / 61–90 / 90+), claims with turnaround days, claims by product. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several computers.
