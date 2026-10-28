# ZI Bari Vara — Rent Manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

বাড়িওয়ালা ও বিল্ডিং ম্যানেজারের জন্য: ফ্ল্যাট ও দোকান, ভাড়াটিয়ার তথ্য, মাসিক বিল (ভাড়া + সার্ভিস চার্জ + গ্যাস + পানি + মিটার অনুযায়ী বিদ্যুৎ), ভাড়া আদায় ও মানি রসিদ, বাকি, খরচ ও নিট আয়।

- **Online demo:** https://zi-rent-demo.vercel.app → নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Bari-Vara-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Buildings, flats & shops:** several buildings, unit no, floor, type (flat / shop / room / garage / office), usual rent and charges, meter no. Vacant units in green; **TO-LET poster** print.
- **Tenants:** photo, mobile, NID, occupation, permanent address, family members, emergency contact, move-in date, rent, service charge, gas, water, advance (security deposit). **Tenant information form** (for the police station / ward office) printable.
- **Monthly bills:** one tap makes everyone's bill; type each electric meter reading — units × rate = electricity bill; extra charges (repairs share…). Bills print 2 per A4 with old dues; SMS / WhatsApp each tenant their bill.
- **Rent collection:** cash / bKash / Nagad / bank; oldest months cleared first; money receipt (A4 / 80mm) shows which months were paid. Tenant statement.
- **Moving out:** take dues from the advance and see how much to return.
- **Expenses:** guard, cleaner, common electricity, repairs, holding tax, lift…
- **Reports:** month by month (billed, collected, expenses, net income), flat-wise income and months let, dues list, expenses by category. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for owner + caretaker phones.

## Changelog

### v1.0.1 — 28 Oct 2026
- Money receipt printed right after taking rent now shows the correct "due now" (before, it ignored the payment just taken and showed too much due).
- New: monthly adjustment from the advance — e.g. ৳5,000 of a shop's advance is adjusted against each month's rent automatically when the month's bills are made, until the advance runs out. The tenant page, statement and "advance held" show what is left.
- Moving out: the amount to return now counts rent paid in advance and what was already adjusted, and shows any amount still due after using the advance.
- New tenant form: choosing a flat fills its rent and charges when left empty; with only one vacant flat it is chosen for you; the form no longer shows a flat or tenant as selected when none is (this used to give a "fill required fields" error).
- Checks: negative rent / charges / payments / expenses and wrong mobile numbers are refused with a clear message.
- Tenant information form prints "Photo" in English mode (was always Bangla); phone layout of the tenant header fixed.
