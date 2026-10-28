# ZI Used Phone — Pre-owned Phone Buy & Sell Register

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

পুরাতন মোবাইল কেনাবেচার দোকানের জন্য: প্রতিটি ফোনের IMEI, বিক্রেতার এনআইডি ও ছবি, NEIR (চুরি / অনিবন্ধিত) যাচাই, গ্রেড ও ব্যাটারি, ওয়ারেন্টিসহ বিক্রি, এক্সচেঞ্জ, আর থানায় দেখানোর মতো ক্রয়-বিক্রয় রেজিস্টার।

- **Online demo:** https://zi-usedphone-demo.vercel.app → দোকানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Used-Phone-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Buying:** brand, model, RAM / storage, colour, IMEI 1 & 2 (check-digit validation catches typing mistakes; warns if the IMEI was in the shop before), grade A–D, battery health, accessories, problems, phone photos.
- **NEIR check:** one tap opens an SMS "KYD <IMEI>" to 16002 (BTRC); record the result (OK / problem) — a phone with a NEIR problem cannot be sold.
- **Seller KYC:** name, mobile, NID number, address, seller photo and NID front / back photos. **Purchase slip** with the seller's declaration ("not stolen, lawfully owned") and signature lines.
- **Selling:** buyer details, price, cash / bKash / Nagad / card, checking warranty days, sale invoice with terms. **Exchange:** the buyer's old phone is valued, deducted, and goes into stock as a new purchase linked to the sale.
- **Stock:** in stock / in repair (repair cost added to the phone's cost) / sold / returned to seller; days in stock, old stock alert, asking price, profit per phone.
- **IMEI lookup:** was this phone bought or sold here before, from whom.
- **Register & reports:** buy–sell register for any period (A4 landscape) with both parties' NID and IMEI — for the police / market committee; CSV; profit per month and by brand.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several branches.
