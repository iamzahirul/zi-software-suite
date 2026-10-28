# ZI Hotel & Resort — Room booking

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

হোটেল, রিসোর্ট ও গেস্ট হাউসের জন্য: রুম বোর্ড (খালি / ভর্তি / আজ আসবেন / আজ ছাড়বেন / অপরিষ্কার / মেরামত), বুকিং ও রুম চার্ট, চেক-ইন ও চেক-আউট, সার্ভিস চার্জ ও ভ্যাটসহ বিল, অতিরিক্ত সেবা, অগ্রিম ও বাকি, অতিথি রেজিস্টার।

- **Online demo:** https://zi-hotel-demo.vercel.app → হোটেলের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Hotel-Resort-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Front desk:** occupancy %, arrivals and departures today, guests in house, collected today, guest dues; colour room board by floor — tap a free room to book / check in, an occupied room to open the guest, a dirty room to mark it cleaned.
- **Booking / walk-in:** dates → only rooms free for those dates are shown (no double booking) → existing guest search or new guest (name, mobile, NID / passport / birth certificate / driving licence, nationality, address) → adults, children, source (walk-in, phone, Facebook, Booking.com, Agoda, corporate, agent), rate, advance. Reserve or check in now.
- **Guest folio:** room nights × rate, extras (food, laundry, extra bed, pickup, minibar, late check-out, damage), discount, service charge % and VAT % (Settings), payments and refunds, due. Change dates / room / rate (checked for clashes), cancel, no-show.
- **Check-out:** final payment, bill print (A4 or 80mm), room goes to "dirty" for housekeeping.
- **Reservations:** 14-day room chart (tap an empty day to book that room), upcoming / in-house / past lists.
- **Guests:** history and spend per guest, VIP flag, notes; **guest register** for any period (name, ID, nationality, address, room, dates) for the police / records; guest registration card for signature.
- **Rooms & rates:** room types with rate, capacity and facilities; rooms with floor and housekeeping state.
- **Accounts & reports:** room revenue, extras, money in by method, expenses (salary, electricity, laundry, OTA commission…), occupancy by day with chart, ADR, RevPAR, room types, booking sources, extra services, guest dues — print or CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for reception + owner's phone.

## Needs from the client
- Nothing paid is required. Channel-manager sync with Booking.com / Agoda (automatic availability) would need their partner API access; here OTA bookings are entered by the front desk.
