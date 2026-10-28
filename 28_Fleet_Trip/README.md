# ZI Fleet — Truck & Trip Manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ট্রাক, কাভার্ড ভ্যান, পিকআপ, বাস বা রেন্ট-এ-কার মালিকের জন্য: প্রতিটি ট্রিপের ভাড়া ও রাস্তার সব খরচ (তেল, টোল, চাঁদা, খাবার, লোড-আনলোড), ট্রিপের লাভ, পার্টির বাকি ভাড়া, ড্রাইভারের বাট্টা ও বেতনের হিসাব, গাড়ির কাগজপত্রের মেয়াদ, মাইলেজ আর মেরামত।

- **Online demo:** https://zi-fleet-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Fleet-Trip-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/` (driver or manager phone). **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Trips:** vehicle, driver, helper, party, from → to (places remembered), goods, start / return date, status (booked / on the road / done / cancelled), start & end km, rent, advance taken at loading, road costs (diesel with litres, toll / bridge / ferry, chanda / terminal, food, loading-unloading, parking, repair on the road, other), driver & helper bata — trip profit worked out live. Trip sheet print (driver's hisab) and trip bill for a party.
- **Vehicles:** registration no, type, model, capacity, owner / partner, driver; papers with expiry — fitness, tax token, route permit, insurance, registration — warning before they expire (also driving licences); odometer and next service due; month profit, mileage (km/l).
- **Parties:** rent due ledger (trip rent − advance − payments), statement, SMS / WhatsApp reminder.
- **Drivers & helpers:** licence no & expiry, salary, daily bata; ledger: trip bata + salary added − paid − advances → what we owe.
- **Fuel & maintenance:** fuel outside trips (litres × diesel price), service / oil change with next-service km, repair, tyre, papers, garage rent, loan installment.
- **Reports:** vehicle profit (rent − road costs − fuel − maintenance), trip list, road costs by head, mileage & cost per km, routes (most run and most profitable), party dues. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).

## Note
GPS tracking needs a tracker device / paid service — the trip log here works without it. Can be linked later if the client has a tracker.
