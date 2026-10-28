# ZI Travel Agency — Ticket, visa & Hajj-Umrah

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ট্রাভেল এজেন্সির জন্য: বিমান টিকেট বিক্রি (PNR, টিকেট নং, হোল্ড/টাইম লিমিট, রিফান্ড), ভিসা প্রসেসিং, হজ ও ওমরাহ গ্রুপ, ট্যুর ও হোটেল বুকিং, কাস্টমারের বাকি, ভেন্ডর (কনসোলিডেটর) দেনা, লাভ-ক্ষতি।

- **Online demo:** https://zi-travel-demo.vercel.app → এজেন্সির নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Travel-Agency-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Air tickets:** passenger, passport, airline, route (DAC-DXB-DAC), travel / return date, class, PNR, ticket no, hold with time limit, issued / flown / void. Buying cost (consolidator) and selling price → profit per ticket. **Refund:** airline penalty + service charge kept, the rest paid back.
- **Visa processing:** country, visa type, submit and delivery dates, status (collecting papers → submitted → approved / rejected → delivered).
- **Hajj & Umrah groups:** package price, departure / return, seats, airline, Makkah & Madinah hotels, group leader; each pilgrim with passport, tracking / pre-registration no, maharam, status, vaccine and ID-card checklist, due; printable group list. Tour groups the same way. Hotel bookings and any other service.
- **Customers:** quick add while booking, corporate clients, passport expiry warnings (under 6 months), total due, statement, due reminders by SMS / WhatsApp.
- **Vendors:** consolidators, embassy agents, Hajj agencies, hotels — bought, paid, payable, statement, pay vendor.
- **Dashboard:** today's and this month's sales & profit, receivable, payable, next 7 days (travel dates, visa deliveries, ticket time limits) with one-tap SMS, 14-day profit chart.
- **Accounts:** sales, profit, office expenses, net profit, money in / out, refunds to customers.
- **Reports:** by service, day by day, airlines, visa by country, customer dues, vendor payables — print or CSV (Excel).
- **Print:** invoice and money receipt (A4 or 80mm) with IATA / licence no, statements, group list.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several counters.

## Needs from the client
- Nothing paid is required. GDS / airline API booking is not included (tickets are issued in the consolidator's portal and recorded here). Automatic bulk SMS would need an SMS gateway account.
