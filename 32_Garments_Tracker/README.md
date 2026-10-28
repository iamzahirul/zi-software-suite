# ZI Garments — Order & Sample Tracker

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

বায়িং হাউস ও ছোট গার্মেন্টস ফ্যাক্টরির জন্য: বায়ার অর্ডার, এক্স-ফ্যাক্টরি থেকে স্বয়ংক্রিয় T&A প্ল্যান, দেরির সতর্কতা, স্যাম্পল (কুরিয়ার/AWB, বায়ারের কমেন্ট), ফ্যাক্টরির পারফরম্যান্স, শিপমেন্ট ও কমিশন।

- **Online demo:** https://zi-garments-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Garments-Tracker-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/` (for merchandisers). **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Orders:** style, PO, item, season, buyer, factory, qty, FOB and factory price (USD), commission %, price term, colours / ratio, fabric, merchandiser, ex-factory.
- **T&A plan (auto):** lab dip, trims, fit sample, fabric booking, PP sample, fabric in-house, size set, cutting, sewing, finishing, final inspection, ex-factory — counted back from the ex-factory date; tap a task to mark done; late tasks in red with days late; re-planned when the ex-factory date moves.
- **T&A agenda:** all late tasks and the next 7 / 14 / 30 days across orders; T&A status print (landscape) for weekly meetings; order sheet print.
- **Samples:** proto, fit, lab dip, PP, size set, photo, shipment; round (re-submission); courier (DHL, FedEx, UPS, Aramex, hand) + AWB; buyer comments; approved / comments / rejected; days waiting; sample list print.
- **Shipments & commission:** shipped qty, invoice, sea / air, vessel; shipped value; commission earned per order (order % or buyer default), commission received, due; commission statement per buyer.
- **Buyers & factories:** order book, commission due; factory compliance (BSCI, WRAP…), capacity, on-time %.
- **Reports:** by buyer, by factory, ex-factory by month, delays, sample approval time. Print / CSV.
- Bangla/English (trade terms in English), dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).
